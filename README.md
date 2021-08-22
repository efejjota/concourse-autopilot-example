# Autopilot example repo

This is a companion repo for the [concourse-autopilot-resource](https://github.com/efejjota/concourse-autopilot-resource)

It showcases most of the current features of the resource:
- Configuring pipelines using multiple config files
- Passing static variables to individual pipelines
- No enforced location for storing config files
- Using wildcards in 'autopilot.yml' resource config
- Arranging pipelines into different Concourse teams

To see the [concourse-autopilot-resource](https://github.com/efejjota/concourse-autopilot-resource) in action simply set the [autopilot.yml](autopilot.yml) manifest in your own Concourse instance. Wait a few seconds, and _Voilà_!

You can experiment further by forking this repo and modifying the [autopilot.yml](autopilot.yml) `source.uri` accordingly.