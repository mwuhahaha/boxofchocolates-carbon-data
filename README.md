# BoxOfChocolates.ai Carbon Data

Public, read-only carbon telemetry for
[BoxOfChocolates.ai](https://boxofchocolates.ai/).

The `live` branch contains the latest published snapshot at:

```text
https://raw.githubusercontent.com/mwuhahaha/boxofchocolates-carbon-data/live/carbon/latest.json
```

The publisher replaces the rolling `live` commit every three minutes after
validating source freshness. Consumers should not use the bootstrap snapshot on
`main` as live data.

## Data

- `carbon/latest.json`: current aggregate snapshot on the `live` branch
- `schema.json`: JSON Schema Draft 2020-12 contract
- `ATTRIBUTION.md`: methodology, source attribution, and licensing notes

The snapshot contains only aggregate energy and estimated emissions
measurements. It excludes internal hostnames, IP addresses, node names,
namespaces, pod names, and other infrastructure identifiers.

## Method

Energy measurements combine monitored Kepler CPU/platform energy with NVIDIA
DCGM GPU energy. Estimated emissions combine measured energy with regional
grid-carbon-intensity data for `US-MIDA-PJM`.

These values are estimates for transparency and are not audited carbon
accounting.

## License

This database is available under the
[Open Data Commons Open Database License 1.0](LICENSE). See
[ATTRIBUTION.md](ATTRIBUTION.md) for upstream attribution.
