# Introduction to Drone Request Scheduling
A drone request is a set of instructions that a consumer provides to a drone service provider and drone pilot.  The request may include an area on a map and explicit instruction of what the pilot should photograph.  An example [(ER1)](TODO) might include a [request](#request) for a drone to take aerial images of the guests at a wedding.  This example has a tightly constrained by the start and end time.  A request becomes a [mission](#mission) which has 1 flight.   Another example [(ER2)](TODO) might be a request for all the cell towers in Cook county to be inspected and photographed by the drone.    All the mission must be flown for this request by the by May 25, and should only be carried out on sunny days that have moderate to low wind (< 25 knots).  This request specifically  states that the images must be at least 12mb and should capture each cell and Microwave dish in full frame.  They should also include infrared images of all the equipment as well.  

The act of scheduling would assign both a drone and a pilot to a mission such that both the drone and the pilot's output would be maximized. A **schedule** would include the assigned pilot, drone and predicted start times, end times for each request/mission which would be a function of:

  1. The relative location of the request to the drones base
  2. The ability of a drone and a pilot (skills) which may include equipment like infrared camera as well as the pilots experience of a specific task like inspecting cell towers.
  3. The predicted weather for that operational area for that given day
  4. The cost of operation for a particular drone and pilot
  5. The time/cost to travel between assignments
  6. Plus future considerations

This is but a small sample set of constraints that may come into play with request scheduling.  A primary goal of this objective is to build a robust extensible platform that would allow us to add new parameters and constraints to the request scheduling.  See the first challenge [Scheduling Architecture Component Survey](challenges/schedulingArchitectureComponentSurvey.md) to see the first challenge where we will explore the components to built this scheduling tool.

---

## One proposed approach
Topcoder's mtwomey and kbowerma have drafted an approach to scheduling described by the image below and followed by a description of each of the scheduling components and test harness.

![](../img/schedulingApproach.svg)
