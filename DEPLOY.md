# Deploying biodati.com

[Build status](https://drone.biodati.com/biodati/biodati.com.hugo)

The .drone.yml describes the configuration of the build/deploy process for this repository.

Only the staging and master (prod) branches are built and deployed to Amazon S3.

## Steps

Any changes to the staging branch will kick off a CI process using Drone (see below).

Steps:
1. Clone
1. Build hugo public folder
1. Deploy to Amazon S3 (staging.biodati.com)


## Drone CI

BioDati CI server: https://drone.biodati.com/


Useful commands:

    # In staging branch, run drone locally for testing (requires installing drone-cli)
    drone exec --branch staging --repo biodati/biodati.com.hugo
