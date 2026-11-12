# SignalBridge — Product brief

**Status:** Reconstructed concept prototype; discovery and outcome claims are unvalidated.

## Problem hypothesis

When home internet behaves unpredictably, people often cannot tell whether to troubleshoot one device, their home Wi-Fi/router, or their provider. They may repeat irrelevant steps or contact support without the observations needed to route the issue efficiently.

This is a hypothesis, not a finding from completed user research. The prototype tests whether a short, evidence-led flow can help a person choose a sensible next action and produce a useful support handoff.

## Initial audience

People who manage their own home internet and have a common issue such as slow service, intermittent connection, or a device that cannot connect. The initial flow is intended for non-expert consumers, including people who need a clearer path before contacting provider support.

## User journey

1. Select the symptom, how many devices seem affected, and when it started.
2. Optionally report observations from a second device, router status light, or moving closer to the router.
3. Review the likely area to investigate, the clues behind the suggestion, and reversible next steps.
4. Copy or download a support summary that clearly labels observations as user-reported.

## MVP scope

- A responsive, browser-only guided flow.
- Transparent heuristic routing with a low-evidence outcome and cautious confidence wording.
- Safe, reversible suggested checks and explicit outage-verification limits.
- User-reviewed support summary with optional provider name and short note.
- No collection or transmission of answers, credentials, account numbers, addresses, or router telemetry.

## Non-goals for this prototype

- Diagnosing or remotely repairing routers, modems, devices, or provider networks.
- Measuring latency, throughput, packet loss, or Wi-Fi signal.
- Detecting provider outages or integrating provider accounts.
- Replacing provider support or making a guaranteed cause determination.

## Product hypothesis

If a person can answer a few plain-language questions and see why a next step was suggested, then they will be more likely to take an appropriate first action and provide support with a concise, structured description.

## Discovery plan (not yet conducted)

Conduct 6–8 interviews with people who contacted their ISP in the past six months. Ask them to recount their last incident, what they tried, where they got stuck, what information support asked for, and which details they were comfortable sharing. Do not pitch the prototype until after the unaided story.

Then run moderated usability sessions with 5–6 participants across three scenarios: one device cannot connect; several devices lose service; and one app fails while other services work. Ask participants to think aloud, identify which clue influenced the result, and explain whether they would share the generated summary. Observe task completion, misclassification risk, comprehension, and trust.

## Proposed measures and hypotheses

These are proposed evaluation criteria, not measured results:

- **Correct next-step selection:** at least 4 of 5 usability participants choose a safe action consistent with the scenario.
- **Time to useful next step:** median under 3 minutes in moderated sessions.
- **Evidence comprehension:** at least 4 of 5 participants can explain which answers led to the suggestion.
- **Safe abstention:** in ambiguous scenarios, the flow should say that evidence is insufficient instead of naming an unverified outage or root cause.
- **Handoff usefulness:** provider-support reviewers can identify symptom, scope, timing, and checks from the summary without asking the user to re-enter those details.

Do not optimize for a high “diagnosis rate.” A correct, clear abstention is better than a confident but unsupported conclusion.

## Experiment plan

Start with a scenario-based usability test, not a broad launch. Use scripted cases with known answer patterns and an observer rubric. For every case, check whether the result is supported by the provided observations, whether the suggested action is safe, and whether the user understands the limits. Revise confusing questions before comparing completion metrics. If a future pilot is considered, first review privacy, accessibility, provider-specific guidance, and escalation language with subject-matter experts.

## Risks and guardrails

- **False diagnosis:** use “likely,” “possible,” or “not enough evidence”; show the clues; never confirm an outage from user answers alone.
- **Unsafe troubleshooting:** suggest only low-risk observations and settings the user controls; do not ask users to open equipment, alter wiring, or factory-reset hardware.
- **Privacy:** keep this prototype local to the browser and warn users not to include passwords, account numbers, or full addresses in the optional note.
- **Accessibility:** use plain wording, keyboard-operable controls, semantic headings, responsive layout, and reduced-motion support; validate with assistive technology before a production release.
- **Over-trust:** label the app as informational and disclose that it cannot access router or provider telemetry.

## Roadmap

1. Validate the problem and language with interviews and scenario-based usability sessions.
2. Improve the decision tree from observed errors; add validated local-provider instructions only where source and maintenance ownership are clear.
3. Review privacy, accessibility, security, and operational support requirements.
4. Consider provider or device integrations only after explicit consent design, security review, and evidence that integrations improve user outcomes.
