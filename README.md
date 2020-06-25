# Honeycode AppFlow Integration

Add Honeycode as a destination from AppFlow.

![Honeycode Screenshot](assets/screen1.png)

> :exclamation: Only Google Analytics is currently mapped as a valid source

## Installation

> Currently, the only possible region is `us-west-2`.

First, create your Honeycode account and create an ADMIN user and record credentials (email address / password).

[![Launch Stack](https://cdn.rawgit.com/buildkite/cloudformation-launch-stack-button-svg/master/launch-stack.svg)](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/quickcreate?templateUrl=https%3A%2F%2Fs3.amazonaws.com%2Fianmckay-us-west-2%2Fhoneycode-appflow%2Ftemplate.yml&stackName=honeycode-appflow)

Click the above link to deploy the stack to your environment.

If you prefer, you can also manually upsert the [template.yml](https://github.com/iann0036/honeycode-appflow-integration/blob/master/template.yml) stack from source.

You will need to provide the Workbook ID and Sheet ID which can be found in the URL bar, or via the [modal](https://docs.aws.amazon.com/honeycode/latest/UserGuide/arns-and-ids.html).

![AppFlow Screenshot](assets/screen2.png)

Once launched, the CloudFormation stack will output the name of an S3 bucket it has created. You can now create an AppFlow flow that points from a Google Analytics source, with direct mappings, to this destination bucket and the Honeycode table will be populated each time the flow is run.
