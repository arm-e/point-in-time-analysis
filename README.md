**Problem**: from the time a creator is contacted to the time their campaign runs, over time, this difference between first contact and final sales has grown.

**Goal**: the goal of this repo is to organize dashboards for stakeholders to better assess the time differences at different levels.

Departments involved:

- Sales: individuals that first contact creators
- Contract: once a creator is willing to participate, a contarct is signed
- Design: designers create the plushy design
- Manufacturing: an initial plushy is sent to the creator
- Campaign: once the creator is satisfied with the plushy, a 21-day campaign begins

For each level, a dashboard should be made to give insight into the time it takes for each sub-level (i.e., employee/manufacturing process to complete it's steps).
For example, in sales, there may be 20 creators being contacted in a given week, but it is important to understand the workload distribution and the rate at which
individual employees complete their steps. This gives an indication of productivity on an employee level and on the level of the department.

# Point-in-time analytics

The best way to track changes when we have a (start date, end date) would be to follow a point-in-time approach which takes a range of days and splits
it into day-to-day view of the data. 

**Columns for stratification:**

- Creator: creator involved
- Employee: employee assisting creator
- Department: department the employee belongs to
- Report date: day of tracking

**Columns for reporting:**

- Initiated contact: did the employee begin working for that creator that day (did they open a ticket w/ the creator) (0/1)
- Is ticket open: is the employee still working on that creator ticket (0/1)
- Ticket age: how old the ticket is in days
- Ticket closed: if the ticket closed (0/1) -- If initialized contact && open contact are 0, then this should be 1 and vice-versa
- Days to close: days to close the ticket -- If initialized contact && open contact are 0, then this should be >= 1, otherwise None

# Dashboarding

Using the point-in-time oriented data, we can begin to generate dashboards to visualize the time it takes for departments and employees to complete tickets at different time periods.

YouTube videos of dashboards (for vid controls):
- Overview: https://youtu.be/TW-MIFdJ0CQ
- Employees: https://youtu.be/uDGv2lcI66I

![overview](https://user-images.githubusercontent.com/121126300/212743444-762dc62e-516f-4d08-ab05-c7346c1d67f8.gif)


![departments](https://user-images.githubusercontent.com/121126300/212741289-a111b0bc-3e2a-490b-994e-f3ed9d9d4324.gif)

# Directories

- `intermediates`: randomly generated datasets (created via `generate_data.ipynb`)
- `out`: point-in-time table used for dashboarding (created via `get_views.ipynb`)
