# Work out how to assert a ContentResult

1. Nullable cast the return value of the action method to ContentResult

```
var result = controller.PartnerMasterModel(agentName) as ContentResult;
```

2. Assert on ContentResult.Content 

```
Assert.That(result.Content, Is.EqualTo("something"));
```