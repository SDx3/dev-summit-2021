# Index
1. My name is ~.
2. working under alias James Cole on Firefly III, 10 years now.
3. Loads of people know it's me, but I like the "anonymity"




# History

## index
1. Started in ~2010 with "Firefly"
2. Launched "Firefly III" somewhere in 2014

## budgets
Basic budgeting things, set amount, roll-over to the next month

## rule engine 
Added a rule engine for transaction management

## reports
1. Shiny reports
2. Tried Groovy in ~2012 in "Firefly Mark 2".

## More info?
1. Check out these sites.




# Topics for today

1. (Read topics out loud)
2. Remember questions for the end.
3. Contact me if you want to learn more. AMA





# Architecture

1. Firefly III is a Laravel application.
2. It uses 3 design patterns I want to show you.

## Repository design
1. From controllers, go to repository, who will go to DB for you.

## Repository DEMO
1. Go to Repositories folder.
2. Show TransactionJournal folder.
3. Show Account

## Repository notes
1. In the demo you saw lots of classes. They have lots of business logic.

## Builder pattern
1. Lots of views that show transactions. Grouped by date, by type, by account. By budget, etc.
2. Query builder that creates the exact query you need to collect the right transactions.

## Builder pattern DEMO
1. Go to GroupCollectorInterface. Show all the functions in the overview.
2. Go to GroupCollector. Show all extra code.

## Builder notes (SQL QUERY IMAGE)
1. Massive queries
2. Can't handle everything through queries
3. Tends to be overkill for simple cases

## API first approach
1. Make a PLATFORM
2. API all the things
3. Already amazing stuff built by users.

## API first approach screenshot
1. This is Grafana, extracting data from Firefly III.

## API first approach notes
1. Requires a Single Page Application. You have to use your own platform as an app.
2. Example: AWS, (almost) everything you can do in the portal can be done over an API.



# Upgrade Firefly III
1. Talking about two subjects, upgrading open source apps AND helping users upgrade.


## Three main challenges
1. When using open source components only, you realize how tricky this can be.
2. Laravel used to do use backwards incompatible changes between releases. Many other packages still do
3. Lots of ancient libraries out there. Security warnings.

## JC5 packages
1. I'll do it myself then.
2. Lots of trial and error.


## Public security update alerts
1. Everybody can see you are vulnerable.


## Upgrade users
1. Little support, people will flood in anyway. They won't stop.
2. You have no responsibility, but lets not go the "Tiny Tiny RSS" way.

## Docs.firefly.org
1. Documentation extends itself.

## Docs.firefly.org (TWEE KEER)
1. Documentation extends itself.


## Upgrade support.
1. Many scripts and tools around.
2. Lots of documents and trying to build a community.
3. Still many users holding out their hand.


## Hosting platforms
1. There are many hosting platforms and most of them are pretty foolproof.
2. Lots of internal upgrade and verify commands.

## Screenshot of PHP update commands
1. Lots of code is present in Firefly III for a smooth upgrade.
2. Still able to upgrade from 3, 4 years ago to a current version, in ONE go.

## Screenshot of softaculous
1. They caught a lot of bugs.
2. Yunohost used to have everything in French. Less helpfull.






# API
1. Trying to turn Firefly III into a platform that supports apps and tools requires a reliable API.
2. Very proud of these creations.
3. None of these are mine.

## Create.vue
1. My own code is now calling the API.
2. Saves me a lot of code.

## New layout
1. Slowly working towards a new SPA in Vue.
2. Everything through the API.

## API DEMO
1. Show API classes
2. Show API transformers.
3. Show API routes
4. hoe de applicatie de API submit
5. aparte routes voor de API.
6. betekent dat je de gewone code kan droppen.
7. Nu nog per model maar wellicht per domain?

(8. Eventueel ook tricks per pagina.)

## API Challenge
1. Design not build. Slowly extend is tricky.
2. Let go of the database as your model.

## API challenge 2 (image)
1. Explain objects briefly
2. API generators usually cant handle this. 

## API docs
1. Write the docs. Users will follow.
2. You can TRY the API here as well.
3. Use Postman to test and develop.

## Using other API's
1. Each user must register separately.
2. I can't really "do" PSD2 because of this.
3. There is not a single Firefly III
4. Users that don't upgrade will lose API's.








# Teamwork
1. Most of the work is done by me
2. Small team of dedicated submitters.

## Git flow
1. Current flow (explain it)

## New flow
1. Explain it.

## Pi-hole
1. Example of what i'd like
   
## Pi hole screenshot 2
1. Current code of Firefly III is complex, lots of spagetti

## Getting PR's from strangers
Also interesting is, linked to the git

## Getting PR's screenshot
Not always included.

## Tricky to manage
1. Arch changes
2. New features
3. Security updates

## Tricky to manage
1. Security fix from Nextcloud. Nothing worked.

## Managing versions
1. Used to have main and develop and that was it.
2. New version = some brave souls test it and lets see what happens.
3. Now also alpha beta channels for brave guys.

## Dedicated version website.
1. Basic piece of code so users can poll for new version.
2. Always opt in!

## JSON example
1. Shows a basic JSON file, static hosting.

## Demo of testing code.
1. VersionCheckEventHandler
2. UpdateRequest















# TESTING
1. Lets talk about unit tests en how to test the API.
2. Firefly III has a lot of spagett code.

## PHPUnit
1. Im not going to demo a lot here.
2. Firefly iii had a lot of feature tests.
3. Now mainly focussing on unit tests and the API.
4. User interface is a bit of a closed book to me.

## DEMO
1. API tests, trying to be smart about testing all combinations.

## Running GitHub actions
1. It's been a while.
2. Big advantage is that you can set up flows to test everything.
3. Maybe Travis CI again.

## Plaatje van issues
1. However does not mean you cant forget test data when releasing. Oops.


## Building
1. Docker built on Azure using a machine that's currently in my attic.
2. Not really sustainable but it's cheap.
3. Building the base image in 7 variants can take up to an hour.
   Most CI's dont like that.
4. Building Firefly III itself is pretty fast.


## DEMO
- dev.azure.com
- project settings
- agent pools
- default pool
- agents
- compare with Azure Pipelines


