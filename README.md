# oc-cluster-wrapper-lite
A lightweight wrapper around oc cluster, for simple local OpenShift development

# Setup

1.) Set DEFAULT_OS_TYPE, and DEFAULT_OS_VERSION environment variables to specify defaults (optional). e.g

**DEFAULT_OS_TYPE="ose"**
**DEFAULT_OS_VERSION="v3.4"**

Will use OSE latest if this isn't specified

2.) Add cluster to your path. e.g

**cp $HOME/oc-cluster-wrapper-lite/cluster /usr/local/bin**

# Description/Usage

This wrapper will "remember" what cluster type, and version you brought up with the last "cluster up". For example, to initially bring up an Openshift Enterprise v3.4 cluster, run:

**cluster up ose v3.4**

After you are finished, you can run

**cluster down**

to bring down the cluster. The next time you want to run your cluster, you can just run

**cluster up**

and it will bring up the previous ose v3.4 cluster.

**cluster clear**

will erase saved settings, and persistence - allowing you to start fresh.

**cluster logs**

Will show curated master logs, highlighting debug vs warning vs error log messages. This automatically runs on cluster up. 
