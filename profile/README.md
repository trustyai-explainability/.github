# Welcome to TrustyAI 👋

[TrustyAI](https://trustyai-explainability.github.io/trustyai-site/main/main.html) is an open source Responsible AI toolkit supported by Red Hat and IBM. TrustyAI provides tools for a variety of responsible AI workflows, such as:
- Local and global model explanations
- Fairness metrics
- Drift metrics
- Text detoxification
- Language model benchmarking
- Language model guardrails

TrustyAI is a default component of [Open Data Hub](https://opendatahub.io/) and [Red Hat Openshift AI](https://www.redhat.com/en/technologies/cloud-computing/openshift/openshift-ai), and has integrations with projects like [KServe](https://github.com/kserve/kserve), [Caikit](https://github.com/caikit/caikit), and [vLLM](https://github.com/vllm-project/vllm).

** **
## 🗂️ Our Projects 🗂️
### TrustyAI Explainability
The **[trustyai-explainability](https://github.com/trustyai-explainability/trustyai-explainability)** repo is our main hub, containing the **[TrustyAI Core Library](https://github.com/trustyai-explainability/trustyai-explainability/tree/main/explainability-core)** and **[TrustyAI Service](https://github.com/trustyai-explainability/trustyai-explainability/tree/main/explainability-service)**.

The **[TrustyAI Core Library](https://github.com/trustyai-explainability/trustyai-explainability/tree/main/explainability-core)** is a Java library for explainable and transparent AI, containing XAI algorithms, drift metrics, fairness metrics, and language model accuracy metrics. 

The **[TrustyAI Service](https://github.com/trustyai-explainability/trustyai-explainability/tree/main/explainability-service)** exposes TrustyAI Core as a containerized REST server, enabling responsible AI workflows in
cloud and distributed environments. The TrustyAI Service has the following integrations:
* Connectivity to Open Data Hub model servers
* Connectivity to Red Hat Openshift AI model servers
* KServe side-car explainer support
* MariaDB connectivity for storing model inferences

For example, you can deploy the TrustyAI service alongside KServe models in Open Data Hub to perform
drift and bias measurements throughout your deployment.


### TrustyAI Python Library
**[TrustyAI Python](https://github.com/trustyai-explainability/trustyai-explainability-python)** provides a Python interface to the TrustyAI Core library, which lets you use TrustyAI in more traditional data science environments like Jupyter. 


### Language Model Evaluation Service  
The **[LM-Eval K8s Service](https://github.com/trustyai-explainability/trustyai-service-operator/tree/main/controllers/lmes)** packages and serves EleutherAI's popular [LM-Evaluation-Harness](https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks) library in a Kubernetes environment, allowing for scalable evaluations running against K8s LLM servers such as vLLM. 


### Language Model Guardrails Project
The **[Guardrails project](https://github.com/trustyai-explainability/fms-guardrails-orchestrator)** provides a Kubernetes LLM guardrailing ecosystem, with dynamic, request-time pipelining of specific detectors and text chunkers. 


### TrustyAI Operator
The **[TrustyAI Kubernetes Operator](https://github.com/trustyai-explainability/trustyai-service-operator)** manages the deployment of various TrustyAI components into a Kubernetes cluster. The TrustyAI operator is a default component of both Open Data Hub and Red Hat Openshift AI.

While these are our largest and most active projects, also check out our [full list of repos](https://github.com/orgs/trustyai-explainability/repositories) to see more experimental work like [trustyai-detoxify-sft](https://github.com/trustyai-explainability/trustyai-detoxify-sft).

** **
##   📖 Resources 📖
### Documentation
- [Service and Operator Documentation](https://trustyai-explainability.github.io/trustyai-site/main/features.html)
- [Open Data Hub Documentation](https://opendatahub.io/docs/monitoring-data-science-models/#configuring-trustyai_monitor)
- [TrustyAI Python Documentation](https://trustyai-explainability-python.readthedocs.io/en/latest/)

### Tutorials
- [TrustyAI Website Tutorials](https://trustyai-explainability.github.io/trustyai-site/main/installing-opendatahub.html): Walkthroughs of a variety of different TrustyAI flows, like bias monitoring, drift monitoring, and language model evaluation.
- [trustyai-explainability-python-examples](https://github.com/trustyai-explainability/trustyai-explainability-python-examples): Examples on how to get started with the Python TrustyAI library.
- [trustyai-odh-demos](https://github.com/trustyai-explainability/odh-trustyai-demos): Demos of the TrustyAI Service within Open Data Hub.

### Demos
- Coming Soon

### Blog Posts
- [An Introduction to TrustyAI](https://www.redhat.com/en/blog/introduction-trustyai)
- [TrustyAI Detoxify: Guardrailing LLMs during training](https://developers.redhat.com/articles/2024/08/01/trustyai-detoxify-guardrailing-llms-during-training)

### Papers
- [TrustyAI Explainability Toolkit](https://arxiv.org/abs/2104.12717)

### Development Notes
* [TrustyAI Reference](https://github.com/trustyai-explainability/reference/tree/main) provides scratch notes on various common development and testing flows


** **
## 🤝 Join Us 🤝
Check out our [community repository](https://github.com/trustyai-explainability/community) for [discussions](https://github.com/orgs/trustyai-explainability/discussions) and our [Community Meeting information](https://github.com/trustyai-explainability/community?tab=readme-ov-file#community-meetings).

The [project roadmap](https://github.com/orgs/trustyai-explainability/projects/10) offers a view on new tools and integration the project developers are planning to add.

TrustyAI uses the [ODH governance model](https://github.com/opendatahub-io/opendatahub-community/blob/master/governance.md) and [code of conduct](https://github.com/opendatahub-io/opendatahub-community/blob/master/CODE_OF_CONDUCT.md).

### Links
- [Community Meeting Info](https://github.com/trustyai-explainability/community?tab=readme-ov-file#community-meetings)
- [Discussion Forum](https://github.com/orgs/trustyai-explainability/discussions)
- [Contribution Guidelines](https://github.com/trustyai-explainability/trustyai-explainability/blob/main/CONTRIBUTING.md)
- [Roadmap](https://github.com/orgs/trustyai-explainability/projects/10)

