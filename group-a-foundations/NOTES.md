# Group A - Exercise 1: Branch Performance Check

## Syntax learned
- Variables: text needs quotes ('like this'), numbers don't
- Arithmetic operators: - and / for calculations
- Comparison operator: > for checking conditions
- if / elif / else: decision logic, needs a colon (:) and indentation
- f-strings: f'...{variable}...' to insert values into text
- Format specifier :.1% — converts a decimal to a percentage
  (multiplies by 100, adds %, rounds to 1 decimal place)

## Business terms
- Revenue: total money in from sales, before costs
- Cost / COGS: what it cost to generate that revenue
- Profit: Revenue - Cost
- Profit Margin: Profit as a % of Revenue
  Why it matters: raw profit doesn't show efficiency — margin lets you
  compare branches of different sizes fairly
- Rating/Tiering: turning a raw number into a judgment label
  (Excellent / Good / Needs Improvement) so it's easy to scan quickly

## What tripped me up
- Forgot that both single (') and double (") quotes work the same way
  in Python — thought there was a difference, there isn't
- Without any quotes, Python treats a word as a variable name, not text
  (e.g. rating = excellent looks for a variable called excellent,
  and errors if it doesn't exist)
- Tested a case where cost was much higher than revenue — got a
  large negative margin (-511.8%). Learned that negative margin
  means the branch lost money (cost > revenue), and it's worth
  checking raw revenue/cost values before trusting a surprising
  final result
- Was unsure why we divide by revenue instead of just using
  (revenue - cost) — realized raw profit alone isn't comparable
  across branches of different sizes, margin is

## Status
Code tested and working (including edge case with negative margin).
Ready — moving to Exercise 2.


# Group A - Exercise 2: Customer Tier Check

## Syntax learned
- Same if/elif/else + f-string pattern as Exercise 1, applied to a
  new scenario (spend amount instead of profit margin)
- Reinforced: every if / elif / else line needs a colon (:) at the end

## Business terms
- Spend-based tiering: unlike profit margin (a ratio), this tier is
  based on a raw currency amount — common pattern in loyalty
  programs and CRM systems (e.g. Gold/Silver/Bronze membership tiers)

## What tripped me up
- Wrote numbers with commas (35,000) thinking it was just formatting,
  like how humans write large numbers. In Python, a comma inside a
  number creates a completely different data type (a tuple) instead
  of a single number — caused the comparisons to break.
  Fix: never use commas when writing a number in code (35000, not 35,000)
- Forgot the colon (:) after `else` — only had it on `if` and `elif`.
  Every if/elif/else line needs a colon, no exceptions.
- Note: I customized the tier names ('Golden tier 1', 'silver tier 2',
  'bronze tier 3') instead of the original plain Gold/Silver/Bronze —
  intentional change, not a bug, just personalizing the output.

## Status
Code tested and working — spend of 35000 correctly returned 'silver tier 2'.
Group A complete (Exercise 1 + Exercise 2 both done).
