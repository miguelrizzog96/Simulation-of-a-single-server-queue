# Discrete Event Simulation of a Queue Using Python. 
*Written by: Miguel Angel Rizzo Gonzalez*
![](https://user-images.githubusercontent.com/69512046/93006624-747df780-f52c-11ea-9b3a-8e0f97714b87.jpg)

##  Project Overview: 
- **Generated a Simulation model that outputs the performance measures, such as average length, average waiting time, utilization of the system, etc. to provide information for designing or improving service facilities.**
- **Showed that using this approach, system changes and different layouts can be tested without actually having to carry them out physically.**
- **Simulated over 1000 customer arrivals and departures using Python.**


 ## Code walkthrough 
 [https://github.com/miguelrizzog96/Queue_analisis_using_simluation/blob/master/server.ipynb](https://github.com/miguelrizzog96/Queue_analisis_using_simluation/blob/master/server.ipynb)

## Why Study Queues?
Waiting to be attended is part of daily life. We wait in restaurants, we do a
line to board a plane, and we stand in line to be served at
official dependencies. The phenomenon of waiting is not limited to human beings:
jobs wait to be processed, planes fly in circles at different heights
until they are allowed to land, and the cars stop at traffic lights. Deleting the
waiting entirely is not a feasible option because the cost of installation and
operation of the operation center can be prohibitive. Our only recourse is to search
the balance between the cost of offering a service and the cost of waiting for it to be served.
Queue analysis is the vehicle to achieve this goal.*(Taha,H.)* 


## How does it work?
At its core, a queuing situation involves two parts.

1. Someone or something that requests a service—usually referred to as the customer, job, or request.
2. Someone or something that completes or delivers the services—usually referred to as the server.

 Consider this Example: A filling station that has two dispensers. Cars arrive about every 5 minutes on average according to a Poisson process, this means that the average time between events is known, but the exact timing of events is random. The average time it takes to fill a car is 3 minutes, also a Poisson process. These rates often are actually modeled from actual data to get accurate results. When a car enters the facility, and at least a station is idle, they enter the system. if not they wait in line until a station becomes available, as it can be seen on the following diagram:


![](https://user-images.githubusercontent.com/69512046/94444662-8c808880-0174-11eb-8706-e05c9b4b7eed.JPG)


## Which data do we need?
- λ: the arrival rate (the expected number of consecutive arrivals per the same unit time, e.g. 1 minute)
- μ: the service rate (the expected number of consecutive service completions per the same unit time, e.g. 1 minute)
- the distribution of the data
- c: the number of servers


## Data Visualization

Here are the distributions of the data and the value counts for other variables like occupation and number of customers in an example model. Below are a few key points of the corresponding system.


![Figure 2020-09-17 074636 (1)](https://user-images.githubusercontent.com/69512046/99907675-87dbda80-2cb4-11eb-8bd9-431acfcdf26a.png)

![Figure 2020-09-17 074636 (2)](https://user-images.githubusercontent.com/69512046/99907674-86aaad80-2cb4-11eb-9469-1a2fdd2651f6.png)

![Figure 2020-09-17 074636 (3)](https://user-images.githubusercontent.com/69512046/99907672-86121700-2cb4-11eb-994c-aa76205650cf.png)

![Figure 2020-10-19 084256](https://user-images.githubusercontent.com/69512046/99907671-84e0ea00-2cb4-11eb-9da5-47c03c67d5db.png)

| Example Output:                 |          | 
| ----------- | ----------- |
|  Time Between Arrivals (minutes):  | 1.0108  |
| Service Time (minutes):            |  0.6494  |        
| Utilization:             |  0.6418  |
|  Expected wait time in line (Wq) (minutes):|    1.5845 |  
|  Expected number of customers in line (Lq):|   1.5673 |  
|   Expected number of clients in the system (Ls): |  2.2092 |  
|   Expected time spent on the system (Ws) (minutes):|   2.2338 |  

## Model Development Steps
Using Python 3.7.6:

Parameters used for reference: λ = 1 (Poisson) , μ = 1.5 (Poisson) , c = 1 , n=1000

- Generated arrival and service times with random number generation using the python library `numpy`
- Generated lists and dataframes with conditional statements to represent the events ocurring in the queue
- Used the generated model for simulating a multiple server queue with n customers
- Generate the output for a range from 1 servers to n numbers of servers




