# CS-255-Project-2

1. Summary of the project
The project is the same one: DriverPass, with Liam as owner and Ian as IT officer, wanted a web-based training system for DMV test preparation. It includes online classes and practice tests, reservation of driving lessons, and administrative and reporting tools. This document turns the business requirements into a technical design using UML diagrams and a technical requirements specification.

2. What I did well
The Technical Requirements section is the strongest part. I matched the technology to the business needs:

Booking and payments: a relational database with ACID compliance (PostgreSQL or MySQL), because reservations and payments need strict consistency.
Availability: multi-availability-zone cloud hosting for disaster recovery, plus auto-scaling.
Mobile and desktop use: a responsive front end in React or Angular.
Security: TLS 1.3 for all traffic.

I also broke the requirements into hardware, software and tools, and infrastructure, which makes them easy to review.

3. What I would revise
I would revise the UML section, because the four diagram sections are empty in the file you uploaded. I would complete them in this order:

A use case diagram for the five roles.
Activity diagrams for registering, booking, and canceling a lesson.
A sequence diagram for making a reservation, from customer through the interface and booking service to the database and the log.
A class diagram for User, Reservation, Package, Driver, Car, Test, and ActivityLog.

I would also trim the technical requirements, since “React or Angular” and “AWS or Azure” leave decisions open. Those choices should be justified with cost and team skills.

4. Interpreting user needs, and why it matters
Liam’s needs for reports and data access anywhere led to the cloud-hosted, responsive design and a durable database. Ian’s concern about security and backups led to managed cloud infrastructure and TLS. The need to book without double-booking led to the choice of a transactional database. Considering users matters because design choices such as performance, security, and platform all depend on how people actually use the system. If the design ignores that, the result may be technically sound but unusable.

5. My approach to designing software
I move from requirements to models to architecture. The UML diagrams show who uses the system, how work flows, how components interact, and how data is structured, and then I choose technology to fit. In the future I would also use:

Architecture decision records to document why each technology was chosen.
Prototypes and early testing of risky areas, such as the DMV connection and payment handling.
Design reviews with the client at each stage.
Threat modeling to find security risks before building.
Iterative development with continuous feedback.
