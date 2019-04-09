# Getting started with IBM Business Automation Insights for decisions

## Audience

This tutorial is for technical and business users who want to configure Operational Decision Manager, the decisioning capibility of IBM Digital Business Automation, to emit decision events for Business Automation Insights. 

## Time required

45 minutes

## Learning objectives

-   Configure Operational Decision Manager to use the ODM event emitter for Business Automation Insights.
-   Explore the predefined Kibana dashboard for decisions.
-   Create and test a custom Kibana dashboard.

## Scenario

This tutorial demonstrates the following tasks:

-  How to configure the sample server to enable the Business Automation Insights event emitter during an HTDS ruleset execution. 
-  How to configure a ruleset to emit events.
-  How to run an HTDS ruleset execution in the Rule Execution Server console.
-  How to view the emitted events in the predefined Kibana dashboard for decisions. 
-  How to create a Kibana dashboard that contains custom widgets that are linked to a predefined search.

**Important:** In this tutorial, you use the default configuration for the Business Automation Insights plug-in. The plug-in can try numerous times to connect to Kafka. This can reduce performance, and should be taken into consideration when moving to production (see [Moving to production](https://www.ibm.com/support/knowledgecenter/SSYHZ8_18.0.x/com.ibm.dba.bai/topics/tsk_bai_moving_to_prod.html)).

## Additional information

For more information, visit the following resources:

-   [Configuring the ODM event emitter](https://www.ibm.com/support/knowledgecenter/SSQP76_8.10.x/com.ibm.odm.distrib.config/topics/con_config_bai.html)
-   [Properties for ODM emitter](https://www.ibm.com/support/knowledgecenter/SSQP76_8.10.x/com.ibm.odm.dserver.rules.res.console/topics/con_rescons_rs_prop_bai.html)
-   [Overview - What is IBM Business Automation Insights?](https://www.ibm.com/support/knowledgecenter/SSYHZ8_18.0.x/com.ibm.dba.bai/topics/con_bai_overview.html)
-   [Decisions dashboard](https://www.ibm.com/support/knowledgecenter/SSYHZ8_18.0.x/com.ibm.dba.bai/topics/con_bai_odm_dashboards.html)

## Prerequisites
You must do the following tasks before you can work on the tutorial:
-   Install WebSphere Application Server Liberty 18.0.0.4. An image of the server, **WLP**, is included as a complementary application server in the Operational Decision Manager installation files. Locate the file in your downloaded images, and decompress it in a separate directory on your computer. In the tutorial, the Liberty directory is referred to as *LibertyInstall*.
-   Install Operational Decision Manager 8.10.1 (see [Installing Operational Decision Manager](https://www.ibm.com/support/knowledgecenter/SSQP76_8.10.x/com.ibm.odm.distrib.install/topics/odm_distrib_install.html)). Keep the options for samples and tutorials when you do the installation. In the tutorial, the installation directory is referred to as *ODMInstall*.

**Note:** [Task 1: Enabling the Business Automation Insights plug-in](gs_topics/tut_bai_gs_enable_lsn.md) explains how to configure the ODM event emitter for an on-premises installation of Operational Decision Manager. This configuration is slightly different from Operational Decision Manager in Digital Business Automation for Multicloud. Additional information is provided in task 1.

-   Install Business Automation Insights 18.0.2. See [Getting started with IBM Business Automation Insights](https://www.ibm.com/support/knowledgecenter/SSYHZ8_18.0.x/com.ibm.dba.bai/topics/tut_getting_started.html) to install Business Automation Insights and IBM Cloud Private, and [Installing IBM Business Automation Insights on Certified Kubernetes](https://github.com/dbamc/cert-kubernetes/tree/master/BAI ) for installation instructions for other Certified Kubernetes platforms in the [Certified Kubernetes Conformance Program](https://landscape.cncf.io/category=platform). You need to note the following information for the tutorial:

    -   The Kafka bootstrap server
    -   The Ingress topic name
    -   Whether the security is enabled. If security is enabled, you need the chosen configuration and eventually a key file.
    
-   Download this tutorial from this ODMDev GitHub repository. Click **Clone or download**, and then **Download ZIP**. This action downloads the entire contents of this GitHub repository. The compressed files include a sample property file that you edit in the tutorial. Decompress the contents of the downloaded file to a new directory on your computer. In the tutorial, the new directory is referred to as *GettingStartedInstall*.

## Table of contents

-   [Task 1: Enabling the Business Automation Insights plug-in](gs_topics/tut_bai_gs_enable_lsn.md)
-   [Task 2: Enabling Business Automation Insights properties for a ruleset](gs_topics/tut_bai_gs_prop_ruleset_lsn.md)
-   [Task 3: Running the ruleset](gs_topics/tut_bai_gs_emit_lsn.md)
-   [Task 4: Looking at the predefined dashboard](gs_topics/tut_bai_gs_dashboard_lsn.md)
-   [Task 5: Making a custom dashboard](gs_topics/tut_bai_gs_custom_lsn.md)

## Licensing information

Copyright IBM Corp. 1987, 2019. Licensed to the Apache Software Foundation \(ASF\) under one or more contributor license agreements. See the NOTICE file distributed with this work for additional information regarding copyright ownership. The ASF licenses this file to you under the Apache License, Version 2.0 \(the "License"\); you may not use this file except in compliance with the License. You may obtain a copy of the License at [http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0). Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

[**Next task**](gs_topics/tut_bai_gs_enable_lsn.md)
