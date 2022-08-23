# iPod Photo Battery Thermistor Analysis

This repo contains data and analysis to determine the `B`/`beta` and `r_inf` values of the NTC thermistor found inside the iPod photo battery.

For details see https://en.wikipedia.org/wiki/Thermistor#B_or_%CE%B2_parameter_equation

## Measurement Setup

- Original iPod Photo Battery
- UNI-T 300S Infrared Thermometer
    - Emissivity set to 0.92
- OWON B35T Multimeter

## Measurement Procedure

1. Place battery in freezer to lower temperature
2. Measure battery temperature with thermometer
    - Measure on black side, not silver side
3. Measure resistance across internal NTC with multimeter (white and black wire)
4. Repeat measurements until battery reaches ambient temperature
5. Repeat all steps until enough data is collected

## Caveats

- The emissivity is little more than a guess, but seems appropriate.
- Temperature at surface of the battery may be slightly different from NTC temperature, this is assumed to be negligible.
- Condensation would occasionally build up on battery, may have thrown off temperature measurements.
- The temperature of the battery likely changes between measurement of temperature and measurement of resistance. This effect is worse at lower temperatures.
- Data may not be valid for 3rd party replacement batteries.
    - I have found at least one 3rd party battery that appears to contain a fixed 10k resistor instead of a real NTC.
    - Other batteries may use NTC thermistors with different properties.