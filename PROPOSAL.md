# Portland Recreational Route Finder
## Research Question
Design a program that creates running/walking routes in Portland, Maine. These routes will be geared twords minimizing street crossing within the constrain of a given distance the user would like to go and a start/end position. The creation of such a program is important becasue it facilitates safe recreating. Additionally, I am unaware of any route planning tool that explicitly takes street crossings into consideration. 

## Algorithm 
This project will use a graph algorithm. Given the goal of the program, the algorithm will need to maximize edge/edge weights (street length) and minimize nodes (intersections). I haven't chosen a specific algorthm yet and need to do more research.  

## Data Plan
I plan to use the python package OSMNx, which pulls street data from OpenStreetMap. OpenStreetMap is free and publically availible. This will then be turned into a graph for analysis. I will start on a small subsection of the city to get the basic program working before expanding to the larger map. 

## Success Criteria
Success for this project will look like generated routes on a map. One way to check if the program is effective is for me to chose a starting point in the city and try to design a route of a certain length that minimzes street crossing by hand, and then compare it to what my program suggests. Another test would be to use a tool like Strava (which is a popular fitness app) to suggest a route (usually based on user data) of a certain length, and then compare the number of street crossings to what my program suggests.  

## Pitfall Scan

- Street data
    - Not all roads are navigable to pedestrians
    - The raw street data will need to be edited to fit the scope of this project
- Complexity
    - As route lengths get longer, route posibilites increase a lot. Also, wether you cross a street at a node depends on the direction you came from, the direction you leave, and the side of the street you are on
- Tools/Setup
    - This project relies heavily on importing street data using a python package. If I run into issues with the package it could derail the project
    - I plan to start early on importing data

## Repo Structure
- Root
    - license
    - gitignore
    - environment.yml
    - scripts
        - main
        - helpers
    - data
        - raw
            - street data
        - processed
            - graph data 
    

