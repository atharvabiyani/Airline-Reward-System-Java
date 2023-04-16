# Airline-Reward-System

Northeast Airlines Rewards Program:
This repository contains the code for the Northeast Airlines Rewards Program, which is a program that calculates the rewards for its passengers based on their flight miles and flight cancellations.

Project Specification:
The rewards program is based on the miles flown within the span of a year, which itself is based on the number of cancelled flights. Flight miles and flight cancellations start to accumulate on January 1, and end on December 31.

The following describes the reward tiers, based on miles earned / flights cancelled within a single year:

Gold – 25 flight cancellations. Each cancellation is worth 1000 miles.
Platinum – 50 flight cancellations. Each cancellation is worth 1000 miles.
Platinum Pro – A special sub-tier of Platinum, reserved for those passengers with the mileage multiplier. This will earn double the miles per cancelled flight (2000 miles) for passengers who did not complain about flight cancellations at all throughout the year.
Executive Platinum – 100 flight cancellations. Each cancellation is worth 1000 miles.
Super Executive Platinum – A special sub-tier of Executive Platinum, reserved for those passengers with the mileage multiplier. This will earn double the miles per cancelled flight (2000 miles) for passengers who did not complain about flight cancellations at all throughout the year.
For each passenger, the program calculates the tier based on the span of an entire year (assume all flight data is for one year only). The tier that a passenger belongs to is updated in real-time as a flight is cancelled.

There is a class for each reward tier and use inheritance to create a class hierarchy, starting with a base class called Tier, which is either abstract or an interface. Every tier class should support the following methods:

public int getMiles() – Returns the miles earned so far.
public int getCancelledFlights() – Returns the current number of flights the passenger was supposed to take but which were cancelled.
public int getFlights() – Returns the current total number of flights the passenger took, including cancelled flights.
public void addFlight(boolean isCancelled) – Adds a new flight. Assume each call to addFlight adds a single flight. The parameter, isCancelled, will be true if the flight was cancelled.

There is a class called Passenger, which represents a Northeast Airlines passenger. It will have a private field of type Tier, which stores a reference to the passenger’s current reward tier. The Passenger class should implement the following methods:

public String getTier() – Returns (as a String) the name of the tier the passenger belongs to.
public int getMiles() – Returns the miles earned over the year. This method will simply return the miles from the Tier object (the private field mentioned above), by calling its getMiles method. This is a form of composition (we are using both composition and inheritance in this project).
public int getCancelledFlights() – Returns the number of flights the passenger was supposed to take but which were cancelled. As with getMiles, this method will simply return the number of cancelled flights from the Tier object.
public boolean hasMultiplier() – Returns true if the passenger has the mileage multiplier. This will return false until the end of the year, at which point a determination can be made as to whether the passenger earned the mileage multiplier.
public void addFlight(boolean isCancelled) – Adds a new flight. This method will call the same method in the Tier object. This method may also be a good place to determine if a passenger needs a tier upgrade.

File Input:
The program will input passenger and flight data, in chronological order, from a file called `flight-data.txt'
