# ASSIGNMENT: Sampling and Reproducibility in Python

Read the blog post [Contact tracing can give a biased sample of COVID-19 cases](https://andrewwhitby.com/2020/11/24/contact-tracing-biased/) by Andrew Whitby to understand the context and motivation behind the simulation model we will be examining.

Examine the code in `whitby_covid_tracing.py`. Identify all stages at which sampling is occurring in the model. Describe in words the sampling procedure, referencing the functions used, sample size, sampling frame, any underlying distributions involved, and how these relate to the procedure outlined in the blog post.

Run the Python script file called whitby_covid_tracing.py as is and compare the results to the graphs in the original blog post. Does this code appear to reproduce the graphs from the original blog post?

Modify the number of repetitions in the simulation to 100 (from the original 1000). Run the script multiple times and observe the outputted graphs. Comment on the reproducibility of the results.

Alter the code so that it is reproducible. Describe the changes you made to the code and how they affected the reproducibility of the script file. The output does not need to match Whitby’s original blogpost/graphs, it just needs to produce the same output when run multiple times

# Author: Aidan Campbell

```
P1
I think there are three instances of sampling (?) but I am confident that the latter two I outline (both instances of contact tracing) are samples.
For the first, the initial infection sampling defined by the variable "infected_indices" using the funtion np.random.choice samples members of the population and adds the trait infected (via ATTACK_RATE) at a probability of 10% (i.e., ~100 ppl). I'm less sure of this because it seems to be absolute. Everyone sampled by this funtion is infected. So, it's the "population" of infected people, but a sample of the original population. This is the "iid" step of the blog - each person has a 10% chance of infection. It would be a uniform distribution that's discrete.
The second is the primary contact tracing portion. This usess the function np.random.rand to randomly select ONLY infected people to be successfully traced at a rate of TRACE_SUCCESS (20%). This sample is also ~100 people as you've sampled each infected person. TRACE_SUCCESS determines if "you" will successfully trace their cotanct back to a particular event/source. It corresponds with the part of the blog post outlining the imperfections of contact-tracing (i.e., there's only a 20% chance of the infection being traced). This would be a binomial distribution.
The final instance is the follow-up/secondary trace. This part uses the .value_counts and .index to count the trace cases by event and then filters all events with 2 or more traces. Because of the TRACE_SUCCESS rate of 0.2, it'd be about 20 traced cases. This corresponds with the portion of the blog post assuming that if 2 or more cases are found to trace to the same event, an effort would be made to test anyone attending that event (leading to all infection from that event being identified). Not sure about this distribution, it's a sample of a binomial distribution which was sampled from a uniform distribution. Binomial as well would be my guess.

P2
After running the script, it appears that the graph mostly reproduces the blog post's graph, albeit skewed right. That is, the graph demonstrates it's highly likely that we would detect any infection occurring at an event like a wedding as opposed to a brunch.

P3
Reducing the number of repititions, of course, leads to higher variability in observed distributions. When we increase that number, we better approximate the expected "true" values. The distributions observed here centered randomly around proportions such as 0.15 or 0.4 - though many did land on 0.2-0.25.

P4
I set the random.seed to 12321 as I lacked creativity to find a more meaningful number. This just sets operations using RNG to the same starting point (as per comment, not sure what that means exactly - but I understand the essence of it). This ensures that the outputs remain the same each run.

```


## Criteria

|Criteria|Complete|Incomplete|
|--------|----|----|
|Altercation of the code|The code changes made, made it reproducible.|The code is still not reproducible.|
|Description of changes|The author explained the reasonings for the changes made well.|The author did not explain the reasonings for the changes made well.|

## Submission Information

🚨 **Please review our [Assignment Submission Guide](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md)** 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

### Submission Parameters:
* Submission Due Date: `23:59 - 09/04/2025`
* The branch name for your repo should be: `assignment-1`
* What to submit for this assignment:
    * This markdown file (a1_sampling_and_reproducibility.md) should be populated.
    * The `whitby_covid_tracing.py` should be changed.
* What the pull request link should look like for this assignment: `https://github.com/<your_github_username>/sampling/pull/<pr_id>`
    * Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.

Checklist:
- [ ] Create a branch called `assignment-1`.
- [ ] Ensure that the repository is public.
- [ ] Review [the PR description guidelines](https://github.com/UofT-DSI/onboarding/blob/main/onboarding_documents/submissions.md#guidelines-for-pull-request-descriptions) and adhere to them.
- [ ] Verify that the link is accessible in a private browser window.

If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via the help channel in Slack. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.
