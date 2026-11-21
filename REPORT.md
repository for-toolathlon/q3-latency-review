# Q3 Latency Review

## Q3 P95 Latency Results

Prepared for the quarterly infra review.

| Service  | Budget (ms) | Actual (ms) | Utilization | Status   |
|----------|-------------|-------------|-------------|----------|
| api-gateway | 250        | 262         | 104.8%      | breach   |
| search-svc  | 400        | 356         | 89.0%       | ok       |
| auth-svc    | 150        | 143         | 95.3%       | at-risk  |
| billing-svc | 300        | 371         | 123.7%      | breach   |
| notify-svc  | 200        | 175         | 87.5%       | ok       |

## Callouts

- **Breaches:** api-gateway (104.8%) and billing-svc (123.7%) exceeded their budgets. api-gateway is 6.8 ms over its 250 ms budget; billing-svc is 71 ms over its 300 ms budget.
- **At-Risk:** auth-svc is at 95.3% of its 150 ms budget, just under the 100% threshold.
- **Ok:** search-svc and notify-svc are well within their budgets.

## MongoDB Support Lifecycle Note

For a quarterly MongoDB upgrade planning, the official MongoDB support lifecycle/policy page was consulted. Per MongoDB's vendor support policies (via https://www.mongodb.com/support/policies, "MongoDB Support Policies" page), software major releases are supported for a defined lifecycle duration, and that duration differs across major versions. However, the page itself does not provide the specific length of support for a major release nor the list of major versions already past end of life. The prompt did not return usable content from the public lookup, so these specific lifecycle figures could not be verified from the vendor page and are therefore not quoted here.
