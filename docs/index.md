# Incident Response Playbooks

This site contains a number of playbooks to assist analysts with maintaining a consistent approach when responding to incidents.

```kql linenums="1"
// Number of errors by URI
AzureDiagnostics
| where ResourceType == "APPLICATIONGATEWAYS" and OperationName == "ApplicationGatewayAccess" and httpStatus_d > 399
| summarize AggregatedValue = count() by requestUri_s, _ResourceId
| sort by AggregatedValue desc
```