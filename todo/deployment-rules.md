# Deploying after-hours is unnecessary
* you should have zero-downtime deploys
* the internet is 24/7
* your customers don't share your timezone
* your devs likely don't either

# Deploying is risky
* deploying to production is inherently risky
* failure is most likely soon after a release (data needed)
* risks are better taken at the start of the day
* find me a workplace that allows your devs to start working at 4pm on deployment day

# Deploy at the start of the day, start of the week
* the whole team has time to react to production issues and provide support
* team members have more energy and can provide a better fix

# Why it's bad
* people can't wait to end the work day
* your deployment will be rushed
* hotfixes will be rushed

# On-call is harmful
* I'll probably never work for Pagerduty, but I'm ok with that
* on-call staff are randomly assigned
    * so they usually didn't write the code, and won't fully understand the problem
* on-call masochism
    * working after-hours is painful, but the team member gets rewarded for "taking one for the team". This can almost encourage shitty deployments and increase on-call incidents
    * some workplaces offer extra compensation for being on-call

