# Stages

Stages contain all `Actions` and `Completions` to do, `Objectives` to check in this phase, as well as different parameters.

## Under `Ruins.Stages.<ID>.Options`:

<table data-full-width="false"><thead><tr><th>Parameters</th><th>Explanation</th><th>Examples</th></tr></thead><tbody><tr><td>Initial</td><td>Define the first stage of the dungeon. Only 1 stage can be defined as initial</td><td><code>true</code> if this is the first stage of the dungeon, otherwise, it can be omitted</td></tr><tr><td>Delay</td><td>How long in ticks will the stage wait before starting, the actions will not be done, and the objectives will not be shown on the scoreboard and checked during the delay</td><td></td></tr><tr><td>End</td><td>Define the last stage of the dungeon. Once this stage is completed, the dungeon ends</td><td><code>true</code> if this is the last stage of the dungeon, more than 1 stage can be defined as last stage</td></tr></tbody></table>

