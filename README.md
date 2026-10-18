\# CI/CD Automation Using AWS CodePipeline



\## 1. Project Overview



This project demonstrates Continuous Integration and Continuous Deployment (CI/CD) using GitHub, AWS CodePipeline, and Amazon S3.



Whenever the source code is updated in the GitHub repository, AWS CodePipeline can retrieve the latest version and deploy the website files to the configured Amazon S3 bucket.



\## 2. Project Objectives



\- Automate website deployment from GitHub to Amazon S3.

\- Understand CI/CD pipeline concepts.

\- Configure AWS CodePipeline with a GitHub source.

\- Deploy website files to S3.

\- Monitor pipeline executions and troubleshoot errors.



\## 3. AWS Services Used



| Service | Purpose |

|---|---|

| GitHub | Stores the project source code |

| AWS CodePipeline | Automates the deployment workflow |

| Amazon S3 | Stores the deployed website files |

| AWS Lambda | Created and tested separately for automation |

| AWS IAM | Controls permissions between AWS services |

| Amazon CloudWatch | Provides logs for troubleshooting |



\## 4. Architecture Diagram



```mermaid

flowchart TD

&#x20;   A\[GitHub Repository] -->|Source changes| B\[AWS CodePipeline]

&#x20;   B -->|Deploy website files| C\[Amazon S3]

&#x20;   D\[AWS Lambda] -.->|Tested separately| E\[CloudWatch Logs]

```



\*\*Note:\*\* The active pipeline currently uses GitHub → AWS CodePipeline → Amazon S3. Lambda was tested separately and is not currently an action in the pipeline.



\## 5. Project Configuration



\- \*\*AWS Region:\*\* Asia Pacific (Mumbai) — `ap-south-1`

\- \*\*Pipeline Name:\*\* `CICDDeploymentPipeline`

\- \*\*S3 Bucket:\*\* `shital-cicd-deployment-2026-unique`

\- \*\*Lambda Function:\*\* `CICDDeploymentAutomation`

\- \*\*GitHub Repository:\*\* \[CI-CD-Lambda-Project](https://github.com/Shital-7841/CI-CD-Lambda-Project)



\## 6. Implementation Steps



1\. Created a GitHub repository for the project.

2\. Added the website source file under the `app` folder.

3\. Created an Amazon S3 bucket for deployment.

4\. Connected GitHub to AWS CodePipeline using the GitHub App connection.

5\. Configured the Source stage to retrieve files from the `main` branch.

6\. Configured the Amazon S3 Deploy action.

7\. Configured IAM permissions required for the pipeline.

8\. Released a pipeline change and verified that Source and Deploy succeeded.

9\. Created and tested the Lambda function separately.



\## 7. Screenshots



Save your screenshots in the `screenshots/` folder using these filenames:



\### GitHub Repository

!\[GitHub repository](screenshots/01-github-repository.png)



\### Successful CodePipeline Execution

!\[CodePipeline success](screenshots/02-codepipeline-success.png)



\### Deployed Files in Amazon S3

!\[S3 deployed files](screenshots/03-s3-deployed-files.png)



\### Lambda Test Result

!\[Lambda test success](screenshots/04-lambda-test-success.png)



> Add each screenshot to the `screenshots` folder before uploading this README. If a screenshot has not been captured yet, capture it and save it with the matching

