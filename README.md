# Autopilot example repo

This is a companion repo for the [concourse-autopilot-resource](https://github.com/efejjota/concourse-autopilot-resource)

## Showcased features
- Easy to setup using familiar tools `fly execute`
- Configuring pipelines using multiple config files
- Passing static variables to individual pipelines
- No enforced location for storing config files
- Using wildcards in `.autopilot/config.yml` config
- Arranging pipelines into different Concourse teams

## Quickstart
To setup this example repo in your own Concourse instance do:

1. Clone this repository
    ```bash
    git clone  https://github.com/efejjota/concourse-autopilot-example
    ```
1. Navigate to the root of your repository
    ```bash
    cd concourse-autopilot-example
    ```
1. Run to generate yout autopilot pipeline
    ```bash
    fly -t <your-target-name>           \
        execute                         \
        -c .autopilot/task.yml          \
        -i 'repository=.'               \
        -o 'regenerated=regenerated'    \
        -v config=.autopilot/config.yml
    ```
1. Run to set autopilot to your Concourse
    ```bash
    fly -t <yout-target-name>           \
        set-pipeline                    \
        -p autopilot                    \
        --team main                     \
        -c regenerated/pipeline.yml
    ```

Wait a few seconds, and _Voilà_!

You can experiment further by forking this repo and modifying the [.autopilot/config.yml](.autopilot/config.yml) accordingly.