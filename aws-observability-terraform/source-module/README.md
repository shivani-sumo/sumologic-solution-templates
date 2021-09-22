## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 0.13.0 |
| <a name="requirement_aws"></a> [aws](#requirement\_aws) | >= 3.42.0 |
| <a name="requirement_random"></a> [random](#requirement\_random) | >= 3.1.0 |
| <a name="requirement_sumologic"></a> [sumologic](#requirement\_sumologic) | >= 2.9.0 |
| <a name="requirement_time"></a> [time](#requirement\_time) | >= 0.7.1 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | 3.57.0 |
| <a name="provider_null"></a> [null](#provider\_null) | 3.1.0 |
| <a name="provider_random"></a> [random](#provider\_random) | 3.1.0 |
| <a name="provider_sumologic"></a> [sumologic](#provider\_sumologic) | 2.9.10 |
| <a name="provider_time"></a> [time](#provider\_time) | 0.7.2 |

## Modules

| Name | Source | Version |
|------|--------|---------|
| <a name="module_cloudtrail_module"></a> [cloudtrail\_module](#module\_cloudtrail\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/cloudtrail | n/a |
| <a name="module_cloudwatch_logs_lambda_log_forwarder_module"></a> [cloudwatch\_logs\_lambda\_log\_forwarder\_module](#module\_cloudwatch\_logs\_lambda\_log\_forwarder\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/cloudwatchlogsforwarder | n/a |
| <a name="module_cloudwatch_metrics_source_module"></a> [cloudwatch\_metrics\_source\_module](#module\_cloudwatch\_metrics\_source\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/cloudwatchmetrics | n/a |
| <a name="module_elb_module"></a> [elb\_module](#module\_elb\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/elb | n/a |
| <a name="module_kinesis_firehose_for_logs_module"></a> [kinesis\_firehose\_for\_logs\_module](#module\_kinesis\_firehose\_for\_logs\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/kinesisfirehoseforlogs | n/a |
| <a name="module_kinesis_firehose_for_metrics_source_module"></a> [kinesis\_firehose\_for\_metrics\_source\_module](#module\_kinesis\_firehose\_for\_metrics\_source\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/kinesisfirehoseformetrics | n/a |
| <a name="module_root_cause_sources_module"></a> [root\_cause\_sources\_module](#module\_root\_cause\_sources\_module) | SumoLogic/sumo-logic-integrations/sumologic//aws/rootcause | n/a |

## Resources

| Name | Type |
|------|------|
| [aws_iam_policy.cloudtrail_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_policy.cw_metrics_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_policy.elb_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_policy.root_cause_policy](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_policy) | resource |
| [aws_iam_role.sumologic_iam_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.cloudtrail_policy_attach](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_iam_role_policy_attachment.cw_metrics_policy_attach](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_iam_role_policy_attachment.elb_policy_attach](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_iam_role_policy_attachment.root_cause_policy_attach](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [aws_s3_bucket.s3_bucket](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket) | resource |
| [aws_s3_bucket_notification.bucket_notification](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket_notification) | resource |
| [aws_sns_topic.sns_topic](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/sns_topic) | resource |
| [null_resource.AddFieldsToCloudTrailSource](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [null_resource.AddFieldsToELBSource](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [null_resource.AddFieldsToLogSource](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [null_resource.AddFieldsToMetricSource](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [random_string.aws_random](https://registry.terraform.io/providers/hashicorp/random/latest/docs/resources/string) | resource |
| [sumologic_collector.collector](https://registry.terraform.io/providers/SumoLogic/sumologic/latest/docs/resources/collector) | resource |
| [time_sleep.wait_for_minutes](https://registry.terraform.io/providers/hashicorp/time/latest/docs/resources/sleep) | resource |
| [aws_caller_identity.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/caller_identity) | data source |
| [aws_region.current](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/region) | data source |
| [sumologic_caller_identity.current](https://registry.terraform.io/providers/SumoLogic/sumologic/latest/docs/data-sources/caller_identity) | data source |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_access_id"></a> [access\_id](#input\_access\_id) | Sumo Logic Access ID. Visit https://help.sumologic.com/Manage/Security/Access-Keys#Create_an_access_key | `string` | n/a | yes |
| <a name="input_access_key"></a> [access\_key](#input\_access\_key) | Sumo Logic Access Key. Visit https://help.sumologic.com/Manage/Security/Access-Keys#Create_an_access_key | `string` | n/a | yes |
| <a name="input_auto_enable_access_logs"></a> [auto\_enable\_access\_logs](#input\_auto\_enable\_access\_logs) | Enable Application Load Balancer (ALB) Access logging.<br>            You have the following options:<br>            New - Automatically enables access logging for newly created ALB resources to collect logs for ALB resources. This does not affect ALB resources already collecting logs.<br>            Existing - Automatically enables access logging for existing ALB resources to collect logs for ALB resources.<br>            Both - Automatically enables access logging for new and existing ALB resources.<br>            None - Skips Automatic access Logging enable for ALB resources. | `string` | `"Both"` | no |
| <a name="input_auto_enable_logs_subscription"></a> [auto\_enable\_logs\_subscription](#input\_auto\_enable\_logs\_subscription) | Subscribe log groups to Sumo Logic Lambda Forwarder.<br>            You have the following options:<br>            New - Automatically subscribes new log groups to send logs to Sumo Logic.<br>            Existing - Automatically subscribes existing log groups to send logs to Sumo Logic.<br>            Both - Automatically subscribes new and existing log groups.<br>            None - Skips Automatic subscription. | `string` | `"Both"` | no |
| <a name="input_auto_enable_logs_subscription_options"></a> [auto\_enable\_logs\_subscription\_options](#input\_auto\_enable\_logs\_subscription\_options) | filter - Enter regex for matching logGroups. Regex will check for the name. Visit https://help.sumologic.com/03Send-Data/Collect-from-Other-Data-Sources/Auto-Subscribe_AWS_Log_Groups_to_a_Lambda_Function#Configuring_parameters | <pre>object({<br>    filter = string<br>  })</pre> | <pre>{<br>  "filter": "lambda"<br>}</pre> | no |
| <a name="input_aws_account_alias"></a> [aws\_account\_alias](#input\_aws\_account\_alias) | Provide the Name/Alias for the AWS environment from which you are collecting data. This name will appear in the Sumo Logic Explorer View, metrics, and logs.<br>            Please leave this blank if you are going to deploy the solution in multiple AWS accounts.<br>            Do not include special characters in the alias. | `string` | n/a | yes |
| <a name="input_cloudtrail_source_details"></a> [cloudtrail\_source\_details](#input\_cloudtrail\_source\_details) | Provide details for the Sumo Logic CloudTrail source. If not provided, then defaults will be used.<br>            To enable, set collect\_cloudtrail\_logs to true and provide configuration information for the bucket at bucket\_details.<br>            If create\_bucket is false, provide a name of an existing S3 bucket where you would like to store CloudTrail logs. If this is empty, a new bucket will be created in the region.<br>            If create\_bucket is true, the script creates a bucket, the name of the bucket has to be unique; this is achieved internally by generating a random-id and then post-fixing it to the “aws-observability-” string.<br>            path\_expression - This is required in case the above existing bucket is already configured to receive CloudTrail logs. If this is blank, Sumo Logic will store logs in the path expression AWSLogs/*/CloudTrail/*/*. | <pre>object({<br>    source_name     = string<br>    source_category = string<br>    description     = string<br>    bucket_details = object({<br>      create_bucket        = bool<br>      bucket_name          = string<br>      path_expression      = string<br>      force_destroy_bucket = bool<br>    })<br>    fields = map(string)<br>  })</pre> | <pre>{<br>  "bucket_details": {<br>    "bucket_name": "aws-observability-random-id",<br>    "create_bucket": true,<br>    "force_destroy_bucket": true,<br>    "path_expression": "AWSLogs/<ACCOUNT-ID>/CloudTrail/<REGION-NAME>/*"<br>  },<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS cloudtrail logs.",<br>  "fields": {},<br>  "source_category": "aws/observability/cloudtrail/logs",<br>  "source_name": "CloudTrail Logs (Region)"<br>}</pre> | no |
| <a name="input_cloudtrail_source_url"></a> [cloudtrail\_source\_url](#input\_cloudtrail\_source\_url) | Required if you are already collecting CloudTrail logs. Provide the existing Sumo Logic CloudTrail Source API URL. The account field will be added to the Source. For information on how to determine the URL, see [View or Download Source JSON Configuration](https://help.sumologic.com/03Send-Data/Sources/03Use-JSON-to-Configure-Sources/Local-Configuration-File-Management/View-or-Download-Source-JSON-Configuration). | `string` | `""` | no |
| <a name="input_cloudwatch_logs_source_details"></a> [cloudwatch\_logs\_source\_details](#input\_cloudwatch\_logs\_source\_details) | Provide details for the Sumo Logic Cloudwatch Logs source. If not provided, then defaults will be used.<br><br>            Use bucket\_details section with Kinesis Firehose Log Source:<br>            If create\_bucket is false, provide a name of an existing S3 bucket where you would like to store cloudwatch logs. If this is empty, a new bucket will be created.<br>            If create\_bucket is true, the script creates a bucket, the name of the bucket has to be unique; this is achieved internally by generating a random-id and then post-fixing it to the “aws-observability-” string.<br><br>            Use lambda\_log\_forwarder\_config section with Lambda Log Forwarder:<br>            Provide your email\_id to receive alerts. You will receive a confirmation email after the deployment is complete. Follow the instructions in this email to validate the address.<br>            IncludeLogGroupInfo:  Set to true to include loggroup/logstream values in logs. For AWS Lambda logs, IncludeLogGroupInfo must be set to true<br>            logformat: For Lambda, the value should be set to “Others”.<br>            log\_stream\_prefix: Enter a comma-separated list of logStream name prefixes to filter by logStream. Please note this is separate from a logGroup. This is used to only send certain logStreams within a CloudWatch logGroup(s). LogGroup(s) still need to be subscribed to the created Lambda function.<br>            workers: Number of lambda function invocations for Cloudwatch logs source Dead Letter Queue processing. | <pre>object({<br>    source_name     = string<br>    source_category = string<br>    description     = string<br>    fields          = map(string)<br>    bucket_details = object({<br>      create_bucket        = bool<br>      bucket_name          = string<br>      force_destroy_bucket = bool<br>    })<br>    lambda_log_forwarder_config = object({<br>      email_id               = string<br>      workers                = number<br>      log_format             = string<br>      include_log_group_info = bool<br>      log_stream_prefix      = list(string)<br>    })<br>  })</pre> | <pre>{<br>  "bucket_details": {<br>    "bucket_name": "aws-observability-random-id",<br>    "create_bucket": true,<br>    "force_destroy_bucket": true<br>  },<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS Cloudwatch Logs.",<br>  "fields": {},<br>  "lambda_log_forwarder_config": {<br>    "email_id": "test@gmail.com",<br>    "include_log_group_info": true,<br>    "log_format": "Others",<br>    "log_stream_prefix": [],<br>    "workers": 4<br>  },<br>  "source_category": "aws/observability/cloudwatch/logs",<br>  "source_name": "CloudWatch Logs (Region)"<br>}</pre> | no |
| <a name="input_cloudwatch_logs_source_url"></a> [cloudwatch\_logs\_source\_url](#input\_cloudwatch\_logs\_source\_url) | Required if you are already collecting AWS Lambda CloudWatch logs. Provide the existing Sumo Logic AWS Lambda CloudWatch Source API URL. The account, accountid, region and namespace fields will be added to the Source. For information on how to determine the URL, see [View or Download Source JSON Configuration](https://help.sumologic.com/03Send-Data/Sources/03Use-JSON-to-Configure-Sources/Local-Configuration-File-Management/View-or-Download-Source-JSON-Configuration). | `string` | `""` | no |
| <a name="input_cloudwatch_metrics_source_details"></a> [cloudwatch\_metrics\_source\_details](#input\_cloudwatch\_metrics\_source\_details) | Provide details for the Sumo Logic Cloudwatch Metrics source. If not provided, then defaults will be used.<br>            limit\_to\_namespaces - Enter a comma-delimited list of the namespaces which will be used for both AWS CloudWatch Metrics Source.<br>            See this list of AWS services that publish CloudWatch metrics: https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/aws-services-cloudwatch-metrics.html | <pre>object({<br>    source_name         = string<br>    source_category     = string<br>    description         = string<br>    limit_to_namespaces = list(string)<br>    fields              = map(string)<br>    bucket_details = object({<br>      create_bucket        = bool<br>      bucket_name          = string<br>      force_destroy_bucket = bool<br>    })<br>  })</pre> | <pre>{<br>  "bucket_details": {<br>    "bucket_name": "aws-observability-random-id",<br>    "create_bucket": true,<br>    "force_destroy_bucket": true<br>  },<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS Cloudwatch metrics.",<br>  "fields": {},<br>  "limit_to_namespaces": [<br>    "AWS/ApplicationELB",<br>    "AWS/ApiGateway",<br>    "AWS/DynamoDB",<br>    "AWS/Lambda",<br>    "AWS/RDS",<br>    "AWS/ECS",<br>    "AWS/ElastiCache",<br>    "AWS/ELB",<br>    "AWS/NetworkELB",<br>    "AWS/SQS",<br>    "AWS/SNS"<br>  ],<br>  "source_category": "aws/observability/cloudwatch/metrics",<br>  "source_name": "CloudWatch Metrics (Region)"<br>}</pre> | no |
| <a name="input_cloudwatch_metrics_source_url"></a> [cloudwatch\_metrics\_source\_url](#input\_cloudwatch\_metrics\_source\_url) | Required if you are already collecting CloudWatch Metrics. Provide the existing Sumo Logic Metrics Source API URL. If the URL is of “CloudWatch Metric source” - account and accountID fields will be added to the Source.  If the URL is of “Kinesis Firehose Metrics source” - account field will be added to the Source. For information on how to determine the URL, see [View or Download Source JSON Configuration](https://help.sumologic.com/03Send-Data/Sources/03Use-JSON-to-Configure-Sources/Local-Configuration-File-Management/View-or-Download-Source-JSON-Configuration). | `string` | `""` | no |
| <a name="input_collect_cloudtrail_logs"></a> [collect\_cloudtrail\_logs](#input\_collect\_cloudtrail\_logs) | Create a Sumo Logic CloudTrail Logs Source.<br>            You have the following options:<br>			true - to ingest cloudtrail logs into Sumo Logic. Creates a Sumo Logic CloudTrail Log Source that collects CloudTrail logs from an existing bucket or new bucket.<br>			If true, please configure \"cloudtrail\_source\_details\" with configuration information to ingest cloudtrail logs.<br>			false - you are already ingesting cloudtrail logs into Sumo Logic. | `bool` | `true` | no |
| <a name="input_collect_cloudwatch_logs"></a> [collect\_cloudwatch\_logs](#input\_collect\_cloudwatch\_logs) | Select the kind of Sumo Logic CloudWatch Logs Sources to create<br>            You have the following options:<br>            "Lambda Log Forwarder" - Creates a Sumo Logic CloudWatch Log Source that collects CloudWatch logs via a Lambda function.<br>            "Kinesis Firehose Log Source" - Creates a Sumo Logic Kinesis Firehose Log Source to collect CloudWatch logs.<br>            "None" - Skips installation of both sources. | `string` | `"Kinesis Firehose Log Source"` | no |
| <a name="input_collect_cloudwatch_metrics"></a> [collect\_cloudwatch\_metrics](#input\_collect\_cloudwatch\_metrics) | Select the kind of CloudWatch Metrics Source to create<br>            You have the following options:<br>            "CloudWatch Metrics Source" - Creates Sumo Logic AWS CloudWatch Metrics Sources.<br>            "Kinesis Firehose Metrics Source" (Recommended) - Creates a Sumo Logic AWS Kinesis Firehose for Metrics Source. Note: This new source has cost and performance benefits over the CloudWatch Metrics Source and is therefore recommended.<br>            "None" - Skips the Installation of both the Sumo Logic Metric Sources | `string` | `"Kinesis Firehose Metrics Source"` | no |
| <a name="input_collect_elb_logs"></a> [collect\_elb\_logs](#input\_collect\_elb\_logs) | Create a Sumo Logic ALB Logs Source.<br>            You have the following options:<br>			true - to ingest load balancer logs into Sumo Logic. Creates a Sumo Logic Log Source that collects application load balancer logs from an existing bucket or a new bucket.<br>			If true, please configure \"elb\_source\_details\" with configuration information including the bucket name and path expression to ingest load balancer logs.<br>			false - you are already ingesting load balancer logs into Sumo Logic. | `bool` | `true` | no |
| <a name="input_collect_root_cause_data"></a> [collect\_root\_cause\_data](#input\_collect\_root\_cause\_data) | Select the Sumo Logic Root Cause Explorer Source.<br>            You have the following options:<br>            Inventory Source - Creates a Sumo Logic Inventory Source used by Root Cause Explorer.<br>            Xray Source - Creates a Sumo Logic AWS X-Ray Source that collects X-Ray Trace Metrics from your AWS account.<br>            Both - Install both Inventory and Xray sources.<br>            None - Skips installation of both sources. | `string` | `"Both"` | no |
| <a name="input_elb_log_source_url"></a> [elb\_log\_source\_url](#input\_elb\_log\_source\_url) | Required if you are already collecting ALB logs. Provide the existing Sumo Logic ALB Source API URL. The account, accountid, region and namespace fields will be added to the Source. For information on how to determine the URL, see [View or Download Source JSON Configuration](https://help.sumologic.com/03Send-Data/Sources/03Use-JSON-to-Configure-Sources/Local-Configuration-File-Management/View-or-Download-Source-JSON-Configuration). | `string` | `""` | no |
| <a name="input_elb_source_details"></a> [elb\_source\_details](#input\_elb\_source\_details) | Provide details for the Sumo Logic ALB source. If not provided, then defaults will be used.<br>            To enable collection of application load balancer logs, set collect\_elb\_logs to true and provide configuration information for the bucket.<br>            If create\_bucket is false, provide a name of an existing S3 bucket where you would like to store loadbalancer logs. If this is empty, a new bucket will be created in the region.<br>            If create\_bucket is true, the script creates a bucket, the name of the bucket has to be unique; this is achieved internally by generating a random-id and then post-fixing it to the “aws-observability-” string.<br>            path\_expression - This is required in case the above existing bucket is already configured to receive ALB access logs. If this is blank, Sumo Logic will store logs in the path expression: *AWSLogs/*/elasticloadbalancing/*/* | <pre>object({<br>    source_name     = string<br>    source_category = string<br>    description     = string<br>    bucket_details = object({<br>      create_bucket        = bool<br>      bucket_name          = string<br>      path_expression      = string<br>      force_destroy_bucket = bool<br>    })<br>    fields = map(string)<br>  })</pre> | <pre>{<br>  "bucket_details": {<br>    "bucket_name": "aws-observability-random-id",<br>    "create_bucket": true,<br>    "force_destroy_bucket": true,<br>    "path_expression": "*AWSLogs/<ACCOUNT-ID>/elasticloadbalancing/<REGION-NAME>/*"<br>  },<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS Application LoadBalancer logs.",<br>  "fields": {},<br>  "source_category": "aws/observability/alb/logs",<br>  "source_name": "Elb Logs (Region)"<br>}</pre> | no |
| <a name="input_environment"></a> [environment](#input\_environment) | Enter au, ca, de, eu, jp, us2, in, fed or us1. For more information on Sumo Logic deployments visit https://help.sumologic.com/APIs/General-API-Information/Sumo-Logic-Endpoints-and-Firewall-Security | `string` | n/a | yes |
| <a name="input_existing_iam_details"></a> [existing\_iam\_details](#input\_existing\_iam\_details) | Provide an existing AWS IAM role arn value which provides access to AWS S3 Buckets, AWS CloudWatch Metrics API and Sumo Logic Inventory data.<br>			If kept empty, a new IAM role will be created with the required permissions.<br>			For more details on permissions, check the iam policy tmpl files at /source-module/templates folder. | <pre>object({<br>    create_iam_role = bool<br>    iam_role_arn    = string<br>  })</pre> | <pre>{<br>  "create_iam_role": true,<br>  "iam_role_arn": ""<br>}</pre> | no |
| <a name="input_inventory_source_details"></a> [inventory\_source\_details](#input\_inventory\_source\_details) | Provide details for the Sumo Logic AWS Inventory source. If not provided, then defaults will be used. | <pre>object({<br>    source_name         = string<br>    source_category     = string<br>    description         = string<br>    limit_to_namespaces = list(string)<br>    fields              = map(string)<br>  })</pre> | <pre>{<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS inventory metadata.",<br>  "fields": {},<br>  "limit_to_namespaces": [<br>    "AWS/ApplicationELB",<br>    "AWS/ApiGateway",<br>    "AWS/DynamoDB",<br>    "AWS/Lambda",<br>    "AWS/RDS",<br>    "AWS/ECS",<br>    "AWS/ElastiCache",<br>    "AWS/ELB",<br>    "AWS/NetworkELB",<br>    "AWS/SQS",<br>    "AWS/SNS",<br>    "AWS/AutoScaling"<br>  ],<br>  "source_category": "aws/observability/inventory",<br>  "source_name": "AWS Inventory (Region)"<br>}</pre> | no |
| <a name="input_sumologic_collector_details"></a> [sumologic\_collector\_details](#input\_sumologic\_collector\_details) | Provide details for the Sumo Logic collector. If not provided, then defaults will be used.<br>			The Collector will be created if any new source will be created and \"sumologic\_existing\_collector\_id\" is empty. | <pre>object({<br>    collector_name = string<br>    description    = string<br>    fields         = map(string)<br>  })</pre> | <pre>{<br>  "collector_name": "AWS Observability (AWS Account Alias) (Account ID)",<br>  "description": "This collector is created using Sumo Logic terraform AWS Observability module.",<br>  "fields": {}<br>}</pre> | no |
| <a name="input_sumologic_existing_collector_details"></a> [sumologic\_existing\_collector\_details](#input\_sumologic\_existing\_collector\_details) | Provide an existing Sumo Logic Collector ID. For more details, visit https://help.sumologic.com/03Send-Data/Sources/03Use-JSON-to-Configure-Sources/Local-Configuration-File-Management/View-or-Download-Source-JSON-Configuration<br>			If provided, all the provided sources will be created within the collector.<br>			If kept empty, a new Collector will be created and all provided sources will be created within that collector. | <pre>object({<br>    create_collector = bool<br>    collector_id     = string<br>  })</pre> | <pre>{<br>  "collector_id": "",<br>  "create_collector": true<br>}</pre> | no |
| <a name="input_sumologic_organization_id"></a> [sumologic\_organization\_id](#input\_sumologic\_organization\_id) | You can find your org on the Preferences page in the Sumo Logic UI. For more information, see the Preferences Page topic. Your org ID will be used to configure the IAM Role for Sumo Logic AWS Sources."<br>            For more details, visit https://help.sumologic.com/01Start-Here/05Customize-Your-Sumo-Logic-Experience/Preferences-Page | `string` | n/a | yes |
| <a name="input_wait_for_seconds"></a> [wait\_for\_seconds](#input\_wait\_for\_seconds) | wait\_for\_seconds is used to delay sumo logic source creation. The value is in seconds. This helps persisting the IAM role in the AWS system.<br>            Default value is 180 seconds.<br>            If the AWS IAM role is created outside the module, the value can be decreased to 1 second. | `number` | `180` | no |
| <a name="input_xray_source_details"></a> [xray\_source\_details](#input\_xray\_source\_details) | Provide details for the Sumo Logic AWS XRAY source. If not provided, then defaults will be used. | <pre>object({<br>    source_name     = string<br>    source_category = string<br>    description     = string<br>    fields          = map(string)<br>  })</pre> | <pre>{<br>  "description": "This source is created using Sumo Logic terraform AWS Observability module to collect AWS Xray metrics.",<br>  "fields": {},<br>  "source_category": "aws/observability/xray",<br>  "source_name": "AWS Xray (Region)"<br>}</pre> | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_aws_cloudtrail"></a> [aws\_cloudtrail](#output\_aws\_cloudtrail) | AWS Trail created to send CloudTrail logs to AWS S3 bucket. |
| <a name="output_aws_cloudwatch_metric_stream"></a> [aws\_cloudwatch\_metric\_stream](#output\_aws\_cloudwatch\_metric\_stream) | CloudWatch metrics stream to send metrics. |
| <a name="output_aws_iam_role"></a> [aws\_iam\_role](#output\_aws\_iam\_role) | Sumo Logic AWS IAM Role for trust relationship. |
| <a name="output_aws_kinesis_firehose_logs_delivery_stream"></a> [aws\_kinesis\_firehose\_logs\_delivery\_stream](#output\_aws\_kinesis\_firehose\_logs\_delivery\_stream) | AWS Kinesis firehose delivery stream to send logs to Sumo Logic. |
| <a name="output_aws_kinesis_firehose_metrics_delivery_stream"></a> [aws\_kinesis\_firehose\_metrics\_delivery\_stream](#output\_aws\_kinesis\_firehose\_metrics\_delivery\_stream) | AWS Kinesis firehose delivery stream to send metrics to Sumo Logic. |
| <a name="output_aws_s3_bucket"></a> [aws\_s3\_bucket](#output\_aws\_s3\_bucket) | Common S3 Bucket to store CloudTrail, ELB and Failed Kinesis data. |
| <a name="output_aws_sns_topic"></a> [aws\_sns\_topic](#output\_aws\_sns\_topic) | Common SNS topic attached to the S3 bucket. |
| <a name="output_cloudtrail_sns_subscription"></a> [cloudtrail\_sns\_subscription](#output\_cloudtrail\_sns\_subscription) | AWS SNS subscription to Sumo Logic AWS CloudTrail source. |
| <a name="output_cloudtrail_sns_topic"></a> [cloudtrail\_sns\_topic](#output\_cloudtrail\_sns\_topic) | SNS topic created to be attached to an existing cloudtrail bucket. |
| <a name="output_cloudtrail_source"></a> [cloudtrail\_source](#output\_cloudtrail\_source) | Sumo Logic AWS CloudTrail source. |
| <a name="output_cloudwatch_logs_auto_subscribe_stack"></a> [cloudwatch\_logs\_auto\_subscribe\_stack](#output\_cloudwatch\_logs\_auto\_subscribe\_stack) | AWS CloudFormation stack for Auto Enable logs subscription. |
| <a name="output_cloudwatch_logs_lambda_function"></a> [cloudwatch\_logs\_lambda\_function](#output\_cloudwatch\_logs\_lambda\_function) | AWS Lambda function to send logs to Sumo Logic. |
| <a name="output_cloudwatch_logs_source"></a> [cloudwatch\_logs\_source](#output\_cloudwatch\_logs\_source) | Sumo Logic HTTP source. |
| <a name="output_cloudwatch_metrics_source"></a> [cloudwatch\_metrics\_source](#output\_cloudwatch\_metrics\_source) | Sumo Logic AWS CloudWatch Metrics source. |
| <a name="output_elb_auto_enable_stack"></a> [elb\_auto\_enable\_stack](#output\_elb\_auto\_enable\_stack) | AWS CloudFormation stack for ALB Auto Enable access logs. |
| <a name="output_elb_sns_subscription"></a> [elb\_sns\_subscription](#output\_elb\_sns\_subscription) | AWS SNS subscription to Sumo Logic AWS ELB source. |
| <a name="output_elb_sns_topic"></a> [elb\_sns\_topic](#output\_elb\_sns\_topic) | SNS topic created to be attached to an existing elb logs bucket. |
| <a name="output_elb_source"></a> [elb\_source](#output\_elb\_source) | Sumo Logic AWS ELB source. |
| <a name="output_inventory_source"></a> [inventory\_source](#output\_inventory\_source) | Sumo Logic AWS Inventory source. |
| <a name="output_kinesis_firehose_for_logs_auto_subscribe_stack"></a> [kinesis\_firehose\_for\_logs\_auto\_subscribe\_stack](#output\_kinesis\_firehose\_for\_logs\_auto\_subscribe\_stack) | AWS CloudFormation stack for Auto Enable logs subscription. |
| <a name="output_kinesis_firehose_for_logs_source"></a> [kinesis\_firehose\_for\_logs\_source](#output\_kinesis\_firehose\_for\_logs\_source) | Sumo Logic Kinesis Firehose for Logs source. |
| <a name="output_kinesis_firehose_for_metrics_source"></a> [kinesis\_firehose\_for\_metrics\_source](#output\_kinesis\_firehose\_for\_metrics\_source) | Sumo Logic AWS Kinesis Firehose for Metrics source. |
| <a name="output_sumologic_collector"></a> [sumologic\_collector](#output\_sumologic\_collector) | Sumo Logic collector details. |
| <a name="output_xray_source"></a> [xray\_source](#output\_xray\_source) | Sumo Logic AWS Xray source. |