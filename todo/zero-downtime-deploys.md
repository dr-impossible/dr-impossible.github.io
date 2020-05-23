# Zero-downtime Deploys

* you should be able to unplug a running server without causing your service to fail
* never allow developers to edit code directly on a server (never bypass CI)
    * there is never a good reason to allow this
    * developers will pressure you to let them do it "just this once". They will adapt if you never let them do this
    * changes must be made through source control and CI
    * your CI/CD process should be quick for hotfixes
    * 


* run the next and current release concurrently
* re-route requests to the new release
* easy rollbacks
* 12-factor app [12factor.net]
* never edit production directly, only edit code via source control
    * there is never a good reason to allow developers to modify code directly on a production (or dev) machine
    * they may even pressure you to allow them to do it "just this once" because they're in a rush - too bad. Your deployment process should be quick and should accommodate quick changes via source control
* 