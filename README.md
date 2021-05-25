<h1>Background</h1>

<p>Today you will become part of Discovery department at Wikimedia Foundation for a day. Your team just made a big change to the <a href = "https://www.wikipedia.org/">Wikipedia Search</a> experience and ran an A/B test to determine whether the new version of the search is better than the old one. It is your task to analyze the data and prepare a brief explaining the results of the test.</p> 

<p>Discovery team relies on event logging (EL) to track a variety of performance and usage metrics to help the team make decisions. Specifically, Discovery is interested in:</p> 

<ul>
    <li><em>clickthrough rate</em>: the proportion of search sessions where the user clicked on one of the results displayed </li>
    <li><em>zero results rate</em>: the proportion of searches that yielded 0 results </li>
</ul>

<p>and other metrics outside the scope of this task. Event Logging uses JavaScript to asynchronously send messages (events) to Discovery servers when the user has performed specific actions.</p>

<h1>Data</h1>

<p>The dataset comes from a <a href = "https://meta.wikimedia.org/wiki/Schema:TestSearchSatisfaction2">tracking schema</a> that Discovery uses for assessing user satisfaction. Desktop users are randomly sampled to be anonymously tracked by this schema which uses a "I'm alive" pinging system to estimate how long users stay on the pages they visit. The dataset contains just a little more than a week of EL data.
The following are possible values for the action field of an event:</p>

<ul>
    <li><b>searchResultPage</b>: when a new search is performed and the user is shown a search results page. </li>
    <li><b>visitPage</b>: when the user clicks a link in the results. </li>
    <li><b>checkin</b>: when the user has remained on the page for a pre-specified amount of time.</li>
   </ul>
   
   <h1>Tasks</h1>
<ol>
    <li>Create a new measure called # of Sessions that counts distinct session IDs and visualize the number of sessions per day split by group (A and B).</li>
    <li>Calculate the overall split of sessions between group A and B (what % of sessions were exposed to the new search experience vs the old one). Check if the split was balanced enough (we are expecting 50/50 split) using <a href = "https://www.gigacalculator.com/calculators/sample-ratio-mismatch-calculator.php">this Sample Ratio Mismatch calculator</a>. You can read more on Sample Ratio Mismatch and why it's important <a href = "https://blog.analytics-toolkit.com/2019/does-your-a-b-test-pass-the-sample-ratio-mismatch-test/">here</a>.</li>
    <li>Calculate the Click Through Rate by group (A and B) and determine whether the difference in Click Through Rates is statistically significant using <a href = "https://abtestguide.com/calc/">this</a> or any other AB test calculator.</li>
    <li>Calculate the Zero Results Rate by group (A and B) and determine whether the difference in Zero Results Rates is statistically significant using this or any other AB test calculator.</li>
    <li>[Optional] Create a new measure called Session Length (the time between the first event and the last event in a session) and build a visualization that shows distribution of session length by group (A and B). Which group tends to have longer sessions?</li>
    <li>Put all the graphs together into a Tableau Story and add the necessary comments so that your business stakeholders understand the outcomes of the A/B test.</li>


