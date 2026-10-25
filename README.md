# Geoeconomic Statecraft Simulator: published data

The data files the Geoeconomic Statecraft Simulator page (Designing Decision
Systems, `/lab/geoeconomic-coercion`) reads, updated automatically every day. No code and no raw data; the model,
its pipeline and its tests live in a separate repository.

| File | What |
|---|---|
| `lab/forecasts.json` | The model's forecasts of new trade restrictions between countries, issued automatically and sealed: each record carries a SHA-256 fingerprint of itself and of the record before it, so nothing issued can be changed without breaking the chain. Records are only ever added. |
| `lab/scoreboard.json` | How the forecasts have scored so far (Brier score next to the base rate and to "last period repeats", month by month; calibration). |
| `lab/explanations.json` | Model parameters and derived feature values that reproduce individual sealed monthly probabilities. Linked to each cycle's fingerprint; the explanations themselves are not sealed. Unavailable inputs are explicit, and capture attempts stop after day 7 of the cycle month. |
| `lab/live.json` | Daily indicators shown on the map: ship traffic through chokepoints, world commodity prices, new sanctions designations, news-based tension, upcoming elections and leaders, UN votes, and the other ties between countries (investment, bank claims, students, tourists, US Treasury holdings). |
| `lab/chains.json` | Retaliation chains: how targets answered when another country started measures against them (in kind, another lever, the WTO, backing down, new partners, nothing), counted from the records and from a researched catalogue, with the researched moves and their sources. |

## Sources and terms
- IMF PortWatch (IMF and University of Oxford; AIS data): free to use with attribution under the IMF's terms.
- World Bank Commodity Price Data (the Pink Sheet): CC BY 4.0.
- GDELT Project: open data, with attribution.
- OpenSanctions: CC BY-NC 4.0 (non-commercial use, with attribution); US Treasury OFAC lists: public.
- UN Comtrade and Global Trade Alert: only derived totals and counts appear here, with attribution; their raw records are not redistributed.
- WTO dispute settlement records (non-commercial reuse with attribution); IFES ElectionGuide (non-commercial research use with attribution); Wikidata (CC0); UN General Assembly voting data (Voeten et al., Harvard Dataverse, CC0).
- TIES, Threat and Imposition of Economic Sanctions v4 (Morgan, Bapat and Kobayashi 2014): counts only, cited.
- IMF CPIS and CDIS (free reuse with attribution; commercial reuse needs the IMF's permission); BIS locational banking statistics (cite the BIS); US Treasury TIC (public domain).
- UNESCO Institute for Statistics: CC BY-SA 4.0. The student figures in `lab/live.json` are derived from it and are shared under the same licence (CC BY-SA 4.0).
- National tourism offices: Australian Bureau of Statistics (CC BY 4.0), Statistics Canada (Open Licence), JNTO, NTTO (public domain), SingStat (Singapore Open Data Licence), Turkiye's Ministry of Culture and Tourism, Taiwan Tourism Administration (Taiwan open data licence), Geostat.

Updated by a scheduled job; please cite the original sources above.
