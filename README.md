# skyhack-data

Public, machine-readable flight-deal digests for [SkyHack](https://skyhackhq.com) —
the same data `/finder` renders, published as plain JSON.

This repo holds **data only**, generated nightly from the engine in the (private)
`skyhackhq/skyhack` repo. It contains the fields `/finder` actually uses: route,
price, airline, qualifying credit earned, earn-per-dollar, and a live Google Flights
search link for the fare. It does not contain scan-internal fields (trip-length
archetype, raw distance, fare-class codes, region groupings) that aren't rendered
anywhere.

**Usage:** provided as-is for informational use. Not licensed for redistribution or
resale. See [skyhackhq.com/privacy](https://skyhackhq.com/privacy) and
[skyhackhq.com/terms](https://skyhackhq.com/terms).

## Layout

- `digests/manifest.json` — the combos (program × cabin) in the latest run, with scan
  metadata (run date, origins scanned, min/max earn-efficiency).
- `digests/combos/<program>-<cabin>.json` — the actual deals for one combo.
