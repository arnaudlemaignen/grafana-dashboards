# Grafana dashboards
This repository showcases custom Grafana dashboards for monitoring and visualizing key metrics in various areas.

Those are also published on [grafana.com](https://grafana.com/dashboards)

## Prometheus datasource

Set of Prometheus Grafana dashboards published on
[grafana.com](https://grafana.com/dashboards?dataSource=prometheus)

## AWS CloudWatch datasource

Set of AWS Grafana dashboards published on
[grafana.com](https://grafana.com/dashboards?dataSource=cloudwatch)

Here is an example of IAM role for Grafana to use those dashboards:

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AllowReadingMetricsFromCloudWatch",
            "Effect": "Allow",
            "Action": [
                "cloudwatch:DescribeAlarmsForMetric",
                "cloudwatch:DescribeAlarmHistory",
                "cloudwatch:DescribeAlarms",
                "cloudwatch:ListMetrics",
                "cloudwatch:GetMetricData",
                "cloudwatch:GetInsightRuleReport"
            ],
            "Resource": "*"
        },
        {
            "Sid": "AllowReadingLogsFromCloudWatch",
            "Effect": "Allow",
            "Action": [
                "logs:DescribeLogGroups",
                "logs:GetLogGroupFields",
                "logs:StartQuery",
                "logs:StopQuery",
                "logs:GetQueryResults",
                "logs:GetLogEvents"
            ],
            "Resource": "*"
        },
        {
            "Sid": "AllowReadingTagsInstancesRegionsFromEC2",
            "Effect": "Allow",
            "Action": [
                "ec2:DescribeTags",
                "ec2:DescribeInstances",
                "ec2:DescribeRegions"
            ],
            "Resource": "*"
        },
        {
            "Sid": "AllowReadingResourcesForTags",
            "Effect": "Allow",
            "Action": "tag:GetResources",
            "Resource": "*"
        }
    ]
}
```


### [AWS AirFlow](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-airflow)
[![AWS AirFlow](cloudwatch-ds/aws-airflow/aws-airflow-mwaa-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-airflow)

### [AWS Athena Performances](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-athena-performances)
[![AWS Athena Performances](cloudwatch-ds/aws-athena-performances/aws-athena-performances-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-athena-performances)

### [AWS Bedrock Foundation Models](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-bedrock-foundation-models)
[![AWS Bedrock Foundation Models](cloudwatch-ds/aws-bedrock-foundation-models/aws-bedrock-foundation-models.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-bedrock-foundation-models)

### [AWS Bedrock GuardRails](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-bedrock-guardrails)
[![AWS Bedrock GuardRails](cloudwatch-ds/aws-bedrock-guardrails/aws-bedrock-guardrails.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-bedrock-guardrails)

### [AWS Elasticache Redis](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-elasticache-redis)
[![AWS Elasticache Redis](cloudwatch-ds/aws-elasticache-redis/aws-elasticache-redis-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-elasticache-redis)

### [AWS FSx](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-fsx)
[![AWS FSx](cloudwatch-ds/aws-fsx/aws-fsx-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-fsx)

### [AWS Glue](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-glue)
[![AWS Glue](cloudwatch-ds/aws-glue/aws-glue-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-glue)

### [AWS MSK](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-msk)
[![AWS MSK](cloudwatch-ds/aws-msk/aws-msk-1.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-msk)


### [AWS S3](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-s3)
[![AWS S3](cloudwatch-ds/aws-s3/aws-s3.png)](https://github.com/arnaudlemaignen/grafana-dashboards/tree/master/cloudwatch-ds/aws-s3)


## Contributions
Pull requests, comments and suggestions are welcome.