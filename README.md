$ Terraform module for AWS Cloudwatch 
## Examples

Check the [examples](/examples/) folder 
<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| terraform | >= 0.12.7, < 0.14 |
| aws | >= 2.68, < 4.0 |

## Providers

| Name | Version |
|------|---------|
| aws | >= 2.68, < 4.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| actions\_enabled | (Optional) Indicates whether or not actions should be executed during any changes to the alarm's state. Defaults to true. | `bool` | `true` | no |
| alarm\_actions | (Optional) The list of actions to execute when this alarm transitions into an ALARM state from any other state. Each action is specified as an Amazon Resource Name (ARN). | `list(string)` | `null` | no |
| alarm\_description | (Optional) The description for the alarm. | `string` | `null` | no |
| alarm\_name | (Required) The descriptive name for the alarm. This name must be unique within the user's AWS account. | `string` | n/a | yes |
| comparison\_operator | (Required) The arithmetic operation to use when comparing the specified Statistic and Threshold. The specified Statistic value is used as the first operand. Either of the following is supported: GreaterThanOrEqualToThreshold, GreaterThanThreshold, LessThanThreshold, LessThanOrEqualToThreshold. | `string` | n/a | yes |
| create\_metric\_alarm | (Optional) Whether to create the Cloudwatch metric alarm | `bool` | `true` | no |
| datapoints\_to\_alarm | (Optional) The number of datapoints that must be breaching to trigger the alarm. | `number` | `null` | no |
| dimensions | (Optional) The dimensions for the alarm's associated metric. | `any` | `null` | no |
| evaluate\_low\_sample\_count\_percentiles | (Optional) Used only for alarms based on percentiles. If you specify ignore, the alarm state will not change during periods with too few data points to be statistically significant. If you specify evaluate or omit this parameter, the alarm will always be evaluated and possibly change state no matter how many data points are available. The following values are supported: ignore, and evaluate. | `string` | `null` | no |
| evaluation\_periods | (Required) The number of periods over which data is compared to the specified threshold. | `number` | n/a | yes |
| extended\_statistic | (Optional) The percentile statistic for the metric associated with the alarm. Specify a value between p0.0 and p100. | `string` | `null` | no |
| insufficient\_data\_actions | (Optional) The list of actions to execute when this alarm transitions into an INSUFFICIENT\_DATA state from any other state. Each action is specified as an Amazon Resource Name (ARN). | `list(string)` | `[]` | no |
| metric\_name | (Optional) The name for the alarm's associated metric. See docs for supported metrics. | `string` | `null` | no |
| metric\_query | (Optional) Enables you to create an alarm based on a metric math expression. You may specify at most 20. | `any` | `[]` | no |
| namespace | (Optional) The namespace for the alarm's associated metric. See docs for the list of namespaces. See docs for supported metrics. | `string` | `null` | no |
| ok\_actions | (Optional) The list of actions to execute when this alarm transitions into an OK state from any other state. Each action is specified as an Amazon Resource Name (ARN). | `list(string)` | `[]` | no |
| period | (Optional) The period in seconds over which the specified statistic is applied. | `string` | `null` | no |
| statistic | (Optional) The statistic to apply to the alarm's associated metric. Either of the following is supported: SampleCount, Average, Sum, Minimum, Maximum | `string` | `null` | no |
| tags | (Optional) A mapping of tags to assign to all resources | `map(string)` | `{}` | no |
| threshold | (Required) The value against which the specified statistic is compared. | `number` | n/a | yes |
| treat\_missing\_data | (Optional) Sets how this alarm is to handle missing data points. The following values are supported: missing, ignore, breaching and notBreaching. | `string` | `"missing"` | no |
| unit | (Optional) The unit for the alarm's associated metric. | `string` | `null` | no |

## Outputs

| Name | Description |
|------|-------------|
| this\_cloudwatch\_metric\_alarm\_arn | The ARN of the Cloudwatch metric alarm. |
| this\_cloudwatch\_metric\_alarm\_id | The ID of the Cloudwatch metric alarm. |

<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## License

Apache 2 Licensed. See LICENSE for full details.
