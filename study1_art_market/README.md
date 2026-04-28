~ Exploring Attention Dynamics in Contemporary Art Forms ~
~ Event-Driven Signals Across Auctions, Institutions, Brand Collaborations, and Social/Popular Media ~

An exploratory research project investigating the factors surrounding major events in an artist's career; auction records, brand collaborations, institutional shows, etc, producing measurable shifts in public attention, and what about those events predict different attention signatures.



~ Research Questions ~

- How does public attention change before and after major events for an artist?
- Is there a measurable spike, decay, or sustained attention effect following certain events?
- Do artists without major events or projects exhibit different baseline attention trajectories? How are they different?



~ Studies in This Repo~

~ Study 1 ~
Brand Collaboration and Attention Lift
Status:
Exploratory analysis complete (n=13 artists)

Investigates whether brand collaborations that precede major auction events correlate with measurably different attention lift compared to artists without collaborations or artists who received collaborations after their market peak.

Key finding:
 In this sample, brand collaborations preceding auction events are associated with meaningfully higher attention lift than auction events alone or post-peak collaborations. Pattern consistent across two control conditions.

See `notebooks/attentionxauctions.ipynb` for the full analysis.

---

~ Repository Structure ~

```
attention_dynamics/
├── README.md                   ← you are here
├── data/
│   └── clean_study_data.csv    ← verified artist-brand-auction dataset
├── notebooks/
│   └── attentionxauctions.ipynb   ← Study 1 full analysis
├── figures/                    ← generated output figures
├── scripts/                    ← reusable analysis functions
├── docs/
│   └── methodology.md          ← detailed methods notes
├── requirements.txt            ← Python dependencies
└── .gitignore
```

---

~ How to Reproduce ~

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/attention_dynamics.git
cd attention_dynamics

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/art_brand_study.ipynb

# Run all cells from top to bottom
# Kernel → Restart & Run All
```

Google Trends fetch takes approximately 60 seconds due to rate-limiting delays between artist requests.

---

~ Limitations ~

This is **exploratory research**, not a confirmatory study. Specifically:
- Small sample sizes (n=7, n=6, n=2 across the three scenario groups)
- Google Trends provides relative (0-100) not absolute search volume
- Wikipedia pageview API returned anomalous data and was excluded pending investigation
- Selection bias : only artists who achieved significant sales are studied
- Correlation not causation

---

~ About ~

Built by **Rene Roelreyna** — NYU Steinhardt Applied Psychology undergraduate (2027), incoming Research Assistant at Icahn School of Medicine at Mount Sinai, working at the intersection of cognitive/computational neuroscience and analytics of humanities.

This repo is part of an ongoing research direction exploring my interest in art, people, and the mystery life :D

---

~ Contact ~

- Email: rrr9353@nyu.edu / rene@kismithgallery.com
- LinkedIn: https://www.linkedin.com/in/rene-reyna-a7837a391/
