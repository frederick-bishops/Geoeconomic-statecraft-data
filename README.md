# Geoeconomic Statecraft Simulator: published data

The data files the Geoeconomic Statecraft Simulator page (Designing Decision
Systems, `/lab/geoeconomic-coercion`) reads, updated automatically every day. No code and no raw data; the model,
its pipeline and its tests live in a separate repository.

| File | What |
|---|---|
| `lab/forecasts.json` | The model's forecasts of new trade restrictions between countries, issued automatically and sealed: each record carries a SHA-256 fingerprint of itself and of the record before it, so nothing issued can be changed without breaking the chain. Records are only ever added. |
| `lab/scoreboard.json` | How the forecasts have scored so far (Brier score next to the base rate and to "last period repeats", month by month; calibration). |
| `lab/live.json` | Daily indicators shown on the map: ship traffic through chokepoints, world commodity prices, new sanctions designations, news-based tension, upcoming elections. |

## Sources and terms
- IMF PortWatch (IMF and University of Oxford; AIS data): free to use with attribution under the IMF's terms.
- World Bank Commodity Price Data (the Pink Sheet): CC BY 4.0.
- GDELT Project: open data, with attribution.
- OpenSanctions: CC BY-NC 4.0 (non-commercial use, with attribution); US Treasury OFAC lists: public.
- UN Comtrade and Global Trade Alert: only derived totals and counts appear here, with attribution; their raw records are not redistributed.
- WTO dispute settlement records; IFES ElectionGuide; Wikidata (CC0); UN General Assembly voting data (Voeten et al., Harvard Dataverse).

Updated by a scheduled job; please cite the original sources above.
