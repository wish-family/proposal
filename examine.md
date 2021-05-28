# Rules for Examining Proposals

## How To make my own decison
All members other than the proposer can participate in the decision by commenting directly under the PR of the proposal. The decision that each approver can make are listed below:

- **I want to participate**. This means that the approver is very interested in the project and will take the time to get involved.
- **Agree**. This means that the approver thinks the project is worth the time, but will not necessarily participate in it immediately.
- **Neutral**. When a member does not comment on this PR, it is automatically classified as such.
- **Reject**. This means that the approver does not think the project is worth doing or is not interested in the project at all.

It is strongly recommended that approvers provide reasons for their decisions, but this is not required.

## How To make the final decision
Each approver's decision has a corresponding score, which is listed in the table below:

| Decision             | Score |
|----------------------|-------|
|I want to participate | 2     |
|Agree                 | 1     |
|Neutral               | 0     |
|Reject                | -1    |

We will use `score(x)` to denote the score corresponding to the decision of approver `x`.

The current score `S` of the proposal will be calculated by the following formula, where `N` is the total number of members and the approvers are `a_1`, `a_2`, ..., `a_m`, and `floor` is the downward rounding function.

```
S = score(a_1) + score(a_2) + ... + score(a_m) - floor(N/2)
```

When `S > 0`, the current proposal will be merged into the repository and a repository named after the item in it will be created.
