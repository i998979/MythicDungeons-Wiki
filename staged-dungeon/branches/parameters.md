# Parameters

{% hint style="warning" %}
**Warning:** Please make sure that all branches will reach a stage with option `End` to make sure that there is no infinite loop.
{% endhint %}

## Under `Stages.<ID>.Branches`:

### Branch

| Parameters  | Explanation                                                                                             | Examples                                | Required                     |
| ----------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------- | ---------------------------- |
| **Branch**  | List of branches                                                                                        | `Branch{id=2;gruop=GroupA";weight=0.5}` |                              |
| id          | ID of the stage that will do when the current stage ends, it has to be a valid stage ID in `stages.yml` |                                         | true                         |
| independent | Is this branch independent. Weight will be calculated independently. Default is `true`                  |                                         |                              |
| group       | Group of the branch, only 1 branch in the same group will be executed depending on weight               |                                         |                              |
| weight      | Weight of the branch. Default is `1.0`                                                                  |                                         | true of `group` is specified |
