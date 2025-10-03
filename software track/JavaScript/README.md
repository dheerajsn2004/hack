Problem statement (real-world):
Smart homes want to schedule flexible loads (washing machine, EV charging, battery charging) to minimize
energy cost while respecting user comfort windows and grid constraints (peak demand limits). This CLI app
reads device jobs with earliest/latest start and duration, electricity price timeline, and produces a feasible schedule that minimizes cost using a greedy shifting heuristic.

Input format (JSON via stdin): {
  "prices": [0.12, 0.15, ...], // hourly price for next 24 hours
  "peak_limit": 5.0, // kW
  "jobs": [ {"id":"EV","power":3.5,"dur":4,"earliest":0,"latest":23}, ... ]
}
Output: schedule for each job: start_hour, end_hour, estimated cost


