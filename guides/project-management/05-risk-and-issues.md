# Risk and issues

Name what could go wrong before it does, and give every problem an owner and a next action.

## Risk versus issue

- A **risk** might happen. It has a probability and an impact.
- An **issue** has happened. It is affecting the work now.

Both need an owner. A risk without an owner is a worry. An issue without a next action is a complaint.

## Keep a short register

A risk register is a small table, not a database. Five to ten active risks is enough for most projects.

| Risk | Probability | Impact | Response | Owner | Trigger |
| --- | --- | --- | --- | --- | --- |
| Vendor misses pilot date | Medium | High | Line up a second vendor | Ana | No confirmation by Friday |
| Legal review takes longer | High | Medium | Start review early | Ben | Contract draft sent |

Review the register in the weekly review. Remove risks that are no longer real. Add new ones without ceremony.

## Choose a response

Four responses cover most cases:

- **Avoid** — change the plan so the risk cannot happen.
- **Reduce** — lower the probability or the impact.
- **Transfer** — move the consequence to someone else, such as a vendor or insurer.
- **Accept** — decide the risk is tolerable and watch it.

Acceptance is a valid choice when it is deliberate and written down. It is not valid when nobody noticed the risk.

## Define a trigger

A trigger is the observable sign that a risk is becoming an issue. It turns watching into a decision.

- "If the vendor has not confirmed by Friday, we start the backup option."
- "If the pilot exceeds two weeks, we cut the optional report."

Without a trigger, the team debates the risk every week and decides nothing.

## Handle issues visibly

When a risk becomes an issue, record it where work lives:

```markdown
**Issue:** Vendor has not confirmed the pilot date.
**Owner:** Ana
**Impact:** The pilot slips one week; the launch date is at risk.
**Next action:** Call the vendor Monday and confirm or switch.
```

In dotpm, set the task to **Blocked** and put this in the description. In TaskNotes, use a `waiting` context or the `blockedBy` field. Do not leave the issue in a chat thread where it will be forgotten.

## Try it

Write five risks for your project.

1. Add probability, impact, and a response for each.
2. Name an owner for each.
3. Write one trigger that turns a risk into a decision.
4. Turn one existing problem into a visible issue with a next action.

Put the register in the project description in `local-project/pm-vault/`, and the issue on the affected task.

Next: [Communication](06-communication.md)
