# Dashboard And Chart Output

Use this reference when the user asks for a `shareable dashboard`, `charts`, `chart-ready output`, `scorecard graphic brief`, `LinkedIn-ready dashboard`, or similar presentation-ready final output.

The dashboard is a markdown-friendly artifact. Do not render charts, install visualization libraries, or imply that chart formatting changes the research verdict.

## Placement

Include the dashboard after the weighted scorecard and before sources/verdict. Keep the mandatory final `## Verdict` table as the last decision block.

If the user asks only for the normal advisor output, do not add the dashboard by default.

## Required Sections

### Dashboard Status

State:

- `Dashboard status`: Final / Provisional.
- `Score status`: Final / Provisional.
- `Confidence`: High / Medium / Low.
- `Evidence quality`: Primary / Official fallback / Mixed / Secondary-only.
- `Do-not-overstate note`: one sentence explaining missing data, stale timestamps, source conflicts, or hard gates.

Use `Provisional` when any department score is unavailable, primary documents are missing, official subscription data is missing, GMP sources conflict, or a hard gate remains unresolved.

### Verdict Card

Use a compact table that can be pasted into a note, document, or social post:

| Field | Display |
|---|---|
| IPO | Name and mainboard/SME classification |
| Decision | Apply / Neutral / Avoid |
| Final score | X/100 or Provisional |
| Confidence | High / Medium / Low |
| Best suited for | Listing gains / Long term / Both / Neither |
| Main reason | One short evidence-backed sentence |
| Biggest risk | One short evidence-backed sentence |
| Data status | Final / Provisional with reason |

Do not personalize the card to the user's financial circumstances. Use research framing such as `Retail research view`.

### Weighted Score Dashboard

Use the same six departments and weights from `skills/shared/references/ipo_scorecard_model.md`.

| Department | Score | Weight | Contribution | Confidence | Evidence quality | Source note |
|---|---:|---:|---:|---|---|---|
| Financial quality | X/100 or Unavailable | 25% | X/25 or Provisional | High/Medium/Low | Primary/Mixed/etc. | DRHP/RHP/source caveat |
| Valuation / peer comparison | X/100 or Unavailable | 20% | X/20 or Provisional |  |  |  |
| Governance, red flags, issue structure | X/100 or Unavailable | 20% | X/20 or Provisional |  |  |  |
| Demand quality | X/100 or Unavailable | 15% | X/15 or Provisional |  |  |  |
| GMP / listing sentiment | X/100 or Unavailable | 10% | X/10 or Provisional |  |  |  |
| Application fit, liquidity, timeline risk | X/100 or Unavailable | 10% | X/10 or Provisional |  |  |  |

Do not treat unavailable departments as zero. Mark the total provisional instead.

### Text Bar Chart

Represent each department with a fixed 10-block text bar. Use approximately one filled block per 10 score points.

```text
Financial quality                  [########--] 82/100  High
Valuation / peer comparison        [######----] 62/100  Medium
Governance / issue structure       [#######---] 74/100  Medium
Demand quality                     [########--] 80/100  Medium
GMP / listing sentiment            [#####-----] 52/100  Low
Application / liquidity / timeline [######----] 65/100  Medium
```

If a score is unavailable, use:

```text
Demand quality                     [??????????] Unavailable  Low - official subscription missing
```

### Radar Chart Data

Provide chart-ready data even when no chart is rendered. Use valid JSON and set unavailable values to `null`.

```json
{
  "chart_type": "radar",
  "scale": {"min": 0, "max": 100},
  "series": [
    {"axis": "Financial quality", "score": null, "confidence": "Low", "evidence_quality": "Mixed"},
    {"axis": "Valuation / peer comparison", "score": null, "confidence": "Low", "evidence_quality": "Mixed"},
    {"axis": "Governance / issue structure", "score": null, "confidence": "Low", "evidence_quality": "Mixed"},
    {"axis": "Demand quality", "score": null, "confidence": "Low", "evidence_quality": "Secondary-only"},
    {"axis": "GMP / listing sentiment", "score": null, "confidence": "Low", "evidence_quality": "Secondary-only"},
    {"axis": "Application / liquidity / timeline", "score": null, "confidence": "Low", "evidence_quality": "Mixed"}
  ]
}
```

### Chart-Ready JSON

Use valid JSON, not pseudocode. Include source and caveat fields so the artifact stays source-aware when shared outside the conversation.

```json
{
  "ipo": {
    "name": "IPO name",
    "classification": "Mainboard / NSE Emerge / BSE SME / Unknown",
    "issue_stage": "Open / Closed / Listed / Unknown",
    "data_checked_at": "YYYY-MM-DD or unknown"
  },
  "decision": {
    "verdict": "Apply / Neutral / Avoid",
    "best_suited_for": "Listing gains / Long term / Both / Neither",
    "final_score": null,
    "score_status": "Final / Provisional",
    "confidence": "High / Medium / Low",
    "hard_gates": [],
    "confidence_caps": [],
    "not_financial_advice": true
  },
  "departments": [
    {
      "name": "Financial quality",
      "score": null,
      "weight": 25,
      "weighted_contribution": null,
      "confidence": "Low",
      "evidence_quality": "Mixed",
      "source_note": "Source or missing-data caveat"
    }
  ],
  "sources": [
    {
      "name": "Source name",
      "tier": "Tier 1 / Tier 2 / Tier 3",
      "used_for": "Field or department",
      "freshness": "Timestamp/date/caveat"
    }
  ]
}
```

### CSV Data Block

Include CSV when the user asks for charting in spreadsheets or a graphic brief:

```csv
department,score,weight,weighted_contribution,confidence,evidence_quality,source_note
Financial quality,,25,,Low,Mixed,Source or missing-data caveat
Valuation / peer comparison,,20,,Low,Mixed,Source or missing-data caveat
Governance / issue structure,,20,,Low,Mixed,Source or missing-data caveat
Demand quality,,15,,Low,Secondary-only,Official subscription missing or timestamp caveat
GMP / listing sentiment,,10,,Low,Secondary-only,GMP is unofficial and source-variable
Application / liquidity / timeline,,10,,Low,Mixed,Issue-specific timetable or SME caveat
```

## Graphic Brief

When asked for a `scorecard graphic brief` or `LinkedIn-ready dashboard`, add a short production brief:

- Format: square post, slide, or document card, as requested.
- Headline: `IPO Name: Apply / Neutral / Avoid research view`.
- Primary visual: six-part weighted scorecard, not a single GMP number.
- Required badges: `Provisional` if applicable, `Confidence: X`, `GMP unofficial`, and `Not financial advice`.
- Footnote: key sources and data checked date.

Do not write promotional copy, FOMO language, or guaranteed-return language.
