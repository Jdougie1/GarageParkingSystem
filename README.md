This code implements a combined garage management system that integrates three main functionalities:

Parking System:

It manages multiple garages and registered vehicles.
Garages have a name, capacity, and a list of parked vehicles.
Vehicles are registered with a license plate and an owner's name.
Commands allow you to park vehicles, remove them, relocate them between garages, resize garages, register new vehicles, generate a utilization report, and count the total number of parked vehicles.
Fine Management:

It uses a Binary Search Tree (BST) to track fines for vehicle owners.
Each node in the BST contains an owner’s name and their total fine amount.
Commands let you add fines, deduct fines (with removal when the fine reaches zero or less), search for an owner’s fine, calculate the average fine, check the height balance of the BST, and compute the total fines for owners with names below a given value.
Garage Sorting:

It sorts the list of garages by their names using merge sort with an insertion sort fallback for small subarrays.
The sorted list (garage name and capacity) is then printed out when requested.
Input Format:

The first line contains three integers:
g: number of garages
v: number of registered vehicles
c: number of commands
The next g lines provide each garage's name and total capacity.
The following v lines provide the license plate and owner name for each registered vehicle.
The remaining c lines are commands that operate on the system.
Supported Commands Include:

PARK <LP> <G>: Park a vehicle with license plate <LP> into garage <G>.
UTILIZATION_REPORT: Print each garage’s capacity, current occupancy, utilization percentage, and the least utilized garage.
RESIZE <G> <nc>: Change the capacity of garage <G> to <nc>.
SEARCH_OWNER <OWNER>: List all vehicles for <OWNER>, showing the garage each is parked in (or "NOT ON CAMPUS" if not parked).
RELOCATE <LP> <G>: Move the vehicle with license plate <LP> to garage <G>.
COUNT_TOTAL: Print the total number of parked vehicles.
REGISTER_VEHICLE <LP> <OWNER>: Register a new vehicle.
REMOVE_VEHICLE_GARAGE <LP>: Remove a vehicle from its current garage.
REMOVE_GARAGE <G>: Remove a garage from the system.
SORT_GARAGES <t>: Sort all garages by name using merge sort with threshold <t> and print the sorted list.
FINE_ADD <OWNER> <fine>: Add a fine amount for <OWNER>.
FINE_DEDUCT <OWNER> <fine>: Deduct a fine from <OWNER>, removing the owner if the fine becomes too low.
FINE_SEARCH <OWNER>: Search and display the fine and BST depth for <OWNER>.
FINE_AVERAGE: Display the average fine across all owners.
FINE_HEIGHT_BALANCE: Display the heights of the left and right subtrees of the fine BST.
FINE_CALC_BELOW <OWNER>: Compute the total fines for all owners with names less than or equal to <OWNER>.
