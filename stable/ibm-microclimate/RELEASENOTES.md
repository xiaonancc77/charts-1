# Breaking Changes
No breaking changes.

# What’s new in Chart Version 1.10.0

## Microclimate
* Microclimate portal now has a new logging feature to help with problem determination.

# Fixes
* Various minor bug and stability fixes.


# Prerequisites
- IBM Cloud Private Version 3.1.1 or later. Older versions of IBM Cloud Private are supported only by chart versions v1.5.0 and earlier. Version support information can be found in the release notes of each chart release.
- Ensure [socat](http://www.dest-unreach.org/socat/doc/README) is available on all worker nodes in your cluster. Microclimate uses Helm internally, and both the Helm Tiller and client require socat for port forwarding.
- Download the IBM Cloud Private CLI, `cloudctl`, from your cluster at the `https://<your-cluster-ip>:8443/console/tools/cli` URL.


# Upgrading from 1.9.0

Microclimate can be upgraded from the IBM Cloud Private Helm Releases view. When performing the upgrade, ensure the `Reuse Value` option is selected.

If you are upgrading with Helm from the command line, you should pass the same values into the Helm upgrade command that you initially installed the chart with to ensure configuration remains the same. It is recommended that you retrieve these values and store them for the upgrade by using the following command with your Microclimate release name:

`helm get values <release-name> > values.yaml`

You can then perform the upgrade with the following command:

`helm upgrade <release-name> <path-to-microclimate-chart> -f values.yaml`


# Documentation
For detailed installation instructions go to https://microclimate-dev2ops.github.io/installicp

# Version History

| Chart | Date | Kubernetes Version Required | Image(s) Supported | Breaking Changes | Details |
| ----- | ---- | ------------ | ------------------ | ---------------- | ------- |
| 1.10.0 | January  11, 2019 | 1.11.0  | 1901 | None | Improved logging. Various fixes and stability improvements |
| 1.9.0 | December 13, 2018 | 1.11.0  | 1812 | None | Added support for Linux® on Power® (ppc64le). |
| 1.8.0 | November 16, 2018 | 1.11.0  | 1811 | None | Added support for ICP 3.1.1. Various fixes and improvements |
| 1.7.0 | October 12, 2018 | 1.11.0  | 1810 | None | Various fixes and improvements |
| 1.6.0 | September 14, 2018 | 1.11.0  | 1809 | Support only for ICP 3.1.0 | Various fixes and improvements |
| 1.5.0 | Aug 20, 2018 | 1.10.0, 1.9.1 | 1808 | None | Various fixes and improvements |
| 1.4.0 | July 20, 2018 | 1.10.0, 1.9.1 | 1807 | None | Logout implemented, various small fixes and improvements |
| 1.3.0 | June 29, 2018 | 1.10.0, 1.9.1 | 1806 | Multi-user support caused changes to the Microclimate PVCs - upgrade will not work  | Various changes and new features |
| 1.2.1 | June 11, 2018 | 1.10.0, 1.9.1 | 1805 | Upgrading from versions v1.1.x requires additional steps for project migration | ICP 2.1.0.2 fixes |
| 1.2.0 | May 25, 2018 | 1.10.0 | 1805 | Upgrading from versions v1.1.x requires additional steps for project migration, An additional secret must be created to use the Helm tiller in kube-system |  |
| 1.1.1 | May 1, 2018 | 1.9.1 | 1804 | None |  |
| 1.1.0 | Apr 27, 2018 | 1.9.1 |  | The docker-registry secret required by microclimate has been changed from microclimate-icp-secret to microclimate-registry-secret |  UI updates, Users can authenticate with Jenkins using their IBM Cloud Private credentials |
| 1.0.0 | Mar 30, 2018|  1.9.1 |  | None  | New product release. See https://microclimate-dev2ops.github.io/ |
