# how to write better react code

<https://x.com/aidenybai/status/1925242687013494945>

```markdown
react patterns moving forward:

* UIs are a *thin* wrapper over data, you should avoid using local state (like usestate unless you have to, and it's independent of the business logic
* even then, consider if you can flatten the ui state into a basic calculation. useState is only necessary if it's truly reactive
* *choose state machines over multiple useStates, makes the code harder to reason about
* *choose to create a new component abstraction when you're nesting conditional logic, or top level if/else statements. ternaries are reserved for small, easily readable logic
* *avoid putting dependent logic in useEffects, it causes misdirection of what the logic is going. choose to explicitly define logic rather than depend on implicit reactive behavior
* *setTimeouts are flaky and usually a *hack*. provide a comment on *why*

this doesn't affect if the "code runs" or not, most of the time, but you can introduce subtle bugs that pile up into big issues that aren't obvious until someone goes in and has to spend a lot of time refactoring everything (edited)
```
