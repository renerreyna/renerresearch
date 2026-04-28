# Study 1 — Methodology

## Research Question
Do brand collaborations between luxury/cultural brands and visual artists correlate with measurable shifts in public attention, and does the timing of those collaborations relative to major auction events predict different attention signatures?

## Hypothesis
Brand collaborations that precede major auction events are associated with higher attention lift than:
- Auction events occurring without a brand collaboration, or
- Brand collaborations occurring after an artist has already reached peak market value.

## Sample
15 contemporary artists grouped into three scenarios:

### Scenario 1 — Collab precedes auction (n=7)
Artists with documented brand collaborations preceding a major auction event that met or exceeded the 150% above-low-estimate threshold.

- KAWS × Dior (2018) → $14.8M auction record (2019)
- Takashi Murakami × Louis Vuitton (2003) → $15.1M record (2008)
- Yayoi Kusama × Louis Vuitton (2012) → $7.9M record (2019)
- Daniel Arsham × Dior (2019) → auction emergence (2021)
- Jean-Michel Basquiat × Supreme (2013) → $110.5M record (2017)
- Kehinde Wiley × Nike (~2014) → $4.8M record (2019)
- George Condo × Kanye West (2010) → auction breakthrough (2013+)

### Scenario 2 — No brand collaboration (n=6)
Artists with major auction events but no documented brand collaborations in the surrounding window.

- Jenny Saville — $12.4M record (October 2018)
- Banksy — Girl With Balloon shredding event (October 2018)
- Rudolf Stingel — $10M+ record (June 2017)
- Cy Twombly — major sale (November 2011)
- Njideka Akunyili Crosby — $3.1M Sotheby's (November 2018)
- David Hockney — $90.3M record (November 2018)

### Scenario 3 — Auction preceded collab (n=2)
Artists whose brand collaboration occurred *after* their major auction peak.

- Jeff Koons — $58.4M record (November 2013), LV Masters collab (April 2017)
- Gerhard Richter — $46M record (October 2015), Porsche collab (2016)

## Data Source
Google Trends search interest (0-100 relative index), fetched via the `pytrends` Python library. All data pulled from the English-language worldwide Google Trends index.

## Measurement
For each artist:
- **Pre-window:** 18 months immediately before the event anchor date
- **Post-window:** 18 months immediately after the event anchor date
- **Lift ratio:** `post_average / pre_average`
- **Statistical test:** Independent samples t-test comparing pre and post distributions

## Event Anchor Dates
- Scenario 1: anchor on collaboration date
- Scenario 2: anchor on auction event date
- Scenario 3: anchor on collaboration date (to measure whether collab produced lift after existing peak)

## Limitations

**Sample size:** n=15 is small and unequal across groups (7/6/2). Results are directional and exploratory.

**Google Trends relativity:** The 0-100 index is normalized to peak interest within each query window. Values are not directly comparable across artists without explicit co-query normalization.

**Wikipedia data excluded:** Initial attempts to use Wikipedia pageview API returned anomalous data (max 328 views/month for KAWS, when true values should be in the hundreds of thousands). Excluded from analysis pending investigation via NYU library API access or Wikimedia bulk download.

**Selection bias:** Only artists who achieved significant auction events or collaborations are studied. No true baseline of artists with neither event type.

**Confounding events:** Several artists show attention spikes unrelated to the measured events:
- Koons 2019 spike reflects Rabbit selling for $91.1M (a new auction record), not the LV Masters collab
- Hirst 2012 spike reflects the Gagosian global Spot Paintings exhibition and his departure from Gagosian

These confounds are documented and discussed in the notebook but not statistically controlled.

**Correlation not causation:** The study identifies associations between event types and attention patterns. It does not establish that brand collaborations cause attention lift — only that the two co-occur in the patterns described.

## Next Steps

1. Pre-register the hypothesis on OSF before expanding the dataset
2. Resolve Wikipedia API access for triangulation with a second attention signal
3. Expand Scenario 1 to 15+ artists
4. Investigate structural reasons for Scenario 3 scarcity (why do brands rarely engage already-peak artists?)
5. Add institutional event category (major museum retrospectives) as a fourth scenario
