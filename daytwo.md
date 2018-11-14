# Day 2

## Alison Polton-Simon - The DevOps Experiments: Reflections From a Scaling Startup

Angaza Products

- Solar home
- Sell life chngin gprducts
  - Solar lights
  - Solar phone chargers
- 50% engineering
- pay as you go
- Key codes to unlock device
- Create software to meter waterpumps/lights/cook tops
- Allow locking if payments are not met
- Operating with dodgy networks - 2G

Platform uptime is business critical

- households without lights
- famers without irrigation

Tools

- buildkite - healthchecks
- grafana - enpointdashboard
- zendesk - ticketing system


Growing from very small team to larger team

Stage 1

- everyone does everything

Stage 2

- One person fights all fires
- blue / green
- fewer interruptions

Stage 3

- Support + ops teams
- Dedicated team for roadmaps and requests
- Team rotation allowed people to get a deeper understanding of the environment/products
- rotation caused context switching

Stage 4

- 5 independatnt teams
- own what you build
- cross team coordination
- Still have tributes to ensure incidents are managed - mitigates shared code having no ownership

Shared engineering manifesto in source control signed by all staff

- Dependable is better than fashionable
- Prefer industry standare tech
- Get creative when neccessary

## Anthony Borton - Four lessons learnt from Microsoft's DevOps Transformation

Lessons migrating on prem service to the cloud

- Need to know customers are going to use a feature before spending time on it
- Use of feature teams including dev ops product mangers etc
- Physical team rooms - 10-12 people (two pizza team)
- Own features and deployments of those features
- Self forming teams
  - 20% make the move
- Tests took too long and were not trust worthy
- move testing to the left
  - unit tests + functional
  - strive to test broad class of fast in memory tests
- Massive shift over 3 years from lots of end to end tests to unit tests
- 83000 tests run on each PR
- Same tools from dev - > prod
- zero downtime
- 5 deployment rings - test on themselves, then slowly deploy out to the rest of the world
- more features in 2016 than the previous 4 years combined

A book recommendation from Anthony

Drive: The Surprising Truth About What Motivates Us
Book by Daniel H. Pink

## Theresa Neate - Lean QA : T-shaped QAs in the DevOps World

- People have Generalist and specialist skills
- Devops = Anything that smooths the operation between dev and ops
- What do testers bring?
  - Critical thinking
  - Curiosity
  - Feedback
  - Systems thinking
- Tshaped = capable in a lot of things and expert in one of them
- Testers need to be able to do dev, architect, ba, ux, and sysops + expert in critical thinking
- Testing at every step of the process

Theresa recommended Damon Edwards devops podcast

## Mrinal Mukherjee - A DevOps Confessional

### One track devops

- Focusing on short term wins and not thinking about the long term strategy
- Only focused on infra
  - became bottle neck
  - siloed from devs

- Manage expectations
- Move outside your comfort zone

### MVP driven devops

- Cutting corners to go faster
  - Increased tech debt (phase two)
  - Security overlooked

- Minimum engineering standard
  - Peer review
  - Ensure rearchitecture is not required for each interation
  - Be proud of the work you do

### Judgemental devops

- Other teams causing delays
  - Criticism encourages stubborness

- Empathy
  - Find out what is causing the delay
  - There may be valid reasons for lead times
  - motivations and constraints
  - Stive for common ground
  - Collaborate

## Open spaces

### Kubernetes + Openshift

I didnt find this one particularly useful, it was a large room of people and mostly just talking about what people are doing

### Infra as code

Mostly talking about what people use to manage their infra.

Interesting discussion about when its worth automating vs not.

There was a mention of this xkcd comic https://xkcd.com/1205/

### WIP

- Less is better
- Measure improvements
  - WIP Chart
  - Cycle time
- Symptoms of an issue
  - Not getting stuff done
  - Context switching
  - Unplanned work
- Break stories up with defined goals
- Make it visible
- Use sprint limits
- Self controlling (haha)
- Waiting is OK (dont jump onto something else while you wait)
 - Try Mob programming
   - [A day of mob programming](https://www.youtube.com/watch?v=p_pvslS4gEI)
   - [Mob programming](https://www.youtube.com/watch?v=hJ5kdv28pgI)

## Ignite

### Allen Geer, Amanda Baker - Continuously Testing govt.nz

- Gherkin test cases
- Circleci
- behat
- spec by example?
- How long do you take to automate something - xkcd
- Visulise so view improvements

### Jules Clements - Configuration Pipeline : Ruling the One Ring

Use CI tools as souce of trust

### Nigel Charman - Keep Calm and Carry On Organising

Sorry, no notes taken

## Jessica DeVita - Retrospecting our Retrospectives

I found this talk very hard to follow.

What I got from it was dont play the blame game at retros, change your language to make it less agressive.

A book recommended by Jessica

Fierce Conversations by Susan Scott

https://stella.report - incident reports

[Catch the apache SANFU](snafucatchers.github.io/#3_1_Catching_the_Apache_SNAFU)

[Ironies of automation](https://www.sciencedirect.com/science/article/pii/0005109883900468)