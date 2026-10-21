# Head / Heart / Gut questionnaire: design spec

Oct 19, 2026 · @james

Keep the 30-item, three-scale structure and equal weights. Change four things: a fully labeled 5-point frequency scale, tap buttons instead of a slider, mean-based scoring with coarser rounding, and result bands tied to the scale labels.

## Recommended specification

Each line below is the default to build. Section 2 says how strong the evidence is for each one.

- **Items:** 30 statements, 10 per dimension, interleaved. Keep your dimension assignments.
- **Item form:** one behavior or experience per item, first person, plain words. No frequency words (usually, often, most days) inside the statement, because the scale carries frequency.
- **Keying:** 7 positive and 3 reverse-keyed items per dimension. Write reverse items as plain statements of the opposite behavior, never with "not" or "never".
- **Instruction:** "For each statement, choose how often it was true for you over the past month. Answer for how you are, not how you want to be. There are no right answers."
- **Response scale:** 5 points, every point labeled: Almost never · Rarely · Sometimes · Often · Almost always.
- **Control:** five full-width tap targets stacked vertically on mobile, horizontal on desktop. Nothing is selected at the start.
- **Skips:** a small "Skip" link under each item. A dimension needs at least 8 of its 10 items answered to get a score.
- **Scoring:** reverse-score, take the mean of the answered items (1–5), convert to 0–100, round to the nearest 5.
- **Display:** three independent bars on one 0–100 axis. Each bar shows a phrase from the scale ("between Sometimes and Often") first and the number second.
- **Bands:** cut points at 25 and 75, which match the labels Rarely and Often. A score within 5 points of a cut point says "near the line".
- **Comparisons:** name a lowest or highest dimension only when it is at least 15 points from the others.

## Decision table

Evidence strength: **Strong** = several controlled experiments agree. **Moderate** = some experiments, or consistent expert guidance. **Mixed** = studies disagree. **Judgment** = no direct research; my recommendation for this product.

| Topic | Current | Recommended | Rationale | Evidence | Tradeoff |
| --- | --- | --- | --- | --- | --- |
| Response format | Agree / disagree | Frequency (how often) | Agree/disagree scales invite yes-saying and gave lower measurement quality than item-specific scales | Strong | Ability items ("I can…") need light rewording |
| Number of points | 7 | 5 | 5 points beat 7 or 11 on agree/disagree scales; 5 fully labeled points fit a phone | Moderate | Fewer score steps (41 instead of 61) |
| Labels | Ends and middle only | Every point | Full labels improve reliability and make the meaning of each point clear | Moderate | Labels take space |
| Midpoint | "Neutral" | "Sometimes" | A neutral midpoint often hides "don't know"; a frequency midpoint has real content | Moderate | None of note |
| Control | Slider | Tap buttons | Sliders produced more missing data and longer response times, worst on mobile | Moderate | More vertical space |
| Start state | Thumb shown at 4 | Nothing selected | Removes any visual anchor; sliders show start-position effects in some studies | Mixed | None of note |
| Missing answers | All required | Skip allowed, 8 of 10 needed | A forced answer to an item that does not fit becomes a fake midpoint | Judgment | Score rests on 8–10 items |
| Time frame | "Usually" | "Over the past month" | A fixed window gives everyone the same frame and makes retakes comparable | Judgment | Captures a recent state, not "all of life" |
| Reverse items | 7 + 3 | 7 + 3, no negations | No established ratio; negations cause the most misresponse | Mixed | Partial, not full, cancel of yes-saying |
| Weights | Equal | Equal | No data exists to set other weights | Moderate | None |
| Score | Sum to 0–100, integer | Mean to 0–100, nearest 5 | Same math; the mean handles skips; integers imply false precision | Strong (math) / Judgment (rounding) | Less fine-grained number |
| Bands | Cuts at 40 / 70 | Cuts at 25 / 75 + "near the line" | Ties the band to the labels the person chose | Judgment | Middle band is wider |
| Weakest dimension | Not specified | Name only on a gap of 15+ points | Small gaps are within answer noise | Judgment | Some profiles get no "focus" line |

## Wording

The main fix is to remove frequency words from the statements and let the scale ask "how often". The other fixes split double items and put the situation first.

**Rules (broadly supported guidance):**

- **One idea per item.** An item with "or" / "and" gets an unclear answer when only one half is true.
- **No frequency words inside the item.** "Disagree" with "I often wait…" can mean "sometimes" or "never". The answer carries two quantifiers at once.
- **Vague quantifiers are relative.** People judge "often" against their own norm or peers. A fully labeled scale with a stated time frame narrows that drift; it does not remove it.
- **"I can" vs "I do".** "I can" asks about ability, and most people rate their ability high. "I do" or a plain behavior asks what happens. Use a behavior where the meaning allows.
- **Situation first** ("When I make a mistake, …") so the reader knows the context before the claim.
- **Plain, non-judgmental verbs.** Describe what happens, not whether it is good. This lowers the pull toward the desirable answer.
- **No absolutes** (always, never) and **no negations** (not, don't) inside items.

**Rewrites (your meaning and dimension kept):**

| Before | After | Change |
| --- | --- | --- |
| I can usually explain clearly why I believe what I believe. | When someone asks why I believe something, I explain my reasons clearly. | Frequency word removed; behavior and situation instead of ability |
| I can name what I feel in the moment with some precision. | I can put a specific name to what I feel in the moment. | Hedge "with some precision" removed; "can" kept because naming is the skill |
| I usually know what I want before I can explain why. | I know what I want before I can explain why. | Frequency word removed |
| I can say a plain no without over-explaining. | I say no plainly, without over-explaining. | Ability changed to behavior |
| I offer myself kindness when I make a mistake. | When I make a mistake, I treat myself kindly. | Situation first; plainer verb |
| My body feels grounded and settled on most days. | My body feels grounded. | Frequency word removed; split — add "My body feels settled." only if it is a separate idea for you |
| My thoughts often loop on the same worry without going anywhere. (R) | My thoughts loop on the same worry without getting anywhere. (R) | Frequency word removed |
| I often wait for permission or reassurance before small decisions. (R) | Before a small decision, I wait for someone else's OK. (R) | Frequency word removed; "permission or reassurance" merged into one idea |
| When strong feelings come up, I go numb or change the subject. (R) | When strong feelings come up, I go numb. (R) + When strong feelings come up, I change the subject. (R) | Split: one is inner, one is outward behavior |
| I keep people at a distance, even people I trust. (R) | No change | Already one idea, plain words |
| I find it hard to receive care or compliments. (R) | When someone shows me care, I find it hard to take in. (R) | Split "care or compliments"; add a compliment item only if you need it |

If you split an item, drop a weaker item in the same dimension so each dimension stays at 10.

## Response scale and controls

Use a 5-point frequency scale with every point labeled, shown as five tap buttons with nothing selected.

| Value | Label |
| --- | --- |
| 1 | Almost never |
| 2 | Rarely |
| 3 | Sometimes |
| 4 | Often |
| 5 | Almost always |

- **Frequency vs agreement.** Item-specific scales scored about 20% higher in measurement quality than agree/disagree scales across countries in the European Social Survey experiments. Frequency also removes the double quantifier problem from the Wording section.
- **5 vs 7 points.** Krosnick and Presser suggest 7 points for bipolar scales (agree–disagree) and 5 for unipolar ones. Frequency is unipolar. Revilla, Saris and Krosnick found 5 points beat 7 and 11 on agree/disagree scales. Five labeled options also fit a phone without truncation.
- **Labels.** Label every point. Partial labels pull answers toward the labeled points, and full labels make the spacing clear.
- **Midpoint.** A "neutral" or "neither" midpoint often works as a polite "don't know". "Sometimes" is a real answer, so it does not have this problem.
- **"Not applicable".** Do not add it as a sixth button. Write items that apply to everyone, and use the Skip link for the rare misfit. If you do show N/A, put space between it and the five points.
- **Slider vs buttons.** In Funke's experiment, sliders lowered response rates (most on mobile) and increased response times; radio buttons had no such costs. A MeasuringU study found similar data quality but a 2-to-1 user preference for buttons.
- **Start position.** One study found no consistent default effect on 7-point sliders; another found clear anchoring. Buttons with no preselection avoid the question.
- **Required vs skip.** With all answers required, a person who cannot answer picks the middle, which looks like real data. A Skip link plus the 8-of-10 rule in Scoring keeps those non-answers out of the score.

**Mobile layout:** one item per screen or a short page of 3 items, each option at least 44 px tall, the label text inside the button, auto-advance after a tap, a Back control, and a progress line ("12 of 30").

## Reverse-scored items

Keep three reverse items per dimension, written as plain opposite behaviors without "not". The research does not support a fixed ratio, and your current items already use the safer form.

**Why they are used.** Weijters and Baumgartner list three gains: they offset yes-saying, they interrupt answers given without reading, and they cover the low end of a trait.

**What they cost.**

- **Confusion and misresponse.** Reverse items lower reliability and often split one trait into a "positive" and a "negative" factor. When 10% or more of people answer carelessly, this split shows clearly in the data.
- **Weak protection in practice.** A study of the MFI-20 fatigue scale found that 10 reverse items did not stop biased answers; a 10-item same-direction version gave fewer errors.
- **Real middle cases.** A person in the middle of a trait can honestly agree with both directions ("I'm not tall, but not short either"). Not every contradiction is an error.

**Do they help with yes-saying?** Partly. In the total score, they cancel some of it: with your 7 + 3 split, a person who picks the top answer on every item gets 70, not 100. A 5 + 5 split would cancel it fully (50). The frequency format already lowers yes-saying, so full balance matters less here.

**Is 7 + 3 sensible?** It is a common choice, not a rule. The IPIP 50-item Big Five scales range from 5 + 5 to 2 + 8 across factors. No study sets a best proportion. 7 + 3 is a reasonable default; 6 + 4 is equally defensible.

**How to write them.** Three forms exist (Baumgartner, Weijters and Pieters):

| Form | Example | Use? |
| --- | --- | --- |
| Negation | "I do not keep people close." | No — most misresponse |
| Polar opposite | "I keep people at a distance." | Yes |
| Opposite behavior in a situation | "When strong feelings come up, I go numb." | Yes — clearest |

Also match the intensity of positive items. A reverse item worded more extreme than its positive partner ("terrible" vs "good") tends to split off as its own factor.

**Optional check:** if a person picks the same answer on all 30 items, show a short note: "You chose the same answer for every item. Want to review before you see results?"

## Scoring

Your current algorithm is a correct, standard conversion: it is the "percent of maximum possible" (POMP) score from Cohen and colleagues. Keep the idea and change three details: use the mean so skips work, round to the nearest 5, and refuse a score when fewer than 8 items are answered.

```latex
\text{score} = \mathrm{round}_5\!\left( \frac{\bar{x} - 1}{4} \times 100 \right), \quad \bar{x} = \text{mean of the answered, reverse-scored items}
```

```javascript
const MIN_ANSWERED = 8;

function scoreDimension(items) {
  // items: [{ response: 1..5 | null, reverse: boolean }]
  const scored = items
    .filter(i => i.response !== null)
    .map(i => (i.reverse ? 6 - i.response : i.response));
  if (scored.length < MIN_ANSWERED) return null; // "not enough answers"
  const mean = scored.reduce((a, b) => a + b, 0) / scored.length;
  const pomp = ((mean - 1) / 4) * 100;
  return { mean, score: Math.round(pomp / 5) * 5 };
}
```

- **Equal weights.** Keep them. Other weights need data from many respondents to estimate. Without that data, equal weights are the standard choice.
- **Mean vs sum.** They give the same rank and the same POMP when nothing is skipped. The mean also stays on the 1–5 label scale, so it maps back to words.
- **Skips.** Averaging the answered items is "person-mean" scoring. Methodologists accept it when most items are present (about 80%, never under half) and the items behave alike. It can bias a score a little, so keep the floor at 8 of 10.
- **Precision.** Ten 5-point items give only 41 possible means, so the score moves in steps of 2.5. A self-report score also carries error. Rounding to 5 shows 21 levels, which is closer to what the answers support.
- **No tradeoffs between dimensions.** Score each dimension only from its own items. Never normalize across the three, rank them into a total, or show them as shares of a whole.

**Worked examples** (same patterns as your verified table, on the new scale):

| Pattern for one dimension | Scored items | Mean | Exact | Shown |
| --- | --- | --- | --- | --- |
| Positive 5, reverse 1 | ten 5s | 5.0 | 100 | 100 |
| Positive 4, reverse 2 | ten 4s | 4.0 | 75 | 75 |
| Every answer 5 (yes-saying) | seven 5s, three 1s | 3.8 | 70 | 70 |
| Every answer 3 | ten 3s | 3.0 | 50 | 50 |
| Every answer 1 | seven 1s, three 5s | 2.2 | 30 | 30 |
| Positive 1, reverse 5 | ten 1s | 1.0 | 0 | 0 |
| 9 answered: positive 4,4,4,5,5,3 + one skip; reverse 2,1,2 | 4,4,4,5,5,3,4,5,4 | 4.22 | 80.6 | 80 |
| 7 answered | — | — | — | "Not enough answers" |

## Results display

Lead each result with words from the scale the person used, show the number second, and show the score as a position on a bar. Score-reporting guidance (Hambleton and Zenisky) says to put the main takeaway first and state plainly that every score has error.

**Number format.** Show "75 / 100" or the bar alone. Avoid "75%": readers take a percent as a share or a percentile. Add one line under the bars: "Scores show how often you chose each answer. They do not compare you with other people."

**Phrase from the mean.** Round the dimension mean to the nearest 0.5:

| Mean (rounded) | Score (approx.) | Phrase |
| --- | --- | --- |
| 1.0 | 0 | Almost never |
| 1.5 | 10–15 | Between almost never and rarely |
| 2.0 | 25 | Rarely |
| 2.5 | 35–40 | Between rarely and sometimes |
| 3.0 | 50 | Sometimes |
| 3.5 | 60–65 | Between sometimes and often |
| 4.0 | 75 | Often |
| 4.5 | 85–90 | Between often and almost always |
| 5.0 | 100 | Almost always |

This also answers the "neutral = 50" question: 50 reads as "Sometimes", which is what the person chose.

**Bands (your names kept).** The 40 / 70 cuts are product choices with no tie to the scale. Anchor them to labels instead: Closed at 25 or below (Rarely or less), Open at 75 or above (Often or more), Mixed between. A score within 5 points of a cut shows "near the Mixed / Open line" instead of a hard label. This stops a 1-point change from flipping the word.

**Profiles.**

| Profile | Headline |
| --- | --- |
| All three 75+ | "All three centers are high right now." |
| All three 25 or below | "All three centers are low right now." No ranking. |
| All within 15 points | "Your three scores are close together." No highest or lowest named. |
| One 15+ points from both others | Name it: "Gut is lower than Head and Heart right now." |
| Two tied, one apart by 15+ | Name the one apart; treat the tied two as equal. |

- **"Weakest".** Always naming one implies a deficit even when the gap is noise. Name a dimension only on a 15+ point gap, and use "lower" or "less used right now", not "weakest". The 15-point threshold is my judgment (0.6 of one 25-point scale step); change it if you collect retest data.
- **Chart form.** Three horizontal bars on the same 0–100 axis, each starting at 0. Do not use a pie, a stacked bar, or a ranked list: those imply the scores share a fixed total. A radar chart is acceptable but exaggerates differences through area.
- **Precision.** Never show decimals. Show the number rounded to 5, or no number at all.

## Sources

**Questionnaire-design guidance**

- Krosnick & Presser (2010), [Question and Questionnaire Design](https://web.stanford.edu/dept/communication/faculty/krosnick/docs/2010/2010%20Handbook%20of%20Survey%20Research.pdf), Handbook of Survey Research — scale points, labeling, satisficing
- Imperial College London, [Best practice in questionnaire design](https://www.imperial.ac.uk/research-and-innovation/education-research/evaluation/tools-and-resources-for-evaluation/questionnaires/best-practice-in-questionnaire-design/) — avoid agree/disagree, label every point, items must apply to everyone
- Survey Practice, [Should I label all scale points or just the end points?](https://www.surveypractice.org/article/2956-should-i-label-all-scale-points-or-just-the-end-points-for-attitudinal-questions)

**Response format and scale length**

- Saris, Revilla, Krosnick & Shaeffer (2010), [Agree/disagree vs item-specific response options](https://ojs.ub.uni-konstanz.de/srm/article/view/2682), Survey Research Methods
- Revilla, Saris & Krosnick (2014), [Choosing the number of categories in agree–disagree scales](https://ideas.repec.org/a/sae/somere/v43y2014i1p73-97.html), Sociological Methods & Research
- Sturgis, Roberts & Smith (2014), [Middle alternatives revisited](https://researchonline.lse.ac.uk/id/eprint/101999) — the neither/nor midpoint as hidden "don't know"
- Kankaraš & Capecchi (2024), [Neither agree nor disagree](https://ideas.repec.org/a/spr/metron/v83y2025i1d10.1007_s40300-024-00276-5.html), METRON
- Laird et al. (2008), [How often is "often" revisited](https://purdue.edu/idata/documents/Laird-et-al-2008-vague-quantifiers.pdf) — vague quantifiers

**Sliders and controls**

- Funke (2016), [Negative effects of slider scales](https://journals.sagepub.com/doi/10.1177/0894439315575477), Social Science Computer Review
- Liu & Conrad, [Where should I start? Default values for slider questions](https://api.isr.umich.edu/?p=196977)
- MeasuringU, [Radio buttons vs sliders: preferences](https://measuringu.com/?p=29896)

**Reverse-keyed items**

- Weijters & Baumgartner (2012), [Misresponse to reversed and negated items: a review](https://pure.psu.edu/en/publications/misresponse-to-reversed-and-negated-items-in-surveys-a-review/), Journal of Marketing Research
- Baumgartner, Weijters & Pieters, [Misresponse framework: reversals, negations, polar opposites](https://research.tilburguniversity.edu/en/publications/misresponse-to-survey-questions-a-conceptual-framework-and-empiri/)
- van Sonderen et al. (2013), [Ineffectiveness of reverse wording](https://pmc.ncbi.nlm.nih.gov/articles/PMC3729568), PLoS ONE
- Zhang, Noor & Savalei (2016), [Reverse-worded items and the Need for Cognition scale](https://pmc.ncbi.nlm.nih.gov/articles/PMC4909292), PLoS ONE
- Suárez-Álvarez et al. (2018), [To reverse or not to reverse Likert-type items](https://www.psicothema.com/pdf/4582.pdf), Psicothema

**Scoring and missing items**

- Cohen, Cohen, Aiken & West (1999) POMP scores, as implemented in [R quest::pomp](https://search.r-project.org/CRAN/refmans/quest/html/pomp.html)
- Mazza, Enders & Ruehlman (2015), [Proration vs full-information estimation](https://pmc.ncbi.nlm.nih.gov/articles/PMC4701045)
- Bell et al. (2016), [Missing items in the HADS: the half rule](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5075158/)

**Results reporting**

- Center for Assessment, [Lead with the reports](https://www.nciea.org/blog/lead-with-the-reports/) — Hambleton's score-report practices

**Example instruments (method only)**

- [IPIP 50-item Big Five scale](https://ipip.ori.org/New_IPIP-50-item-scale.htm) — "as you generally are now, not as you wish to be"; keying ratios from 5 + 5 to 2 + 8
- [Self-Compassion Scale](https://www.testable.org/scale/scs-self-compassion-scale) — 5-point frequency scale (Almost never to Almost always), reverse-scored subscales, mean scoring
