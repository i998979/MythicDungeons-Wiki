# Parameters

## Under `Ruins.Stages.<ID>.Branches`:

{% hint style="warning" %}
**Warning:** Please make sure that all branches will reach a stage with option `End` to make sure that there is no infinite loop.
{% endhint %}

### Branch

| Parameters | Explanation                                                                                                  | Examples       | Required |
| ---------- | ------------------------------------------------------------------------------------------------------------ | -------------- | -------- |
| **Branch** | List of branches                                                                                             | `Branch{id=2}` |          |
| id         | ID of the stage that will do when the current stage ends, it has to be a valid stage ID under `Ruins.Stages` |                | true     |
