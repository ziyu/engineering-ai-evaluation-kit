# Engineering AI Evaluation Kit

A vendor-neutral worksheet for evaluating generated CAD and BIM outputs. Use it to record whether a design survives editing, measurement and handoff, rather than judging only a rendered image.

Maintained alongside the [SKY-001 Independent Guide](https://sky-001.app/#evaluation). We are not affiliated with Skyfall AI and have not independently reproduced SKY-001 benchmarks. This kit is an evaluation aid, not a certification, benchmark dataset or model SDK.

## Files

- [Evaluation protocol](evaluation-protocol.md): define acceptance criteria, run comparable trials and preserve evidence.
- [Trial log](trial-log.csv): import into a spreadsheet or Notion database; one row per complete trial.

## Quick start

1. Copy the CSV and choose a representative task you are permitted to share with a model provider.
2. Define required units, tolerances, editable features, assembly relationships and delivery format **before** viewing outputs.
3. Record the exact input, model/version, output file and evaluator. Do not enter API credentials or confidential design files into a public issue or repository.
4. Execute the same checks for every candidate; log failed attempts and manual repairs as well as successes.
5. Review the evidence with a qualified engineer before manufacturing or construction. Passing this worksheet is not regulatory or safety approval.

## Four checks that a screenshot cannot answer

| Check | Action | Evidence to preserve |
| --- | --- | --- |
| Editability | Open the deliverable in the intended CAD tool; change a specified dimension and regenerate | Input/output format, tool version, lost constraints and regeneration result |
| Geometry and assembly | Measure selected dimensions and inspect units, interference and relationships | Measurement report, declared tolerances, assembly defects |
| BIM handoff | Import the deliverable and inspect object types, properties, levels and coordinates | Import report and any missing semantics |
| Repeatability and total effort | Repeat the same task under the same acceptance criteria, including failed attempts | Trials, retries, latency, direct cost and human repair time |

## Interpret costs without hiding failures

For a group of comparable trials:

- **Acceptance rate** = accepted trials / all trials. Report the numerator and denominator, not just a percentage.
- **Direct cost per accepted design** = total direct model cost for all trials / accepted trials. If no trial passes, report `not defined (zero accepted)`, not zero cost.
- **Total effort per accepted design** = total recorded human-review and repair minutes / accepted trials. Do not add human minutes to machine seconds as though they were the same cost.
- If you choose to monetize labor, disclose the hourly rate and currency separately. Keep provider-reported benchmark cost separate from observed trial costs and retail prices.

A reported IoU overlap score does not establish dimensional tolerances, editability, manufacturability, building-code compliance or safety. Different task sets, hardware, output formats and repair policies make headline comparisons non-equivalent.

## Example use: interpreting SKY-001 claims

The [official SKY-001 product page](https://skyfall.ai/sky-001) presents CAD/BIM demonstrations and comparisons. The [independent guide](https://sky-001.app/) distinguishes those vendor statements from engineering checks a team should run. This repository contains **no measured SKY-001 results**. Do not fill the trial log with vendor figures as if they were your own experiment.

## Contributions

Useful contributions include clearer acceptance criteria, reproducible checks and corrections with a source. Anonymize real evaluation logs and obtain permission before sharing. Do not submit confidential assets, credentials, promotional link lists, fabricated results or claims of vendor affiliation.

## Reuse

You may copy and adapt this original checklist and CSV for internal evaluation or educational use, with attribution to Engineering AI Evaluation Kit and a note of any changes. No permission is granted to use third-party product names or artwork as your own branding. Provided as-is without warranties; users remain responsible for engineering decisions.
