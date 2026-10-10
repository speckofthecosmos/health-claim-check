# Healthcare reasoning fallacies

Each entry: **name**, one-sentence definition, how it shows up in a patient conversation, and the question that catches it. Grouped by the check question in `SKILL.md` that it belongs to. Entries marked (IHC) adapt an Informed Health Choices Key Concept, CC BY 4.0 (Oxman et al., 2018/2022); changes made.

## 1. Compared with what? (causation from one course of events)

### Single-person before/after (no counterfactual)
- **Definition:** inferring a treatment's effect from one person's values before and after starting it, when what would have happened without it is unobserved.
- **Shows up as:** "Your eGFR has been flat since you started it, so it's working"; "the closest thing to an n-of-1 answer"; "my pain went away after the injection". (IHC: "It worked for me!")
- **Catch:** *What would this line have looked like without the treatment, and how do I know?* If the answer is "we can't know", the trajectory is consistent-with, not evidence-of. A real n-of-1 needs planned crossover, blinding where possible, and repeated periods; a single switch-on is not one.

### Post hoc ergo propter hoc
- **Definition:** treating "B followed A" as "A caused B".
- **Shows up as:** a new symptom blamed on the latest drug; an improvement credited to the supplement started that week.
- **Catch:** *What else changed in the same window, and would B have happened anyway at this point in the disease?*

### Regression to the mean
- **Definition:** an extreme measurement tends to be followed by a less extreme one, with no intervention.
- **Shows up as:** a treatment started *because* a lab was unusually bad, followed by a better lab, read as the treatment working. Same for a flare that prompts a visit and then settles.
- **Catch:** *Was the starting value chosen because it was extreme? What do repeat measurements without treatment look like?*

### Natural history
- **Definition:** the disease's own course (progression, plateaus, remission, flares) mistaken for a treatment effect.
- **Shows up as:** stable eGFR in a disease where many people at that stage and age are stable for years; a self-limiting illness "cured" by whatever was taken.
- **Catch:** *What does the untreated course look like for people like me at this stage, and is my trajectory outside it?*

### Measurement noise mistaken for change
- **Definition:** reading normal test-to-test variation (hydration, lab, assay, time of day, muscle mass for creatinine) as a real change.
- **Shows up as:** "eGFR went from 52 to 58, it's improving"; "creatinine jumped, the drug is hurting me."
- **Catch:** *Is the change larger than the test's usual variation, and has it held across several measurements?*

### Placebo, expectation and attention effects
- **Definition:** improvement from expecting benefit, from extra attention, or from changed behaviour around starting a treatment.
- **Shows up as:** symptom improvement on a new drug, especially for subjective outcomes like fatigue or pain.
- **Catch:** *Is the outcome one that expectation can move, and did anything else about my routine change when I started?* (IHC: "Dissimilar expectations or behaviours")

### Co-intervention (confounded change)
- **Definition:** several changes made at once, with the effect credited to one.
- **Shows up as:** new drug started the same month as a diet change, BP-med adjustment and more water.
- **Catch:** *What else did I start, stop or change at the same time?*

### Correlation to causation / confounding by indication
- **Definition:** an observed association taken as an effect, when a third factor (often the reason for treatment) drives both.
- **Shows up as:** "people on drug X have worse outcomes" (sicker people get X); "people who take Y live longer" (healthier people take Y). (IHC: "Associated with!", "Real world data!")
- **Catch:** *Why did these people get the treatment, and could that reason, not the treatment, explain the outcome?*

### Reverse causation
- **Definition:** the outcome, or early disease, causing the exposure rather than the reverse.
- **Shows up as:** "people who stopped the drug declined faster" when declining is why they stopped.
- **Catch:** *Could the outcome, or its early stage, have caused the exposure?*

## 2. In whom? (indirect evidence)

### Animal / in-vitro / in-silico extrapolation
- **Definition:** treating results in mice, rats, cell lines, organoids or models as evidence of effect in people.
- **Shows up as:** "the drug lowers the risk of kidney failure" when the evidence is slowed cyst growth in a mouse model; "this supplement kills cancer cells" (in a dish).
- **Catch:** *Is there any human outcome data in this disease? If not, the true sentence is "in [model], it did [marker]; untested in people".* Most interventions that work in animal models do not reach approval in humans.

### Different-population transfer
- **Definition:** applying results from one human population to another that differs in disease, cause, stage, genotype, age or co-treatment.
- **Shows up as:** results from diabetic CKD trials presented as evidence for a non-diabetic kidney disease; adult data for a child; trial participants with eGFR above 25 used for someone at 20.
- **Catch:** *Were the trial participants people like me in the way that matters for this mechanism? (IHC: "Are people very different from you?")* GRADE calls this indirectness; it lowers certainty, it does not erase it.

### Ecological fallacy / average effect
- **Definition:** assuming an average or group-level effect applies equally to each individual.
- **Shows up as:** "the trial showed a 30% benefit, so I'll get 30% benefit."
- **Catch:** *Does the average hide people who benefit a lot, some not at all, some harmed?* (IHC: "Average effects")

### Subgroup over-reading
- **Definition:** trusting an effect found in one subgroup of a trial when the overall trial did not show it, or when many subgroups were tested.
- **Shows up as:** "it didn't work overall but it worked in people with my genotype."
- **Catch:** *Was this subgroup pre-specified, is the interaction test significant, and has it been replicated?* (IHC: "Subgroup analyses")

## 3. Which endpoint?

### Surrogate endpoint taken for the outcome
- **Definition:** treating a change in a marker (lab, imaging, biomarker) as a change in the outcome patients care about.
- **Shows up as:** "it lowers albuminuria, so it prevents dialysis"; "it reduced cyst volume, so it preserves kidney function long-term".
- **Catch:** *Has this marker been shown, in this disease and drug class, to predict the outcome when a treatment moves it?* Some kidney surrogates (eGFR slope, albuminuria change, 40-57% eGFR decline) are accepted under defined conditions (NKF/FDA/EMA 2018 workshop); that acceptance is condition-specific. Classic failures: anti-arrhythmics that suppressed ectopic beats and increased deaths (CAST); torcetrapib raised HDL and increased deaths.

### Outcome that doesn't matter to the patient
- **Definition:** a statistically real effect on an outcome the patient does not value, or omission of the one they do.
- **Shows up as:** a drug that slows a marker with side effects that matter more day to day.
- **Catch:** *What outcomes matter to me, and did the study measure them?* (IHC: "What outcomes matter to you?")

### Composite endpoint inflation
- **Definition:** a combined endpoint whose effect is driven by its least important component.
- **Shows up as:** "reduced kidney failure, death or 40% eGFR decline" where nearly all the effect is the eGFR component.
- **Catch:** *Which component carried the result?*

## 4. Mechanism or result?

### Mechanism as evidence
- **Definition:** reasoning that because a treatment acts on a pathway believed to drive the disease, it must improve outcomes.
- **Shows up as:** "it blocks mTOR, mTOR drives cyst growth, so it should slow my disease." (IHC: "It works like this!")
- **Catch:** *Is there outcome data, or only a plausible pathway?* Mechanism says why to test it; only a test says whether it works. (mTOR inhibitors are a real example: a strong pathway rationale in polycystic kidney disease and disappointing trials.)

### Appeal to nature / novelty / tradition
- **Definition:** treating natural, new, or long-used as evidence of safety or benefit.
- **Shows up as:** "it's just a supplement", "it's the newest drug, it must be better", "doctors have used it for decades". (IHC: "New is better!", "Old is better!")
- **Catch:** *What do comparisons show, independent of how old, new or natural it is?*

### More is better / earlier is better
- **Definition:** assuming higher doses, more testing or earlier treatment always improve outcomes.
- **Shows up as:** pushing for a higher dose or more frequent imaging without outcome evidence. (IHC: "More is better!", "Early is better!")
- **Catch:** *Is there evidence the extra dose, test or earlier start changes outcomes, and what does it cost in harm?*

## 5. How big, in absolute terms?

### Relative vs absolute risk
- **Definition:** presenting a relative change without the baseline risk it applies to.
- **Shows up as:** "cuts risk by 50%" when the risk goes from 2% to 1% over five years.
- **Catch:** *From what to what, over what time? What is the NNT?* (IHC: "Relative effects"; IPDAS: present probabilities with the same denominator and time frame.)

### Statistical significance taken as importance
- **Definition:** treating "statistically significant" as "large" or "worth it".
- **Shows up as:** "it significantly slowed decline" when the difference was 0.5 mL/min/year.
- **Catch:** *How big was the effect, and with what confidence interval? Would I notice it?* (IHC: "Statistically significant", "No confidence interval")

### Base-rate neglect
- **Definition:** judging how likely something is from how well it fits, ignoring how common it is.
- **Shows up as:** a positive screening test read as near-certain disease; a rare side effect feared over a common one.
- **Catch:** *How common is this in people like me before the finding, and how much does the finding shift that?* (A finding moves the probability by its likelihood ratio from the base rate; it does not set it.)

### Lead-time and length-time bias
- **Definition:** earlier detection appearing to lengthen survival because the clock started earlier, or because screening catches slower disease.
- **Shows up as:** "people diagnosed by screening live longer, so screening works."
- **Catch:** *Did screening reduce deaths or disease-specific outcomes, or only lengthen time-since-diagnosis?*

### Few people or events
- **Definition:** confident conclusions from small trials or few outcome events.
- **Shows up as:** "a trial showed it works" (n = 40, 3 events).
- **Catch:** *How many people and how many events? Would a few different outcomes reverse it?* (IHC: "Few people or events")

### Simpson's paradox
- **Definition:** a trend in combined data that reverses within every subgroup, because group sizes differ.
- **Shows up as:** a hospital or treatment that looks worse overall but better in every risk stratum.
- **Catch:** *Does the comparison hold within comparable groups?*

## 6. Who is claiming it, and why?

### Label indication vs evidence
- **Definition:** treating FDA approval for an indication as the measure of evidence, or its absence as evidence against.
- **Shows up as:** "it's approved for my disease, so it's proven to prevent kidney failure" (approval may rest on a surrogate); "it's off-label, so there's no evidence" (off-label use can be guideline-supported). For coverage, label and compendia status are the plan's rules, not the science: argue each on its own terms.
- **Catch:** *What did the approval rest on (outcome or surrogate)? Separately, what does the evidence show? Separately, what does the plan's criterion require?*

### "No evidence of harm" vs "evidence of no harm"
- **Definition:** reading absence of data as a negative finding.
- **Shows up as:** "there's no evidence it hurts the kidneys" when it was never studied in CKD; "the trial found no difference" when it was too small to detect one. (IHC: "No evidence")
- **Catch:** *Was it studied with enough people and time to find the effect if it existed?*

### Appeal to authority / "a study shows"
- **Definition:** accepting a claim because of who made it or that a study exists, without checking what was shown.
- **Shows up as:** "my nephrologist says it protects the kidneys"; "a 2023 paper found..." (IHC: "Recommended by experts!", "A study shows!", "Peer reviewed!")
- **Catch:** *What evidence does the authority rest on, and does this one study fit the rest of the evidence?*

### Citation drift
- **Definition:** a claim repeated through reviews, guidelines or websites that grows stronger than the original study supports.
- **Shows up as:** a patient-site sentence "shown to slow progression" that traces to an animal study or a post-hoc analysis.
- **Catch:** *What did the original paper actually report, in whom, for what endpoint?*

### Cherry picking / selective reporting
- **Definition:** citing the supportive studies or outcomes and omitting the rest.
- **Shows up as:** an appeal listing two positive studies and not the larger null trial; a manufacturer page reporting the one outcome that moved. (IHC: "Selective reporting", "Unsystematic summaries")
- **Catch:** *Is there a systematic review, and what does the whole body of evidence say?*

## 7. Would I say this if it cut against the user? (the assistant's own reasoning)

### Motivated reasoning when building the user's case
- **Definition:** lowering the evidential bar for claims that support the conclusion being argued, and raising it for claims against.
- **Shows up as:** a drafted appeal or "is it working" answer that cites the user's trajectory, a mechanism and a mouse study as if they settled the question; dismissing a null trial as "underpowered" while accepting a smaller positive one.
- **Catch:** *If this exact evidence argued for stopping the drug or denying coverage, how strong would I call it?* Rewrite to that strength.

### Anchoring
- **Definition:** sticking to the first framing, diagnosis or hypothesis despite new information.
- **Shows up as:** every later finding read through the first explanation offered in the conversation.
- **Catch:** *If I saw this situation fresh right now, what would I think?* (curiositech `clinical-diagnostic-reasoning`, MIT)

### Premature closure / satisfaction of search
- **Definition:** stopping at the first explanation that fits, without asking what else could explain the findings or co-exist.
- **Shows up as:** a new symptom attributed to the known kidney disease without considering a second cause.
- **Catch:** *Does this explain all the findings? What else could be present at the same time?*

### Framing effect
- **Definition:** the same facts producing different decisions depending on wording (survival vs mortality, gain vs loss).
- **Shows up as:** "90% chance of keeping kidney function" vs "10% chance of losing it" driving different choices.
- **Catch:** *Have I stated it both ways, in absolute numbers?*

### Sunk cost
- **Definition:** continuing a treatment because of what has already been invested in it (time, money, a hard-won approval, side effects endured).
- **Shows up as:** "after fighting the insurer for a year I can't stop now."
- **Catch:** *If I were deciding today from scratch, with today's evidence, would I start it?*

### Commission and omission bias
- **Definition:** preferring to act (commission) or to not act (omission) for its own sake, and judging harms from action differently from harms from inaction.
- **Shows up as:** treating a borderline lab because doing something feels better; refusing a drug because a side effect "would be my fault".
- **Catch:** *Am I comparing the real risks of acting and not acting, on the same scale?*

### Availability
- **Definition:** judging likelihood by how easily examples come to mind.
- **Shows up as:** fear of a rare side effect after reading one vivid forum post; dismissing a common risk nobody talks about.
- **Catch:** *What is the actual frequency, not the most memorable case?*

### Survivorship bias
- **Definition:** drawing conclusions from those who remain visible (still on the drug, still in the forum, still in the study), ignoring those who dropped out.
- **Shows up as:** "everyone in the patient group who stayed on it is doing well."
- **Catch:** *Who stopped, dropped out or died, and what happened to them?* (IHC: "Lots of people not followed-up")

## 8. Coverage-specific

### Stated purpose vs mechanism
- **Definition:** confusing what a treatment is prescribed *for* with how it works, when a benefit rule or exclusion is written about purpose.
- **Shows up as:** an exclusion for "drugs for weight loss" or "cosmetic procedures"; an appeal that argues the drug's weight-lowering or appearance-changing mechanism, which places it in the excluded category, instead of its documented clinical purpose (e.g. a kidney, cardiac or functional indication) and the evidence for that purpose. Also the reverse: a reviewer denying on mechanism when the prescription's purpose is outside the exclusion.
- **Catch:** *What does the exclusion's wording key on: purpose, diagnosis, drug class, or mechanism? Which is this request's documented purpose, and is every sentence of the appeal about that purpose?*

### Medical necessity framed as evidence of efficacy
- **Definition:** conflating the plan's necessity criteria (step therapy tried, diagnosis coded, prescriber specialty) with whether the treatment works.
- **Shows up as:** "they approved it, so it must be effective"; "they denied it, so it doesn't work."
- **Catch:** *Is this a decision about the evidence, or about the plan's rules? Answer each separately.*

## Further reading (link-only sources)

- Catalogue of Bias (Oxford CEBM): https://catalogofbias.org — entry-level detail on most biases above. Linked, not copied.
- IHC Key Concepts 2022: https://zenodo.org/records/6611932 (CC BY 4.0).
- Ottawa Personal Decision Guide: https://decisionaid.ohri.ca/decguide.html — offer when weighing options; do not reproduce or alter.
- CASP checklists: https://casp-uk.net (CC BY-NC-SA 4.0) — for appraising a single study by design.
- Levey AS et al., change in albuminuria and GFR as end points (NKF/FDA/EMA workshop), Am J Kidney Dis 2020 — find via search; do not cite an identifier from memory.
