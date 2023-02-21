# Week 0 — Billing and Architecture
This week the team will be discussing the billing architecture security.

The pricing of aws services is vary depending on the region. Make sure to use the region close to you and see if all services you will utilise are available for the region. And also make sure you set the billing alarm so you don't have unexpected costs.

## Info about billing alerts, Budgets

Billing metric data is stored in the US East (N. Virginia) Region and represents worldwide charges. This data includes the estimated charges for every service in AWS that you use, in addition to the estimated overall total of your AWS charges.
The alarm triggers when your account billing exceeds the threshold you specify. It triggers only when the current billing exceeds the threshold. It doesn't use projections based on your usage so far in the month.
If you create a billing alarm at a time when your charges have already exceeded the threshold, the alarm goes to the ALARM state immediately.

### Budgets
AWS Budgets Improve planning and cost control with flexible budgeting and forecasting. We created budgets for monthly charges and set thresholds for alarms accordingly when the threshold exceeds or when a forecast also exceed the budget we will be notified on respective email id.


tasks:
  - name: aws-cli
    env:
      AWS_CLI_AUTO_PROMPT: on-partial
    init: |
      cd /workspace
      curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
      unzip awscliv2.zip
      sudo ./aws/install
      cd $THEIA_WORKSPACE_ROOT
vscode:
  extensions:
    - 42Crunch.vscode-openapi
