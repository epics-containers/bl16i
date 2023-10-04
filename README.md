Template for a Beamline or Accelerator Domain Repository
========================================================

This is where you will define all IOC instances for the beamline/domain.

The IOC instance will take the form of a subfolder in the iocs folder.
This subfolder will container a values.yaml file with at a minimum the
following (example):

```yaml
image: ghcr.io/epics-containers/ioc-adsimdetector-linux-runtime:23.10.1
```

This determins the Generic IOC image that is used to launch the instance.

In addition there will be a config folder which will be mounted into the
Generic IOC at runtime at /epics/ioc/config. This folder will contain
the required files to make the generic IOC into a specific IOC instance.

For the details of the contents of the config folder see the default
[start.sh](./iocs/blxxi-ea-ioc-01/config/start.sh)
