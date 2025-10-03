Problem statement (real-world):
During natural disasters, aid agencies must allocate limited resources (food, water, medical kits)
across affected zones. Each zone has a severity score and a population; travel time between hubs
and zones influences delivery schedules. Design a CLI app that accepts resources inventory,
zone demands, and travel penalties and produces a prioritized allocation plan and simple route batches.

This is a simplified, single-run simulator focusing on greedy optimization + heuristics (not full MILP).

Input:
- First line: R (number of resource types) N (number of zones)
- Next R lines: resource_name total_quantity
- Next N lines: zone_name population severity_score (1-10) travel_penalty (hours)
- Next line: M (number of resource demands)
- Next M lines: zone_name resource_name requested_quantity

Output: allocation per (zone, resource) and summary of unmet demand and suggestions.

Sample input:
3 3
Food 1000
Water 800
MedKit 200
ZoneA 5000 8 4
ZoneB 2000 6 2
ZoneC 700 9 6
6
ZoneA Food 600
ZoneA Water 400
ZoneB Food 300
ZoneB MedKit 50
ZoneC Food 500
ZoneC MedKit 120

Sample output: (human readable allocation table)



