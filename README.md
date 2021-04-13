
[![DevopPro3 Udacity](https://github.com/melch-inno/DevopPro3/actions/workflows/main.yml/badge.svg)](https://github.com/melch-inno/DevopPro3/actions/workflows/main.yml)


# Overview
 Final project Ensuring Quality Releases.


# Project Structure 
- **.devops/pipelines**: azure pipelines yaml
- **automatedtesting**: suites of different tests
  - **jmeter**: load test (JMeterPlan.jmx), CSV inputs, and TestReports (endurance-report, stress-report)
  - **postman**: functional tests postman collections and environments
  - **selenium**: ui tests (uitests.py)
- **fakerestapi**: api files to deplopy webapp
- **screenshoots**: all screen shots requests
- **terraform**: terraform scripts

---

# Screenshoots Log

## Environment Creation & Deployment

- Create a Service Principal for Terraform named `TerraformSP` by: `az ad sp create-for-rbac --role="Contributor" --name="TerraformSP"`, and such command outputs 5 values: `appId`, `displayName`, `name`, `password`, and `tenant`.

  - screenshot of the log results of Terraform executed by the CI/CD pipeline
   ![1-terraform-output](screenshots/terraform-output.png)
   ![1-terraform-state](screenshots/terraform-state.png)

## Automated Testing

- screenshot of the log output of JMeter Command Line Options reference with results executed by the CI/CD pipeline
    ![3-load-test](screenshots/3-load-test-part1.png)
    ![3-load-test](screenshots/3-load-test-part2.png)
  
- Functional test suites 
  - screenshot of the execution of the test suite by the CI/CD pipeline
   ![4-functional-test](screenshots/4-functional-test.png)

- API-integration tests
  - screenshot of the Run Summary page (which contains 4 graphs)
    ![5-summary-page-part1](screenshots/5-summary-page-part1.png)
  - screenshot of the Test Results page (which contains the test case titles from each test) 
    ![5-test-result-page-part2](screenshots/5-test-result-page-part2.png)
  - screenshot of the output of the Publish Test Results step
    ![5-publish-tests-output-part3](screenshots/5-publish-tests-output-part3.png)

## Monitoring & Observability

- Configure Azure Monitor
  - screenshots of the email received when the alert is triggered
    ![6-emails-part1](screenshots/6-emails-part1.png)
  - screenshots of the graphs of the resource that the alert was triggered
    ![6-webapp-part2](screenshots/6-webapp-part2.png)
  - screenshots of the alert rule
    ![6-alerts-part3c](screenshots/6-alerts-part3c.png)

- Azure Log Analytics
  - screenshots of log analytics queries and result sets which will show specific output of the Azure resource
    ![7-log-analytics](screenshots/7-log-analytics.png)
