# AI Feature Specification: Smart Seat Recommendation

## Problem It Solves
Problem 5: Confusing availability labels (WL/RAC)

## Proposed Feature — User Perspective
User sees “Recommended Train” based on highest confirmation probability.

## Model or API Choice
OpenAI GPT-4 / simple ML classifier

## Training or Input Data
- Historical booking data
- Seat confirmation rates

## How Output Is Shown to the User
Label: "90% chance of confirmation"

## Confidence Threshold and Fallback
If confidence < 60% → show normal data

## Success Metrics
- Increase bookings
- Reduce confusion

## Limitations and Risks
- Wrong prediction → user trust loss