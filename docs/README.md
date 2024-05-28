# Wokwi cd54hct30 Chip

This is a custom chip for [Wokwi](https://wokwi.com/). It implements the cd54hct30 IC.

## Description

The cd54hct30 contain single 2-input Positive-OR gates. Each gate performs the Boolean function
of Y = NOT(A . B . C . D . E . F . G . H)  in positive logic.

## Truth Table
|                                     INPUTS                                    |         |
| ----------------------------------------------------------------------------- |  OUTPUT |
| INPUT A | INPUT B | INPUT C | INPUT D | INPUT E | INPUT F | INPUT G | INPUT H |         |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|    L    |    X    |    X    |    X    |    X    |    X    |    X    |    X    |    H    |
|    X    |    L    |    X    |    X    |    X    |    X    |    X    |    X    |    H    |
|    X    |    X    |    L    |    X    |    X    |    X    |    X    |    X    |    H    |
|    X    |    X    |    X    |    L    |    X    |    X    |    X    |    X    |    H    |
|    X    |    X    |    X    |    X    |    L    |    X    |    X    |    X    |    H    |
|    X    |    X    |    X    |    X    |    X    |    L    |    X    |    X    |    H    |
|    X    |    X    |    X    |    X    |    X    |    X    |    L    |    X    |    H    |
|    X    |    X    |    X    |    X    |    X    |    X    |    X    |    L    |    H    |
|    H    |    H    |    H    |    H    |    H    |    H    |    H    |    H    |    L    |


## Pin names

| Name | Description       |
| ---- | ----------------- |
|  A   | Input signal  A   |
|  B   | Input signal  B   |
|  C   | Input signal  C   |
|  D   | Input signal  D   |
|  E   | Input signal  E   |
|  F   | Input signal  F   |
|  G   | Input signal  G   |
|  H   | Input signal  H   |
|  Y   | Output signal     |
| GND  | Ground            |
| VCC  | Supply voltage    |


## Usage

To use this chip in your project, include it as a dependency in your `diagram.json` file:

```json
  "dependencies": {
    "chip-cd54hct30": "github:wokwi-custom-chips/cd54hct30@0.1.0"
  }
```

Then, add the chip to your circuit by adding a `chip-cd54hct30` item to the `parts` section of diagram.json:

```json
  "parts": {
    ...,
    { "type": "chip-cd54hct30", "id": "chip1" }
  },
```

For a complete example, see [The cd54hct30 chip test project](https://wokwi.com/projects/398977400657873921).
