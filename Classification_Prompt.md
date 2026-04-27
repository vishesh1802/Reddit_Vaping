You are analyzing a social media post about vaping cessation.
Classify the post using a step-by-step decision process:

STEP 1: Determine if the user is ALREADY QUITTING
- YES (already quitting): The person has recently started quitting (within past 2 months) OR has been vape-free for 3+ months. Look for: active steps (reducing use, avoiding triggers, tracking days quit, discarding devices, using quit aids) OR long-term maintenance (vape-free for months, preventing relapse, reflecting on progress).
- NO (not yet quitting): The person is still vaping or has not started the quitting process.

STEP 2: If NOT already quitting, determine if they have a CONCRETE PLAN
- YES (concrete plan): The person discusses specific plans, quit dates, strategies, coping methods, OR asks for help about specific barriers (e.g., living with a vaping partner, working in a vape shop, environmental triggers).
- NO (no concrete plan): The person recognizes vaping may be a problem and is thinking about quitting, but has NOT begun planning or forming concrete strategies.

STEP 3: Apply decision rules
- If already quitting AND started within last 2 months (look for: "day X", "week X", "just quit", "recently stopped") → ACTION
- If already quitting AND vape-free for 3+ months (look for: "months", "long time", "since [month/year]", "6 months", "year") → MAINTENANCE
- If NOT already quitting AND has concrete plan → PREPARATION
- If NOT already quitting AND no concrete plan → CONTEMPLATION
- If person does NOT see vaping as a problem, is not thinking about quitting, or shows no intention to change → PRECONTEMPLATION

IMPORTANT DISTINCTIONS:
- CONTEMPLATION vs PREPARATION:
  * CONTEMPLATION: "thinking about", "considering", "maybe", "not sure", "wondering"
  * PREPARATION: "decided to", "planning to", "quit date", "strategy", "bought [aid]", "set a date"
  
- ACTION vs PREPARATION:
  * PREPARATION: Future tense ("will quit", "planning to", "going to")
  * ACTION: Present/past tense ("quit", "stopped", "day X", "using [aid]", "currently")
  
- ACTION vs MAINTENANCE:
  * ACTION: Recent timeframe ("days", "weeks", "just", "recently", "2 months")
  * MAINTENANCE: Extended timeframe ("3+ months", "long time", "since [date]", "half a year")
  
- PRECONTEMPLATION vs CONTEMPLATION:
  * PRECONTEMPLATION: Explicit denial ("don't see problem", "not bad", "no intention", "not thinking about it")
  * CONTEMPLATION: Any awareness of problem, even if uncertain

EXAMPLES:

Example 1 (CONTEMPLATION):
Post: "I've been thinking about quitting vaping. It's expensive and I know it's bad for me, but I'm not sure how to start."
Decision: Not quitting (NO) → No concrete plan (NO) → CONTEMPLATION
Evidence: "thinking about", "not sure how to start"

Example 2 (PREPARATION):
Post: "I've decided to quit next Monday. I bought nicotine patches and told my roommate to hide my vape."
Decision: Not quitting (NO) → Has concrete plan (YES) → PREPARATION
Evidence: "decided to quit", "quit date (Monday)", "bought patches"

Example 3 (ACTION):
Post: "Day 3 without vaping! Using gum to help with cravings. It's tough but I'm doing it."
Decision: Already quitting (YES) → Recently started (within 2 months) → ACTION
Evidence: "Day 3", "without vaping", "using gum"

Example 4 (MAINTENANCE):
Post: "6 months vape-free! Still get cravings sometimes but staying strong. Never going back."
Decision: Already quitting (YES) → Multiple months (3+) → MAINTENANCE
Evidence: "6 months vape-free", "still get cravings"

Example 5 (PRECONTEMPLATION):
Post: "I don't see what's wrong with vaping. It's not that bad compared to smoking. I'm fine with it."
Decision: No intention to change, explicit denial → PRECONTEMPLATION
Evidence: "don't see what's wrong", "not that bad", "fine with it"

Post to classify:
{post_text}

Return ONLY valid JSON (no markdown, no extra text) with exactly these keys:
- "is_already_quitting": boolean (true if user has started quitting or is maintaining)
- "has_concrete_plan": boolean (true if user has specific plans/strategies, only relevant if not already quitting)
- "stage": one of ["PRECONTEMPLATION","CONTEMPLATION","PREPARATION","ACTION","MAINTENANCE"]
- "explanation": a brief one-sentence justification for why this stage was chosen
- "evidence": an array of up to 2 short quoted snippets from the post that support this stage classification
