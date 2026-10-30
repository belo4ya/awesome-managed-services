# Awesome Managed Services

<!-- TOC -->
* [Awesome Managed Services](#awesome-managed-services)
    * [Managed Spark](#managed-spark)
    * [Managed PostgreSQL](#managed-postgresql)
<!-- TOC -->

### Managed Spark

Tags describe documented modes and versions. Multiple values are alternatives, not necessarily valid combinations.
`unknown`: not established by sources; `not-applicable`: does not apply.

| Tag            | Meaning                                                                                                                                                                                                  |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Engine         | Omitted for Apache Spark, including vendor distributions. `spark-derived`: a modified execution backend; `spark-compatible`: Spark APIs executed by another engine.                                      |
| Infrastructure | Runtime: `kubernetes`, `vm`, `bare-metal`. Kubernetes on VMs is recorded as `kubernetes`.                                                                                                                |
| Manager        | Spark resource manager: `kubernetes`, `yarn`, `standalone`, `custom` (proprietary).                                                                                                                      |
| Compute        | `cluster`: users configure cluster or node-pool capacity, including temporary job clusters. `serverless`: jobs or sessions without managing an infrastructure cluster.                                   |
| Deployment     | `cloud`: provider's own cloud service or vendor-hosted platform; `byoc`: vendor-managed data plane in the customer's cloud account; `self-hosted`: customer-deployed platform, in cloud or on premises.  |
| Market         | Market focus: `global`, `ru-cis`, `cn`, `europe`. Not deployment regions.                                                                                                                                |
| Scope          | Product category: `spark-service`, `lakehouse-platform`, `data-ai-platform`, `embedded-spark`, `spark-api-compatibility`.                                                                                |
| Group          | `leader`: sets industry expectations; `challenger`: distinctive engineering; `established`: mature operating experience; `follower`: follows common approaches; `legacy`: confirmed declining relevance. |
| Tier           | Engineering reference value, rated below independently of Group.                                                                                                                                         |

Spark Standalone on Kubernetes uses Infrastructure `kubernetes` and Manager `standalone`.
Market, Scope, Group, and Tier are editorial classifications; Group and Tier assess the Spark offering, not the vendor.

| Tier       | Engineering reference value                                                               |
|------------|-------------------------------------------------------------------------------------------|
| 💎💎💎💎💎 | Industry benchmark or exceptional depth of original engineering and operating experience. |
| ⭐⭐⭐⭐   | Deep engineering, substantial differentiation, or extensive operating experience.         |
| ⭐⭐⭐     | Mature solution or useful mechanisms and tradeoffs.                                       |
| ⭐⭐       | Mostly common approaches; few distinctive mechanisms established.                         |
| ⭐         | Confirmed technical lag, stagnation, or major limitations that reduce current relevance.  |
| `unrated`  | Insufficient evidence to rate.                                                            |

[Acceldata xDP / xLake (AppSpark)](https://docs.acceldata.io/xdp/xdp/xdp-documentation/app-spark)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`  
Deployment: `byoc`, `self-hosted` · Market: `global` · Scope: `data-ai-platform` · Group: `challenger`  
Tier: ⭐⭐⭐⭐

[Alibaba Cloud EMR on ACK](https://www.alibabacloud.com/help/en/emr/emr-on-ack/getting-started/quick-start-for-emr-on-ack)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Alibaba Cloud EMR on ECS](https://help.aliyun.com/en/emr/emr-on-ecs/user-guide/create-a-managed-as-policy)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Alibaba Cloud EMR Serverless Spark](https://www.alibabacloud.com/help/en/emr/emr-serverless-spark/user-guide/manage-kyuubi-gateways)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless`  
Deployment: `cloud` · Market: `global`, `cn` · Scope: `lakehouse-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Apolo Managed Spark Application](https://docs.apolo.us/index/apolo-console/apps/installable-apps/available-apps/apache-spark)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `byoc`, `self-hosted`  
Market: `global` · Scope: `spark-service` · Group: `unknown` · Tier: ⭐⭐⭐

[Arenadata Hyperwave (ADH Cloud)](https://arenadata.tech/ru/news/arenadata-hyperwave-rasshiryaet-vozmozhnosti-oblachnyh-vychislenij-v-novom-relize-adh-cloud)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `self-hosted`  
Market: `ru-cis` · Scope: `data-ai-platform` · Group: `challenger` · Tier: ⭐⭐⭐⭐

[AWS EMR on EC2](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-managed-scaling.html)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `leader` · Tier: 💎💎💎💎💎

[AWS EMR on EKS](https://docs.aws.amazon.com/emr/latest/EMR-on-EKS-DevelopmentGuide/spark-operator.html)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[AWS EMR Serverless](https://docs.aws.amazon.com/emr/latest/EMR-Serverless-UserGuide/emr-serverless.html)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: 💎💎💎💎💎

[AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/what-is-glue.html)

Infrastructure: `vm`, `unknown` · Manager: `custom`, `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `embedded-spark` · Group: `leader` · Tier: 💎💎💎💎💎

[Azure HDInsight Classic](https://learn.microsoft.com/en-us/azure/hdinsight/spark/apache-spark-overview)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Azure Synapse Analytics (Spark pools)](https://learn.microsoft.com/en-us/azure/synapse-analytics/spark/apache-spark-performance)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Baidu AI Cloud BMR on BCC](https://cloud.baidu.com/doc/BMR/s/ujwvxvcgr)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster`  
Deployment: `cloud` · Market: `cn` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Baidu AI Cloud BMR on CCE](https://cloud.baidu.com/doc/BMR/s/8mh1po82a)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[Canonical Managed Spark / Charmed Spark](https://canonical.com/data/spark/managed)

Infrastructure: `kubernetes`, `vm` · Manager: `kubernetes`, `unknown` · Compute: `cluster` · Deployment: `byoc`,
`self-hosted`  
Market: `global` · Scope: `spark-service` · Group: `established` · Tier: ⭐⭐⭐

[China Telecom (CTYun) Data Lake Insight](https://www.ctyun.cn/document/10014065/10118884)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[Cloud.ru Evolution Managed Spark](https://cloud.ru/docs/spark/ug/topics/concepts__general)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `cloud`  
Market: `ru-cis` · Scope: `spark-service` · Group: `unknown` · Tier: ⭐⭐⭐

[Cloudera Data Engineering](https://docs.cloudera.com/data-engineering/cloud/overview/topics/cde-service-overview.html)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `byoc`, `self-hosted`  
Market: `global` · Scope: `spark-service` · Group: `established` · Tier: ⭐⭐⭐⭐

[Cloudera Data Hub](https://docs.cloudera.com/data-hub/cloud/manage-clusters/topics/dh-autoscaling-behavior.html)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `byoc`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Databricks Classic compute](https://docs.databricks.com/aws/en/compute/configure)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm`, `kubernetes` · Manager: `unknown`, `not-applicable` · Compute: `cluster`  
Deployment: `byoc` · Market: `global` · Scope: `lakehouse-platform` · Group: `leader`  
Tier: 💎💎💎💎💎

[Databricks Serverless](https://www.databricks.com/product/serverless-compute)

Engine: `spark-derived` · Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless`  
Deployment: `cloud` · Market: `global` · Scope: `lakehouse-platform` · Group: `leader`  
Tier: 💎💎💎💎💎

[Dataiku DSS / Elastic AI (Kubernetes execution)](https://doc.dataiku.com/dss/latest/user-isolation/reference-architectures/kubernetes.html)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `self-hosted`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[DataOS / Flare (The Modern Data Company)](https://dataos.info/resources/stacks/flare/)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `unknown`  
Market: `global` · Scope: `embedded-spark` · Group: `challenger` · Tier: ⭐⭐⭐

[Dell Data Processing Engine](https://www.dell.com/support/manuals/en-us/dell-data-lakehouse/ddpe_p_gsg_170/get-started-with-dell-data-processing-engine-for-users?guid=guid-2174ba37-7aff-42c7-a5f7-bb08172a486d&lang=en-us)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `spark-service` · Group: `unknown`  
Tier: ⭐⭐⭐

[Domino Data Lab On-Demand Spark / Domino Cloud](https://docs.domino.ai/cloud/platform-capabilities/features/compute-clusters-hpc)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster`  
Deployment: `cloud`, `self-hosted` · Market: `global` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Google Cloud Managed Service for Apache Spark on Compute Engine](https://docs.cloud.google.com/managed-spark/docs/concepts/configuring-clusters/autoscaling)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster`  
Deployment: `cloud` · Market: `global` · Scope: `data-ai-platform` · Group: `leader`  
Tier: 💎💎💎💎💎

[Google Cloud Managed Service for Apache Spark on GKE](https://docs.cloud.google.com/managed-spark/docs/guides/dpgke/gke-scale-cluster)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `spark-service` · Group: `established` · Tier: ⭐⭐⭐⭐

[Google Cloud Managed Service for Apache Spark Serverless](https://docs.cloud.google.com/managed-spark/docs/concepts/serverless-spark-compare)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm` · Manager: `unknown` · Compute: `serverless`  
Deployment: `cloud` · Market: `global` · Scope: `spark-service` · Group: `established`  
Tier: 💎💎💎💎💎

[Hopsworks](https://docs.hopsworks.ai/latest/user_guides/projects/jobs/spark_job/)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`, `serverless` · Deployment: `cloud`, `byoc`,
`self-hosted`  
Market: `global` · Scope: `data-ai-platform` · Group: `challenger` · Tier: ⭐⭐⭐⭐

[HPE Ezmeral Unified Analytics](https://docs.ezmeral.hpe.com/unified-analytics/15/Spark/spark_overview.html)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Huawei Cloud Data Lake Insight](https://support.huaweicloud.com/intl/en-us/productdesc-dli/dli_07_0027.html)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Huawei Cloud MRS](https://support.huaweicloud.com/intl/en-us/usermanual-mrs/mrs_01_24728.html)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster`  
Deployment: `cloud` · Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Huawei Cloud MRS on CCE](https://support.huaweicloud.com/intl/zh-cn/helppanel-mrs/mrs_10_0011.html)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[IBM Cloud Analytics Engine (deprecated)](https://cloud.ibm.com/docs/AnalyticsEngine?topic=AnalyticsEngine-iae-serverless-relnotes)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `spark-service` · Group: `legacy` · Tier: ⭐⭐⭐

[IBM watsonx.data Spark (Cloud)](https://www.ibm.com/docs/en/watsonxdata/saas?topic=engines-provisioning-spark-engine)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `unknown` · Manager: `unknown` · Compute: `cluster`, `serverless`  
Deployment: `cloud`, `byoc` · Market: `global` · Scope: `lakehouse-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[IBM watsonx.data Spark (Software)](https://www.ibm.com/docs/en/watsonxdata/premium/2.4.x?topic=engines-provisioning-watsonxdata-spark-engine)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `lakehouse-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Iguazio AI/MLOps Platform](https://www.iguazio.com/docs/latest-release/cluster-mgmt/deployment/support-matrix/)

Infrastructure: `kubernetes` · Manager: `kubernetes`, `standalone` · Compute: `cluster` · Deployment: `byoc`,
`self-hosted`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Ilum](https://ilum.cloud/docs/architecture/)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `self-hosted`  
Market: `global` · Scope: `lakehouse-platform` · Group: `challenger` · Tier: ⭐⭐⭐⭐

[Incorta Cloud (Chidori)](https://community.incorta.com/t5/administration-knowledgebase/incorta-horizontal-scalability-scaling-to-meet-enterprise-needs/ta-p/6932)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `embedded-spark` · Group: `established` · Tier: ⭐⭐⭐⭐

[Informatica Cloud Data Integration (Advanced Clusters)](https://docs.informatica.com/cloud-common-services/administrator/current-version/advanced-clusters/troubleshooting/troubleshooting-an-advanced-cluster-subtask.html)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `byoc`  
Market: `global` · Scope: `embedded-spark` · Group: `established` · Tier: ⭐⭐⭐⭐

[IOMETE Data Lakehouse](https://iomete.com/resources/getting-started/architecture)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `lakehouse-platform` · Group: `challenger`  
Tier: ⭐⭐⭐⭐

[JFrog ML / Qwak](https://docs.jfrog.com/ai-ml/docs/batch-feature-set)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `embedded-spark` · Group: `unknown` · Tier: ⭐⭐⭐

[Kauzas Spark](https://kauzas.com/en/kubernetes-data-ai-platform)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `self-hosted`  
Market: `global` · Scope: `data-ai-platform` · Group: `unknown` · Tier: `unrated`

[Kingsoft Cloud KMR on KCE](https://docs.ksyun.com/documents/45120)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[Kingsoft Cloud KMR on KEC](https://docs.ksyun.com/documents/6101)

Infrastructure: `vm`, `bare-metal` · Manager: `yarn`, `standalone` · Compute: `cluster` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Kingsoft Cloud KMR Serverless Compute Engine](https://docs.ksyun.com/documents/43984?type=3)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[LinkTime Cloud Kubernetes Data Platform (KDP)](https://www.linktimecloud.com/kubernetes-data-platform)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `self-hosted`  
Market: `cn` · Scope: `data-ai-platform` · Group: `challenger` · Tier: ⭐⭐⭐⭐

[Microsoft Fabric Spark](https://learn.microsoft.com/en-us/fabric/data-engineering/spark-compute)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `unknown` · Manager: `yarn` · Compute: `cluster`  
Deployment: `cloud` · Market: `global` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Onehouse Cloud (Quanton runtime)](https://docs.onehouse.ai/product/dataplane-setup/architecture/)

Engine: `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`  
Deployment: `byoc` · Market: `global` · Scope: `lakehouse-platform` · Group: `challenger`  
Tier: ⭐⭐⭐⭐

[Oracle Big Data Service](https://docs.oracle.com/en-us/iaas/Content/bigdata/manage-cluster-patching-odh-update.htm)

Infrastructure: `vm`, `bare-metal` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Oracle Cloud Infrastructure Data Flow](https://docs.oracle.com/en-us/iaas/Content/data-flow/using/dfs_service_overview.htm)

Infrastructure: `vm` · Manager: `unknown` · Compute: `cluster`, `serverless` · Deployment: `cloud`  
Market: `global` · Scope: `spark-service` · Group: `established` · Tier: ⭐⭐⭐⭐

[Orange Business Flexible Engine Data Lake Insight](https://cloud.orange-business.com/wp-content/uploads/2022/06/Webinaire-DLI-pdf.pdf)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `europe` · Scope: `data-ai-platform` · Group: `unknown` · Tier: `unrated`

[Orchestera](https://orchestera.com/how-orchestera-works)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster` · Deployment: `byoc`  
Market: `global` · Scope: `spark-service` · Group: `unknown` · Tier: ⭐⭐⭐

[OVHcloud Data Platform (Spark)](https://www.ovhcloud.com/en-gb/public-cloud/data-platform/)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `europe` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Palantir Foundry (Rubix)](https://www.palantir.com/docs/foundry/architecture-center/rubix)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless`  
Deployment: `cloud` · Market: `global` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Qubole Data Service](https://docs.qubole.com/en/latest/admin-guide/engine-admin/spark-admin/autoscale-spark.html)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `byoc`  
Market: `global` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Scaleway Clusters for Apache Spark](https://www.scaleway.com/en/docs/apache-spark/concepts/)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `cluster`  
Deployment: `cloud` · Market: `europe` · Scope: `spark-service` · Group: `unknown`  
Tier: ⭐⭐⭐

[Snowflake Snowpark Connect / Snowpark Submit](https://docs.snowflake.com/en/developer-guide/snowpark-connect/snowpark-connect-apache-spark)

Engine: `spark-compatible` · Infrastructure: `unknown` · Manager: `not-applicable` · Compute: `cluster`  
Deployment: `cloud` · Market: `global` · Scope: `spark-api-compatibility` · Group: `challenger`  
Tier: ⭐⭐⭐⭐

[Stackable Managed Data Lakehouse](https://stackable.tech/en/managed-data-lakehouse/)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `europe` · Scope: `lakehouse-platform` · Group: `challenger` · Tier: ⭐⭐⭐

[STACKIT Workflows](https://docs.stackit.cloud/products/data-and-ai/workflows/tutorials/launching-a-spark-cluster/)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `serverless` · Deployment: `cloud`  
Market: `europe` · Scope: `embedded-spark` · Group: `unknown` · Tier: ⭐⭐⭐

[T Cloud Public / Open Telekom Cloud Data Lake Insight](https://docs.otc.t-systems.com/data-lake-insight/dli-umn.pdf)

Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless` · Deployment: `cloud`  
Market: `europe` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Tencent Cloud Data Lake Compute](https://cloud.tencent.com/document/product/1342/95666)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `serverless`  
Deployment: `cloud` · Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐⭐

[Tencent Cloud EMR on CVM](https://www.tencentcloud.com/document/product/1026/55459)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Tencent Cloud EMR on TKE](https://cloud.tencent.com/document/product/589/93152)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `global`, `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[VK Cloud Cloud Spark](https://land.vkcloud-static.ru/spark/)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `ru-cis` · Scope: `spark-service` · Group: `unknown` · Tier: ⭐⭐⭐

[Volcengine EMR on ECS](https://docs.volcengine.com/docs/e-map-reduce/em-ron-ecs-quick-start?lang=en)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Volcengine EMR on VKE](https://docs.volcengine.com/docs/e-map-reduce/emr-deployment-type-selection-guide?lang=en)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `cn` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐⭐

[Volcengine EMR Serverless](https://docs.volcengine.com/docs/e-map-reduce/product-architecture?lang=en)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `unknown` · Compute: `serverless`  
Deployment: `cloud` · Market: `cn` · Scope: `data-ai-platform` · Group: `challenger`  
Tier: ⭐⭐⭐⭐

[Yandex Cloud Managed Service for Apache Spark](https://yandex.cloud/en/services/managed-spark)

Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster` · Deployment: `cloud`  
Market: `ru-cis` · Scope: `spark-service` · Group: `unknown` · Tier: ⭐⭐⭐

[Yandex Data Processing](https://yandex.cloud/ru/docs/data-proc/concepts/autoscaling)

Infrastructure: `vm` · Manager: `yarn` · Compute: `cluster` · Deployment: `cloud`  
Market: `ru-cis` · Scope: `data-ai-platform` · Group: `established` · Tier: ⭐⭐⭐

[Yeedu](https://docs.yeedu.com/v2.10.0/)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `vm`, `bare-metal` · Manager: `standalone`, `not-applicable` ·
Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `spark-service` · Group: `challenger`  
Tier: ⭐⭐⭐

[Zetaris Cloud](https://www.zetaris.com/cloud)

Infrastructure: `unknown` · Manager: `unknown` · Compute: `cluster` · Deployment: `byoc`  
Market: `global` · Scope: `data-ai-platform` · Group: `unknown` · Tier: ⭐⭐⭐

[Zetaris Enterprise (Kubernetes/Tanzu)](https://kbase.zetaris.com/knowledge/installing-zetaris-on-vmware)

Engine: `apache-spark`, `spark-derived` · Infrastructure: `kubernetes` · Manager: `kubernetes` · Compute: `cluster`  
Deployment: `self-hosted` · Market: `global` · Scope: `data-ai-platform` · Group: `established`  
Tier: ⭐⭐⭐

### Managed PostgreSQL

- [Aiven PostgreSQL](https://aiven.io/postgresql)
- [Akamai Cloud (Linode) Managed PostgreSQL](https://www.linode.com/docs/guides/databases/postgresql/)
- [Alibaba Cloud ApsaraDB RDS for PostgreSQL](https://www.alibabacloud.com/en/product/apsaradb-for-rds-postgresql)
- [Alibaba Cloud PolarDB for PostgreSQL](https://www.alibabacloud.com/en/product/polardb-for-postgresql)
- [AWS Aurora PostgreSQL](https://aws.amazon.com/rds/aurora/)
- [AWS RDS for PostgreSQL](https://aws.amazon.com/rds/postgresql/)
- [Azure Database for PostgreSQL](https://azure.microsoft.com/en-us/products/postgresql/)
- [Baidu AI Cloud RDS for PostgreSQL](https://cloud.baidu.com/en/product/postgresql.html)
- [Civo Managed Databases](https://www.civo.com/public-cloud/databases)
- [ClickHouse Managed Postgres](https://clickhouse.com/docs/cloud/managed-postgres)
- [Cloud.ru Evolution Managed PostgreSQL](https://cloud.ru/products/evolution-managed-postgresql)
- [Crunchy Bridge](https://www.crunchydata.com/products/crunchy-bridge/)
- [Database Labs](https://www.databaselabs.io)
- [DigitalOcean Managed Databases](https://www.digitalocean.com/products/managed-databases/)
- [EDB Postgres AI](https://www.enterprisedb.com/products/edb-postgres-ai)
- [Fly.io Managed Postgres](https://fly.io/mpg)
- [Google Cloud AlloyDB for PostgreSQL](https://cloud.google.com/products/alloydb)
- [Google Cloud SQL for PostgreSQL](https://cloud.google.com/sql/docs/postgres/)
- [Heroku Postgres](https://elements.heroku.com/addons/heroku-postgresql)
- [Huawei Cloud GaussDB](https://www.huaweicloud.com/intl/en-us/product/gaussdb.html)
- [Huawei Cloud RDS for PostgreSQL](https://www.huaweicloud.com/intl/en-us/product/pg.html)
- [IBM Cloud Databases for PostgreSQL](https://www.ibm.com/products/databases-for-postgresql)
- [Instaclustr Managed PostgreSQL](https://www.instaclustr.com/platform/managed-postgresql/)
- [MWS Managed PostgreSQL](https://mws.ru/cloud-platform/managed-postgresql/)
- [Nebius Managed Service for PostgreSQL](https://nebius.com/services/managed-postgresql)
- [Neon](https://neon.com)
- [Nile](https://www.thenile.dev/)
- [Northflank Managed PostgreSQL](https://northflank.com/dbaas/managed-postgresql)
- [Oracle Cloud (OCI) Database for PostgreSQL](https://www.oracle.com/in/cloud/postgresql/)
- [OVHcloud Cloud Databases](https://www.ovhcloud.com/en/public-cloud/postgresql/)
- [pgEdge](https://www.pgedge.com/)
- [PlanetScale](https://planetscale.com/postgres)
- [Railway PostgreSQL](https://docs.railway.com/databases/postgresql)
- [Render Managed PostgreSQL](https://render.com/docs/postgresql)
- [ScaleGrid PostgreSQL DBaaS](https://scalegrid.io/postgresql/)
- [Scaleway Managed Database](https://www.scaleway.com/en/managed-postgresql-mysql/)
- [Scalingo for PostgreSQL](https://scalingo.com/databases/postgresql)
- [Selectel Cloud for PostgreSQL](https://selectel.ru/services/cloud/managed-databases/postgresql/)
- [Stackhero for PostgreSQL](https://www.stackhero.io/en-US/services/PostgreSQL/benefits)
- [Supabase](https://www.supabase.com)
- [Tencent Cloud TencentDB for PostgreSQL](https://www.tencentcloud.com/products/postgres)
- [Thalassa Cloud DBaaS](https://thalassa.cloud/products/databases/postgresql/)
- [Tiger Data Postgres](https://www.tigerdata.com/)
- [Timeweb Cloud Managed Service for PostgreSQL](https://timeweb.cloud/services/postgresql)
- [UpCloud Managed Databases for PostgreSQL](https://upcloud.com/postgresql-managed-databases/)
- [Vela](https://vela.simplyblock.io/)
- [Virtuozzo PostgreSQL](https://www.virtuozzo.com/database-platform-as-a-service/)
- [VK Cloud PostgreSQL as a Service](https://cloud.vk.com/databases/postgresql/)
- [Vultr PostgreSQL Databases](https://www.vultr.com/products/managed-databases/postgresql/)
- [Xata](https://xata.io/)
- [Yandex Cloud Managed Service for PostgreSQL](https://yandex.cloud/en/services/managed-postgresql)
