Problem statement (real-world):
City transit authorities want to offer dynamic multi-modal fares and suggest transfer routes minimizing
cost and travel time for commuters. Given passenger origin-destination flows, route segments with capacities
and base fares, build a CLI tool to compute a suggested fare bundle and a simple route plan per OD pair.

This simplified prototype: reads routes, segments, OD demands, computes shortest-cost paths by combining time and fare,
applies capacity-aware scaling (penalize full segments), and outputs suggested combined fares and sample passenger assignment.

Input format:
First line: S (segments) R (routes) P (OD pairs)
Next S lines: segId from to time_minutes capacity base_fare
Next R lines: routeId K segId1 segId2 ... segIdK
Next P lines: origin dest passengers

Output: For each OD pair: chosen route (sequence of segments), estimated time, average fare, assigned passengers (limited by capacity scaling)


