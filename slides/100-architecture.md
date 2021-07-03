# Architecture

<!--
Note: Omdat je de enige bent ga je mee in wat je online kan vinden.

Note: Belangrijkste architectuurbeslissingen zijn niet anders dan anders.

Note: Sneller gemaakt maar je hebt er ook als enige last van

Note: wel meer druk op goede design patterns want wildvreemden moeten je kunnen volgen.

Belangrijkste verschil: je bent de enige dus er is geen mentor.

Open source componenten zijn snel van de markt of backwards incompatible.

DATABASE ARCHITECTURE?

-->


## Repository Design Pattern

<img class="r-stretch" src="./images/architecture/repository.png">


(demo)


Notes:

- Each repository tends to become a huge class that kind of does everything
- An interface with one class ("because it's a contract") isn't particularly useful
- Important to be consistent.
<!-- Firefly III also has these Factory things -->


## Builder Pattern

<img class="r-stretch" src="./images/architecture/builder.png">


(demo)


<img class="r-stretch" src="./images/architecture/query.png">


## API-first approach

<img class="r-stretch" src="./images/architecture/api-first.png">


(demo)


Notes:

- Saves a lot of code
- Migrating is hard
- Almost requires a SPA
