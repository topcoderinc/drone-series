# Phase 2B

## Introduction to Phase 2B
The next phase Drone Series, which we are calling 2b,  will begin at the end of February 2017 and run through May.   This Phase has three primary objectives.

 1. Drone request Scheduling
 2. Fleet Management
 3. Data (flight log) retrieval, parsing and storage

 Some of these objectives will build on the previous phase front-end and back-end and others will be new

### Drone Request Scheduling
A drone request is a set of instructions that a consumer provides to a drone service provider and drone pilot.  The request may include and area on a map and explicit instruction of what the pilot should photograph.  An example [(ER1)](TODO) might include a [request](#request) for a drone to take ariel images of a wedding.  This example has a tightly constrained start and end time.  This request becomes a [mission](#mission) which has 1 flight.  Another example [(ER2)](TODO) might be a request for all the cell towers in Cook county to be inspected and photographed by the drone.   All the mission for this request must be completed by the by May 25 and should only be carried out on sunny days that have moderate to low wind (< 25 knots).  This request specifically  states that the images must be at least 12mb and they should also include infrared images.  The act of scheduling would include a which assignments each drone and pilot should execute on a given day.  It would include the assigned pilot, drone and predicted start times, end times for each request/mission which would be a function of:

  1. The relative location of the request to the drones base.
  2. The ability of a drone and a pilot (skills) which may include equipment like infrared camera as well as the pilots experience of a specific task like inspecting cell towers.  
  3. The predicted weather for that operational area for that given day.
  4. The cost of operation for a particular drone and pilot
  5. The time/cost to travel between assignments

This is but a small sample set of constraints that may come into play with request scheduling.  A primary goal of this objective is to build a robust extensible platform that would allow us to add new parameters and constraints to the request scheduling.  See the first challenge [Scheduling Architecture Component Survey](challenges/schedulingArchitectureComponentSurvey.md) to see the first challenge where we will explore the components to built this scheduling tool.




### Fleet Management


### Data (flight log) retrieval, parsing and storage

## [Previous Phase output summary and features](dsp/phase2Features.md)


## Definitions
### request
An artifact created by a consumer (customer) for the purpose of exchanging drone services which maybe in the form of imagery or delivery.  A request may have one or more missions.
### mission
The result of a request after a pilot or operator has plotted a course to be flown and have assigned a drone and a pilot.   A mission should only have one request but may have one or more flights.
### flight
