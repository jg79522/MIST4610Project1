# MIST4610Project1

## Team Name:
59925 Group 1

## Team Members:
1. Jacob Greenwald [@jg79522](https://github.com/jg79522)
2. Iliana Venegas [@imv2ven](https://github.com/imv2ven)
3. Alexa Persad [@aepersad](https://github.com/aepersad)
4. Allison Chaloupek [@allisonchaloupek](https://github.com/allisonchaloupek)
5. David Breen [@davidbreen23](https://github.com/davidbreen23)

## Problem Description:
The task at hand is to model and build a relational database for the general operations of a film production company network. The central entity in the model is the ProductionCompany entity, which represents each studio that finances, manages, and oversees film projects. Each production company works collaboratively with agents, actors, crew members, and distribution partners to bring movies from concept to release. The model captures the company’s relationships with agents and contracts, which govern talent representation and project negotiations. It also tracks movies, their filming locations, and production sites, as well as assignments connecting crew members and personnel to those sites. Beyond production, the model reflects the distribution side of operations, linking movies to theaters and corresponding revenue reports that provide insight into financial performance. We will accurately model these relationships, generate sample data, and populate the entities with representative information. We will also perform functioning queries on this data so they may yield valuable business insights into the film production process, such as tracking movie profitability, analyzing agent partnerships, and evaluating personnel and site utilization across projects.

## Data Model:
Our model represents the structure of a hypothetical film production network that captures how production companies, agents, personnel, and partners interact throughout the filmmaking process.

At the top level, the ProductionCompany entity represents different studios that oversee and finance film projects. Each production company works with multiple Agents to secure talent, negotiate agreements, and manage contracts. Similarly, each agent can work with several production companies at once. This many-to-many relationship between ProductionCompany and Agent is represented by the Contract entity, which serves as an associative entity containing details such as compensation, start dates, and end dates.

Each Agent manages multiple Persons, including actors, directors, and technical staff, establishing a one-to-many relationship between Agent and Person. Every Person can be assigned to various ProductionSites, and each ProductionSite can host multiple people working on different aspects of a film. This many-to-many relationship between Person and ProductionSite is represented by the Assignment entity, which serves as the associative table. The Assignment entity stores key details such as department, assignment ID, and start and end dates.

The Movie entity is central to the model. Each Movie can be filmed at several Locations, and each location can host multiple movies, creating a many-to-many relationship represented by the ProductionSite associative entity. The ProductionSite table includes information about the filming location name, the site permit, and the start and end dates.

Movies are also distributed through various TheaterCompanies. Because each movie can be shown by multiple theater companies, and each theater company can screen many movies, this many-to-many relationship is represented by the RevenueReport associative entity. The RevenueReport table captures financial details such as ticket sales and release dates.

Additionally, movies are linked to the Persons who contributed to them—such as actors, directors, and editors—through the Credits associative entity. This many-to-many relationship between Movie and Person records each individual’s credit type and character name if they have one.

Finally, since a single ProductionCompany can oversee the creation of multiple movies, there is a one-to-many relationship between ProductionCompany and Movie. This ties together the creative, operational, and financial aspects of filmmaking under one company, providing a comprehensive structure for managing the full production lifecycle within the data model.


![plot](./ProjectDataModel_Final.png)

## Data Dictionary:
![plot](./Agent.png)

![plot](./Assignment.png)

![plot](./Contracts.png)

![plot](./Credits.png)

![plot](./Location.png)

![plot](./Movies.png)

![plot](./Person.png)

![plot](./ProductionCompany.png)

![plot](./ProductionSite.png)

![plot](./RevenueReport.png)

![plot](./TheaterCompany.png)

## Queries:
![plot](./Query_Table.png)

1. Query 1: 
![plot](./Query_1.png)


3. Query 2:
![plot](./Query_2.png)


5. Query 3:
![plot](./Query_3.png)


7. Query 4:
![plot](./Query_4.png)


9. Query 5:
![plot](./Query_5.png)


11. Query 6:
![plot](./Query_6.png)


13. Query 7:
![plot](./Query_7.png)


15. Query 8:
![plot](./Query_8.png)


17. Query 9:
![plot](./Query_9.png)


19. Query 10:
![plot](./Query_10.png)


## Database Information:
Name of the database: ns_F25MIST4610_59925_Group1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
