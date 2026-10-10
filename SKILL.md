---
name: health-reasoning
description: >
  Load during any conversation about the user's or another patient's health, medical care or coverage of care:
  weighing a treatment or drug, reading a study or lab trend, interpreting their own results over time,
  preparing for an appointment, drafting a letter, appeal, prior-auth or exception request to an insurer,
  pharmacy or doctor, or arguing whether something helps or harms. Triggers even when the user never says
  "fallacy", "bias" or "evidence" — "is this drug working", "my eGFR went up since I started X",
  "write the appeal", "the study shows", "does this lower my risk" are all triggers. It is a pre-statement
  check the assistant runs on its own causal and evidential claims before saying or drafting them, hardest
  when it is building a case in the user's favour, plus a reference list of the fallacies that distort
  healthcare decisions. Patient-side, not a clinician or manuscript tool, and not a disclaimer skill.
---

# health-reasoning

Before the assistant says that something causes, helps, harms, lowers the risk of, or "is evidence for" anything in a health conversation, it runs the check below on that sentence. The aim is a true sentence of the right strength, said plainly. This is not a hedge or a refusal. The skill is for users who want rigor, not "consult your doctor": people managing a chronic condition, patients who read the studies themselves, people writing appeals and exception requests.

**Why:** in one session the assistant called a user's own lab trajectory on a drug "the closest thing to an n-of-1 answer" to whether the drug helps or harms their disease. The user corrected it: a single-person before/after has no counterfactual; nobody can know what that lab value would have done without the drug. The same session nearly passed along a drafted letter claiming the drug lowered the risk of a hard outcome in a disease where the only evidence was animal data. Both claims were on the user's side. That is the failure this skill exists for: the assistant's reasoning gets weakest exactly where it is helping most.

## The check (run on every causal or evidential claim before stating it)

Seven questions. Most claims pass the first two in a second; a claim that fails any one is rewritten (next section) before it is said or written down.

1. **Compared with what?** A claim that X helped or hurt is a claim about the difference from the world without X. Name the comparison that supports it. If the only comparison is the same person before and after, there is no counterfactual: natural history, regression to the mean, other changes made at the same time, and measurement noise all fit the same data. A personal trajectory can show consistency with a claim, or a safety signal worth raising; it cannot show the effect.
2. **In whom?** Is the evidence from people with this disease, at this stage, of this genotype or subtype, on this co-treatment? Mouse, rat, cell-culture, organoid and in-silico data are evidence about the model, not about the patient. Data in a different human population (another kidney disease, diabetic vs non-diabetic CKD, a different age band) is indirect. Say which one it is.
3. **Which endpoint?** Does the evidence show the outcome the claim names (kidney failure, dialysis, death, symptoms, function), or a marker (eGFR, albuminuria, cyst volume, a lab value, a pathway readout)? A marker counts as the outcome only where it has been validated as a surrogate *for this disease and this drug class*, and that validation is itself a claim to check.
4. **Mechanism or result?** "It works by blocking Y, and Y drives the disease" is a reason to run a trial, not a result. Many drugs with a sound mechanism failed or harmed on outcomes.
5. **How big, in absolute terms?** A relative reduction ("cuts risk 30%") without the baseline risk is unreadable. Restate as absolute risk over a stated time, or NNT, before using it.
6. **Who is claiming it, and why?** Is this the drug label, a guideline, a trial result, a review's conclusion, a manufacturer page, a forum, or the assistant's own inference? A label states an approved indication, which is a regulatory fact, not a measure of evidence (and the absence of an indication is not evidence of no effect). "No evidence of harm" means nobody measured or found it, not that it is safe.
7. **Would I say this if it cut against the user?** When the claim helps the case being built (an appeal, a prior auth, "is it working", "should I stay on it"), apply the bar that would be applied to the same claim arguing the other way. If the honest answer is "I would call that weak", it is weak here too.

For coverage arguments, add one: **purpose or mechanism?** An exclusion or criterion is usually written about the *purpose* of a treatment (cosmetic, weight loss, fertility, experimental). Argue from the documented clinical purpose of this prescription and the evidence for that purpose. Arguing from mechanism ("it works by reducing weight, which protects the kidneys") can walk the request straight into the exclusion it was meant to avoid.

The full list of fallacies, each with the question that catches it, is in [`references/fallacies.md`](references/fallacies.md). Load it when reading a study, drafting anything to an insurer or clinician, or when a claim is close to the line.

## When a claim fails the check

1. **Say the weaker claim that is true.** Not "the drug prevents heart failure" but "in a rat model it reduced cardiac fibrosis; there is no human outcome data for this use." Not "your eGFR trajectory is the n-of-1 answer" but "your eGFR has been stable on it, which fits benefit and fits the disease's natural course at your stage; it rules out a large rapid decline." Use the support levels plainly: shown in people like you / shown in a related population / shown only in a marker / shown only in animals or cells / not studied.
2. **Say what would settle it.** Name the evidence that would make the strong claim true: an RCT in this disease with the named outcome, a validated-surrogate trial, a registry comparison with a matched control group, a stopping and restarting pattern (where safe and clinically agreed), or for the user's own data, a comparison against their pre-drug slope with the noise band stated.
3. **Keep the goal; drop only the bad argument.** If the user wants the drug covered, the appeal still gets written, built on what is true: guideline position, label or compendia status, the clinician's documented rationale, the specific marker evidence, the harm of the alternative, the gap in treatment options. A weaker true argument usually also survives a reviewer better than a strong false one. Never quietly abandon the goal because one argument failed; say which argument was dropped and why.
4. **Do not over-correct into uselessness.** "We can't know anything" is also false. Indirect and mechanistic evidence are real evidence with a known weight; say the weight. The output is a calibrated sentence, not a disclaimer.

## Sources and citations

- Cite only sources actually retrieved in the session, with the URL the search returned. Never write a PMID, DOI or trial number from memory.
- If the search finds nothing in the user's population, that is a finding: say "there are no human outcome trials in this disease" out loud rather than filling the gap with the nearest population.
- Name the study type, population and endpoint each time a study is used, in a few words: "RCT, 1,400 adults with diabetic CKD, outcome kidney failure or death at 2.6 years".

## Common mistakes

- **Treating the user's own trajectory as a trial.** It is the most persuasive data in the conversation and the least able to answer a causal question. It can rule out large effects and flag safety signals; it cannot measure benefit.
- **Letting the drafted document carry a claim the chat would not.** Letters, appeals and messages get the check sentence by sentence before they are handed over. A claim in a draft is the assistant's claim.
- **Borrowing evidence from the nearest disease.** Results in a related kidney disease are indirect evidence and must be labelled so; they are not "the evidence" for this one.
- **Reading "approved for" as "proven for" and "not approved for" as "doesn't work".** The label is about what was submitted and accepted.
- **Hedging everything.** If the evidence is strong, say so plainly; a calibrated "this is well established in people like you" is part of the job.
- **Checking only the user's reasoning.** The check is for the assistant's own sentences first; the user's claims get it too, but as a collaborator, never as a gatekeeper.

## Provenance

Built 2026-10. Borrows, with changes: the anti-confirmatory and "absence of evidence is a finding" principles and the citation-integrity rule from DrCatHicks/informed-patient (CC BY 4.0); claim labels and several catching questions from the Informed Health Choices Key Concepts (Oxman et al., CC BY 4.0); the forbidden-upgrade list and graded support scale, paraphrased, from aipoch/medical-research-skills `paper-to-claim-verifier` (MIT); the fallacy roster, rewritten, from K-Dense-AI `scientific-critical-thinking` (MIT); the "fresh eyes" reset from curiositech/some_claude_skills `clinical-diagnostic-reasoning` (MIT). Concepts, not text, from Croskerry (cognitive dispositions to respond), GRADE (indirectness, outcome importance), JAMA Users' Guides (surrogate validity), IPDAS (absolute-risk presentation) and CASP.
