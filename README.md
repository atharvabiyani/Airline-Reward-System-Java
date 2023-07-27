<h1>Northeast Airlines Reward Program Project ✈️</h1>
<img src='https://media.tenor.com/mL7suP22MNwAAAAM/plane-flying.gif' alt='Flying Plane Image'>

This academic project is a Java program that calculates the rewards for its passengers based on their flight miles and flight cancellations. 


<h1>Project Specification 🔎</h1>
<h3>Background: </h3>

- The rewards program is based on the miles flown within the span of a year, which itself is based on the number of cancelled flights. Flight miles and flight cancellations start to accumulate on January 1, and end on December 31.

<h3>Reward tiers, based on miles earned / flights cancelled within a single year:</h3>

- Gold – 25 flight cancellations. Each cancellation is worth 1000 miles.
- Platinum – 50 flight cancellations. Each cancellation is worth 1000 miles.
- Platinum Pro – A special sub-tier of Platinum, reserved for those passengers with the mileage multiplier. This will earn double the miles per cancelled flight (2000 miles) for passengers who did not complain about flight cancellations at all throughout the year.
- Executive Platinum – 100 flight cancellations. Each cancellation is worth 1000 miles.
- Super Executive Platinum – A special sub-tier of Executive Platinum, reserved for those passengers with the mileage multiplier. This will earn double the miles per cancelled flight (2000 miles) for passengers who did not complain about flight cancellations at all throughout the year.

<h3>Inheritance:</h3>

- There is a class for each reward tier and inheritance is used to create a class hierarchy, starting with a base class called Tier, which is either abstract or an interface.

<h3>File Input:</h3>

- The program will input passenger and flight data, in chronological order, from a file called 'flight-data.txt'
