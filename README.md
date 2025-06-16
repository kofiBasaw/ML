# ML
Machine learning project
F1 DRIVERS: USE OF MACHINE LEARNING TECHNIQUES TO PREDICT WHETHER A DRIVER WILL FINISH THE RACE OR NOT.

EXPLANATION OF THE VARIABLES USED

### Race Information

•	raceId → Unique identifier for each race.

•	year → Year in which the race took place.

•	round → Round number of the race within the season.

•	circuitId → Unique identifier for the circuit.

•	circuit_name → Name of the circuit.

•	location → Location of the circuit.

•	country → Country where the race takes place.

•	date → Date of the race.

•	event_name → Official name of the event.
________________________________________
### Constructor (Team) Information

•	constructorId → Unique identifier for each constructor.

•	constructor_name → Name of the team.

•	position_constructors_championship → Constructors’ championship standing before the race.

•	constructor_qtimes_avg → Average of the best qualifying times of the two drivers on that circuit (performance indicator of the team on that track).

•	constructor_qtime_gap → Delay in qualifying (per race), calculated as the gap between the team's average best two times and the overall best average (the best team will have 0).
________________________________________
### Driver Information

•	driverId → Unique identifier for the driver.

•	driver_name → Abbreviated name of the driver.

•	nationality → Nationality of the driver.

•	age → Age of the driver in that race.

•	experience → Number of races completed before that race.
________________________________________
### Race Performance

•	grid → Starting grid position.

•	prevraces_positiondiff → Median difference between starting and final position over the previous 5 races. If fewer than 5 races are available, use those (nulls correspond to drivers debuting in F1).

•	q1_gap → Best lap time in Q1 of qualifying of the driver (null if the driver didn’t complete a lap in Q1) as delay from the best one.

•	championship_points_before_race → Championship points before the race (for the first race of the year, use the final standings from the previous year).

•	position_driver_championship → Driver’s position in the championship standings before that race.
________________________________________
### Incidents and Retirements

•	is_crash → 1 if the driver retired due to crash, 0 if not

•	totcrashes_in_circuit → Number of crashes on that circuit by the driver in past races (null if it's the first race on that circuit).

•	totraces_in_circuit → Number of races completed on that circuit by the driver before the current one (same null condition).

•	%crash_in_circuit → Crash frequency of the driver on that circuit (total_crashes / total_races) (same null condition).

•	laplace_crash_in_circuit → Crash frequency of the driver with Laplace smoothing ((total_crashes + 1) / (total_races + 2)) (same null condition).

•	recent%crashes → Percentage of races not finished due to crashes in the previous 5 races. If fewer than 5 are available, use those (null in the first race of each season + debuts mid-season).

•	recent_laplace_crashes → Crash percentage with Laplace smoothing in the last 5 races (same null condition).

•	recent_laplace_mechproblems → The probability of experiencing mechanical issues in a given race, computed as the Laplace-smoothed average of the previous 5 races. Helps track the frequency or severity of mechanical failures (null in the first race of each season).

•	historical_%crashes_circuit → Historical percentage of crash-related retirements on that circuit (null for new circuits).

•	historical_%mechproblems_circuit → Historical percentage of retirements due to mechanical issues on that circuit (null for new circuits).

•	mechanical_problems → 1 if the driver retired due to mechanical problems, 0 otherwise.

•	retirement_target → 1 if the driver did not finish the race, 0 if they completed it.
________________________________________
###  Weather and Circuit Conditions

•	alt → Altitude of the circuit.

•	n_corners → Number of corners on the circuit.

•	air_temperature → Average air temperature during the race.

•	air_temperature_range → Difference between the maximum and minimum air temperatures during the race.

•	track_temperature → Average track temperature during the race.

•	track_temperature_range → Difference between the maximum and minimum track temperatures during the race.

•	atmospheric_pressure → Average atmospheric pressure during the race.

•	%rainfall → Percentage of laps driven in wet conditions during the race.
•	atmospheric_conditions → Weather conditions for the race (wet/dry).
•	wind_speed → Wind speed during the race.

