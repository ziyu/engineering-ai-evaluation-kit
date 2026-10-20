# CAD/BIM model trial protocol

## 1. Establish a fair comparison

Write the task brief before running any model. Keep inputs, acceptance criteria and allowed human intervention consistent across candidates. Record any unavoidable differences instead of collapsing them into a single ranking.

Record:
- Task identifier and permitted input asset/version.
- Model identity, model version and evaluation date.
- Expected deliverable type and target application/version.
- Required unit system, reference coordinate system and critical measurements.
- Required editable features and assembly relationships.
- For BIM: required object types, property sets, levels and coordinate preservation.
- Maximum allowed retries and what counts as a complete trial.
- Evaluator identity in private records; use an anonymized identifier in shared logs.

Do not upload proprietary designs before checking provider data retention, training-use terms and your permission to disclose the inputs.

## 2. Preserve the raw result

Save the output before manual repairs. Store the original prompt or input hash, configuration, model version, timestamps and output identifier together. Record failure cases, refusals and unusable output, not only successful demonstrations.

The public CSV is a schema for your observations, not a request to publish sensitive information. Use private paths or hashes and remove personal or confidential material before sharing.

## 3. Run acceptance checks

### Editable geometry

Open the actual deliverable, not a screenshot. Change one predetermined dimension. Regenerate dependent features. Record whether topology, constraints or downstream geometry break. Label a check `not applicable` only with an explanation; never silently mark it as passed.

### Dimensions and assemblies

Check the prescribed dimensions against the tolerances in the task brief. Inspect units, part count, interference, alignment and mating relationships. A visually similar model can fail these checks.

### BIM information

Import into the intended BIM environment. Inspect object classes, required properties, level assignments and coordinates. A viewable floor plan is not evidence of useful object semantics or compliance with local building requirements.

### Repeatability and repair

Apply the same test across repeated trials. Record generation time, retries, errors, direct model charges and human repair/review time. State whether the decision is based on the raw or repaired output. Keep repair policy consistent.

## 4. Make an explicit decision

Use `pass`, `fail`, or `not_applicable` for each check, with evidence. Overall acceptance requires every mandatory check to pass. Incomplete or untested checks must not become an overall pass.

Report sample size, failed attempts and exceptions. Cost per accepted result is undefined when zero outputs are accepted. Do not extrapolate a small experiment to all CAD/BIM tasks or to manufacturing safety.

## 5. Communicate limitations

A useful report states what was tested, what was not tested and what remains unknown. Vendor benchmarks, your observations and suggested evaluation questions are different evidence types. Keep them separate.

This checklist supports a trial; it does not replace a qualified engineer, safety assessment, contractual review or regulatory approval.
