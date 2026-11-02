# Project-connection notes

**Potential project:** An outdoor travel planner for cities with a local attractions catalog.

**Tools:** A read-only SQLite attractions search to obtain verified places and approximate coordinates, and an Open-Meteo forecast lookup for precipitation probability and maximum wind speed.

**Example combined request:** “Find an outdoor attraction in Stockholm and recommend a forecast date only when precipitation probability is below 30% and wind is below 35 km/h.”

**Possible failure and evaluation:** The assistant may assert that a city has no attractions without checking SQLite, or recommend a date with missing or unacceptable weather. Review full tool traces and confirm a database lookup occurred; check that both numeric thresholds pass on the same date. The dataset includes only four cities and no opening hours.
