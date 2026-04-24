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

## Problem 4: Pages Load Extremely Slowly

**How I found it:**
While searching trains

**What is broken:**
High latency, pages take long to load

**Affected users:**
All users on peak hours

**Frequency:**
Frequent

**Current flow — step by step:**
1. User searches trains
2. Clicks search
3. Loading screen appears
4. Waits 10–20 seconds
5. Sometimes timeout
6. Refresh required

**Where exactly it breaks:**
Step 3 → backend response delay

**Screenshot/Description:**
Train search loading screen with delay

## Problem 5: Confusing Train Availability Labels

**How I found it:**
Checking availability

**What is broken:**
Labels like WL, RAC unclear

**Affected users:**
New users

**Frequency:**
Always

**Current flow — step by step:**
1. User searches trains
2. Views availability
3. Sees WL/RAC
4. Doesn’t understand meaning
5. Hesitates to book
6. Leaves platform

**Where exactly it breaks:**
Step 3 → poor UX communication

**Screenshot/Description:**
Availability column with WL/RAC

## Problem 6: Poor Mobile Web Experience

**How I found it:**
Opened IRCTC on mobile browser

**What is broken:**
UI not responsive, hard to use

**Affected users:**
Mobile users

**Frequency:**
Always

**Current flow — step by step:**
1. User opens IRCTC on mobile
2. Homepage loads
3. Elements overlap
4. Buttons small
5. Hard to navigate
6. Booking becomes difficult

**Where exactly it breaks:**
Step 3 → non-responsive design

**Screenshot/Description:**
Overlapping UI elements on mobile