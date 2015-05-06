# Proposed Log Format

The examples shown are in YAML, the standard is not limited to this markup. We
should at least officially support YAML and JSON.

## Fields

- date, must be ISO 8601
- time, HH:MM:SS 24hrs
- location
  - name, a nice name
  - latitude, decimal latitude
  - longitude, decimal longitude
- meta
  - tags, comma separated
  - notes, long form text
- weather
  - air_temp
  - mode, sun/cloud/rain
- computer, that data was imported from
  - make
  - model
- equipment
  - suit
  - weights
  - cylinders
    - type, steel/Al
    - volume, litres
    - identifier
    - last_serviced
    - working_pressure
    - test_pressure
    - start_pressure
    - end_pressure
  - mode
  - computers
  - bc
- dive
  - mode (OC/CCR)
  - duration
  - max_depth, if omitted should be calculated from samples, stay DRY folks!
  - mean_depth, if omitted should be calculated from samples, stay DRY folks!
  - consumption
  - avg_temperature
  - samples, list of samples
    - time, seconds or HH:MM:SS?
    - depth
    - temperature
