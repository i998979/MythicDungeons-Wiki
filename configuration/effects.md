# Effects

EffectLib is used for particle effects. Please make sure you have [EffectLib](https://dev.bukkit.org/projects/effectlib) installed on your server.

This feature is for advanced users. If you want to create your own effects, please read [https://github.com/elBukkit/EffectLib/wiki/Parametric-Equations](https://github.com/elBukkit/EffectLib/wiki/Parametric-Equations) for more information.

Please visit [here](effects.md#brief-explanation) if you need a brief explanation.

{% code title="effects.yml" lineNumbers="true" %}
```yaml
Effects:
  EffectLib:
    vortex:
      class: VortexEffect
      iterations: 1
      particle: smoke
      helixes: 16
      circles: 1
      grow: 0.0
      radius: 1
      period: 10
      pitch: 90
    equation:
      class: EquationEffect
      xEquation: 0
      yEquation: "0.5t"
      zEquation: 0
      duration: 10000
      particles: 10
      cycle: true
      x2Equation: "sin((0.3141) * t2)"
      y2Equation: 0
      z2Equation: "cos((0.3141) * t2)"
      particles2: 20
    equation2:
      class: EquationEffect
      xEquation: "sin(0.3141 * t)"
      yEquation: "0.5t"
      zEquation: "cos(0.3141 * t)"
      duration: 10000
      particles: 20
      cycle: true
```
{% endcode %}

## Brief explanation

The effects listed [here](https://github.com/elBukkit/EffectLib/tree/master/src/main/java/de/slikey/effectlib/effect) can be used in the section `class` below. You can add/remove options mentioned [here](https://github.com/elBukkit/EffectLib/blob/master/src/main/java/de/slikey/effectlib/Effect.java).&#x20;

Remember only `public` variables can be added/removed and `class` is REQUIRED. In addition, effect-specific options can be added, it depends on what kind of effects you have used. You may check effect-specific options [here](https://github.com/elBukkit/EffectLib/tree/master/src/main/java/de/slikey/effectlib/effect).

The example below creates a `DnaEffect` named `DNA` with `period` of `1` and effect-specific option `length` of `15`, then the file will look like this:

{% code title="" lineNumbers="true" %}
```yaml
Effects:
  EffectLib:
    DNA:
      # comes from https://github.com/elBukkit/EffectLib/tree/master/src/main/java/de/slikey/effectlib/effect
      class: DnaEffect
      # comes from https://github.com/elBukkit/EffectLib/blob/5533225c8f733ac33685c9bc0bb82e1b19a58e62/src/main/java/de/slikey/effectlib/Effect.java#L85
      period: 1
      # comes from https://github.com/elBukkit/EffectLib/blob/5533225c8f733ac33685c9bc0bb82e1b19a58e62/src/main/java/de/slikey/effectlib/effect/DnaEffect.java#L57
      length: 15
```
{% endcode %}
