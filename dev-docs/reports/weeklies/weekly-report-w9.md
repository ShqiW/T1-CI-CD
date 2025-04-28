
# Week 9

# Completed tasks

> List completed (DONE) tasks, include
> 1. A link to the Issue
> 2. The total weight (points or T-shirt size) allocated to the issue

| Task                                                                                                                         | Weight |
|------------------------------------------------------------------------------------------------------------------------------| ------ |
| [Feature: Implement StatusService to Return Detailed Pipeline Status](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/243) |   2     |
| [Feature: Introduce MinIO integration into the worker service to store Docker job logs](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/249)                              |    5    |
| [Enhance CLI Report Querying Capabilities](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/244)                            |   3     |


> I see Weight points on your weeklies but I do not see those in your issues on GitHub. 
> Also having everything as 2 points seems odd to me. 
> The reason we add points is to both show what the team thinks is the estimated **amount of work** needed to complete the issue. With time the team gets better at estimating tasks and it becomes a measure of the teams output per sprint. This measure is a good indicator that tells the team if a sprint has too much or too little work. 
> Please try to add points!
> Sure. I added more weight and wrote in each issue.

# Carry over tasks

> List all issues that were planned for this week but did not get DONE
> Include
> 1. A link to the Issue
> 2. The total weight (points or T-shirt size) allocated to the issue
> 3. The team member assigned to the task. This has to be 1 person!

| Task | Weight | Assignee |
| ---- | ------ | -------- |
| [Make sure the pipeline can run without calrifing workingDir in the yaml file](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/258) | 1 | Wenxue Fang |

# New tasks

> List all the issues that the team is planning to work for next sprint
> Include
> 1. A link to the Issue
> 2. The total weight (points or T-shirt size) allocated to the issue
> 3. The team member assigned to the task. This has to be 1 person!

| Task | Weight | Assignee    |
| ---- |---|-------------|
| [Remote Repo Local CI/CD Run](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/256) | 10 | Shenqian Wen |
| [Connect docker and k8s](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/257) | 10 | Wenxue Fang |
| [Have a flexible team member for final verification checks](https://github.com/CS6510-SEA-SP25/t1-cicd/issues/259) | 10 | Limingtian Fang |


> Do not work on Authentication/Authorization. This is not a feature that is prioritized at the moment. 
> If some of the software you are using has login/passwords make sure we use those to get the software to work correclty but do not go any further than that on authentication/authorization.
> Got it. Delete the Authentication/Authorization task. Added related task based on our in-class discussion.

# What worked this week?

*  Structured Backend Enhancements: Implementing StatusService greatly improved traceability by delivering detailed pipeline status reports. This helped with debugging and visualizing execution flows.
*  Effective Logging: Integrating MinIO for Docker job logs centralized log access and decoupled log storage from the container lifecycle. Lightweight and easy to run locally.
*  Flexible CLI Querying: Adding structured, multi-format report queries enhanced our team’s ability to quickly inspect historical pipeline executions. --format json was particularly useful for tooling integration.

# What did not work this week?

 * MinIO not auto-started: MinIO must be manually launched with Docker every time, which caused issues during development and CI testing. We plan to improve this with automated local bootstrap or embedded test support.
 * Slow MinIO Startup: MinIO takes a long time to start up, which slows down development and testing. We will explore ways to speed up MinIO startup time for better efficiency.
 * Status aggregation in deploy stage: While StatusService correctly retrieves and aggregates pipeline execution data, we encountered cases where the deploy stage was marked as FAILED despite some jobs (like build-jar) succeeding. This inconsistency stems from partial job failures within a stage, which we will handle more explicitly in future status aggregation logic.

# Design updates

 * Implemented a new StatusService in the backend to support detailed pipeline execution inspection. This service aggregates job-level status data and provides a comprehensive view of pipeline execution progress. * The StatusService is designed to be extensible and can be easily integrated with other services for enhanced monitoring and reporting capabilities.
 * Introduced MinIO integration to store logs persistently.
 * Extended CLI report tooling to allow filtering by pipeline, run number, stage, and job with configurable output formatting. This feature enables users to quickly query and analyze historical pipeline executions for debugging and performance tuning.


 > Good output this sprint. Keep it up!
 > Definately! Thank you very much.
