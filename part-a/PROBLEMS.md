## Problem 1: Tatkal Booking Crashes at 10:00 AM [Given]

**What is broken:**
System becomes unresponsive during Tatkal opening. No queue or feedback.

**Affected users:**
High urgency users booking Tatkal (~lakhs daily)

**Frequency:**
Daily at 10 AM

**Current flow — step by step:**
1. User opens IRCTC at 9:50 AM
2. Logs in
3. Searches train
4. Selects Tatkal quota
5. Fills passenger details
6. Clicks Book at 10:00 AM
7. Page freezes / times out
8. Reload → quota gone

**Where exactly it breaks:**
Step 6 → server overload, no queue handling

## Problem 2: Search Filters Do Not Work Reliably [Given]

**What is broken:**
Filters don’t consistently update results or persist.

**Affected users:**
All users searching trains

**Frequency:**
Very frequent

**Current flow — step by step:**
1. User searches trains
2. Results load
3. Applies filter (Sleeper)
4. Results partially change / don’t change
5. Click train → go back
6. Filter resets
7. User re-applies filters

**Where exactly it breaks:**
Step 4 → UI not synced with backend filtering

## Problem 3: Seat Selection Resets [Given]

**What is broken:**
Selected seat preference not retained

**Affected users:**
Users with berth preference (elderly, families)

**Frequency:**
Common (more on mobile)

**Current flow — step by step:**
1. User searches train
2. Selects train
3. Enters passenger details
4. Selects berth (Lower)
5. Clicks Proceed
6. Moves to next page
7. Seat preference missing/reset

**Where exactly it breaks:**
Step 5 → data not persisted to next page