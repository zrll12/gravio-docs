---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Basic commands

In Gravio, operations are executed by a series of commands.

Each command should take up a line and ends with semicolon. Everything on that line behind the semicolon were seen as comment and will be ignored.

### Device management commands

This series of command are compiled to M commands in gcode.

#### Usage:

```
MOTOR <Sub command>;
```

#### Comparison Table:

If you need other M-related commands in G-code, just pass the number behind the M as sub command.

<table><thead><tr><th width="269">Gravio subcommand</th><th width="84">G-code</th><th>Desctiption</th></tr></thead><tbody><tr><td>force_stop</td><td>M1</td><td>Stop immediately</td></tr><tr><td>return</td><td>M2</td><td>Return from the program</td></tr><tr><td>start_clockwise</td><td>M3</td><td>Starts the motor to spin clockwise</td></tr><tr><td>strat_counter_clockwise</td><td>M4</td><td>Starts the motor to spin counter clockwise</td></tr><tr><td>stop</td><td>M5</td><td>Stop the motor</td></tr></tbody></table>

### Movement control commands

This series of command are compiled to G commands in G-code.

<table><thead><tr><th>Gravio command</th><th width="102">G-code</th><th>Desctiption</th></tr></thead><tbody><tr><td>JUMP &#x3C;position: Position>;</td><td>G0</td><td>Fast approach a position</td></tr><tr><td>GLIDE &#x3C;position: Position>;</td><td>G1</td><td>Move towards a position</td></tr><tr><td>TURN &#x3C;direction: Direction> &#x3C;position: Position>;</td><td>G2/G3</td><td>Move along a curve</td></tr><tr><td>ORIGINAL &#x3C;index: number>;</td><td>G54-G57</td><td>Set the original point</td></tr><tr><td>DIAMETER;</td><td>G23</td><td>Use diameter for circle</td></tr><tr><td>ABSOLUTE;</td><td>G90</td><td>Use absolute position</td></tr><tr><td>LINER;</td><td>G94</td><td>Use time based speed</td></tr></tbody></table>

### Othor commands

| Gravio command        | G-code | Desctiption |
| --------------------- | ------ | ----------- |
| TOOL \<type: number>; | T\*    | Switch tool |
|                       |        |             |
|                       |        |             |
