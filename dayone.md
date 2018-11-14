
# Day 1

## Jeff Smith - Moving from Ops to DevOps: Centro's Journey to the Promised-land

- Devops is Different for every company, no one solution will work for everyone.
- Process engineering
  - augment existing processes - not new processes
- Software engineering 
  - New processes
  - Identify the issues
- Managing all environments - don't have different teams managing different environments, this leads to inconsistencies
- Don't assume the people who write the software know the best way to run it, offer your expertise
- As always there are trade offs with any changes you make
  - *time ,flexibility, fewer interruptions* vs *control, security, approval*
- Participate in developer rituals (stand-ups etc)
- Decide on metrics to track
- Don't nanny the devs, but maintain safety
- Monitor how your operationalisation language impacts behaviour
- Monitor the types of work you're doing
- Automate unplanned work where possible

When dealing with queries from developers

- Start with Yes...but - assume you can do something, but figure out how to make it safe.
- Ask for context, often people come to you for help with a solution. Its possible the actual problem could be solved a different way. It helps to have the whole picture

In Jeff's environment the following issues were identified

- devs have no rights on dev instances
- devs have no access on prod
- devs could not create alerts

In response, the following fixes were applied

- Root access on dev instances
- Devs get access to common safe tasks in prod
- Migrated alerts to datadog (metrics, logs, alerting all in one place)
- Share information on infrastructure via lunch and learns and pairing


Jeff also made some book recommendations:

- Turn the Ship Around!: A True Story of Turning Followers into LeadersBook - 
by L. David Marquet 
- Were making this for you - your job should be as cool as your friends think it is (Maybe this was a joke as i cant find it on the internet....)

## François Conil - Monitoring that cares (the end of user based monitoring)

- Don't let your customers tell you stuff is down
- Why are we on-call? - because people use our products
- When there is a sea of red on dashboards people get used to it
- Use the triad to solve issues Performance team + ops + devs. Together you can solve any problem
- Only create actionable alerts
  - Something breaks
  - customers notice
  - I am the best person to fix it
  - I need to fix it immediately
- Dev and ops talk early on to get monitoring from the start
- Use Basic up/down monitoring - define what is up and down
- If you can, use smart monitoring that determines root cause
- AB testing with monitoring ie trial different alerting policies on half the stack
- No one likes meetings, but they are critical
- If you need help, ask the real question with full context
- Not everything has a price but everything has a cost
- Turn complaints into numbers - give it a cost
- The whole is greater than the sum of its parts

**If a server crashes in a forest and no one is using it, is it down?**

## Mark Simpson, Carlie Osborne - Transforming the Bank: pipelines not paperwork

- Banking(ANZ) = risk averse
- Monolith Current state
  - Very slow release cadence, every 16 weeks
  - Middle of the night releases with an outage
- Goal
  - Middle of day releases
  - once a week
  - no downtime

12 week focus group - ended up taking 16 weeks

- Didn't touch monolith code
- Jenkins pipelines - code commit -> -> -> prod
- Replaced selenium with cypress.io
- Rules engine to ensure steps have been completed before going to prod
- Canary testing
- Change process was horrible - convinced change team to allow them to go good as long as they use in house rules engine
- Communicated change to everyone

Results

- 28 releases in 6 months
- 95% less toil for each release

- Small, not big - breaking items down into small tasks
- 4-5 weeks to release a feature
- Break features down into small pieces that deliver value
- Getting feedback and change based on feedback
- Solution derived over time rather than perfect on day one
- Engage sooner rather than later with risk, and any other interested parties

## Ryan McCarvill - Fighting fires with DevOps

Ryan told a great story about a project to replace the onboard computers on New Zealand firetrucks. There was a list of requirements that had to be met. When disaster struck and the main part of the solution overheated and was no longer usable. He fell back to some very simple methods to meet the majority of the requirements. 

Automation gives us the 
- flexibility to change
- flexibility to grow
- Solve any problem
- Solve new problems with old technology
- put out technical fires

## Opens spaces

### Data

- Collect all data in a raw format
- Clean and process data into more usable states
- Everyone should have access to data
- Security needs to be kept in mind when presenting data to everyone (ie sensitive info)

### Documentation

Why?

- Get details out of peoples heads
- Support teams

A wiki is the best way
Tags to allow searching

Sarah Maddox - google tech writer blog

### SRE vs CRE vs Devops

CRE - external
SRE - internal
Devops - ?

- Metrics and monitoring
- Goal - product quality and customer experience
- CRE is part of SRE which is an implementation of devops
- Lots of similarities

## Ignites

### Everett Toews - A Trip Down CI/CD Lane

A history of tools people have used in the past

### Jeff Smith - Creating Shared Contexts

- Context is what we bring when trying to solve a problem
- Get everyone on the same page
- Conversations help create a shared context
- Information exchange
- Communication tools
- Ask why
- The x/y problem, talking about a solution rather than the problem
- Shared presentation of data
- Shared execution methods - eat your own dog food
- Shared goals, shared constraints, shared priorities

### Peter Sellars - 2018: A Build Engineers Odyssey

Hire people that are Humble, hungry, smart

npm ci = consistency

## Katrina Clokie - Testing in DevOps for Engineers

- There are different levels of literacy in testing
- Most people are testing with their blinkers on and realise there are options
- Testing is part of your role - No matter what your role is
- Testing in devops is like air - its all around you
- You need to learn to test as part of your daily work
- Ingrain it in your processes
- oracles - the way we tell something is wrong
  - Does it work how we think it should?
  - Does it work the way it used it?
  - Does it work the way people want it to
- HICCUPPS
  - history
  - image
  - comparable products
  - claims
  - users desires
  - product
  - purpose
  - statutes
- Test pyramid 
- Katrina's take on the testing pyramid - A bug filter test pyramid
- Keep testing even when in prod (Monitoring Alerting Logging)
- AB testing to determine what works better - let the customer tell you
- Look for answers in new places