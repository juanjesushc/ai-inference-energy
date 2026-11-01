# Understanding the Energy Use of Multimodal AI Inference Across the Compute Continuum: Current Trends and Future Scenarios

**J.J. Hernández-Carlón¹, A. Mauro², A.M. Tulino², J. Llorca¹**

¹ Centre Tecnològic de Telecomunicacions de Catalunya (CTTC), Spain
² University of Naples Federico II (UNINA), Italy

📄 [Read the manuscript (PDF)](Understanding_the_Energy_Use_of_Multimodal_AI_Inference_Across_the_Compute_Continuum__Current_Trends_and_Future_Scenarios.pdf)

**Index Terms:** AI inference, multimodal AI, energy efficiency, edge computing, service placement, cloud network flow, PUE

---

## Abstract

AI inference can be executed in hyperscale core data centers, metropolitan edge sites, or compute-enabled access nodes, and the choice has a first-order impact on energy: inner tiers operate more efficient facilities, but reaching them requires hauling data across the network. We study this trade-off through a Cloud Network Flow model that represents the computation, memory, and communication requirements of multimodal AI inference as flows over a multidimensional infrastructure graph, charges every resource — accelerators, router ports, and optical channels — with an idle-plus-load-proportional power model that includes host, over-provisioning, and facility overheads, and solves energy-optimal placement, routing, and resource allocation as a mixed-integer linear program subject to end-to-end latency constraints. We show in closed form that optimal placement is driven by two workload descriptors — the computation-to-communication ratio and the computation-to-memory ratio — together with infrastructure descriptors that capture the energy efficiency of each resource across tiers. We validate the resulting placement rule against the MILP optimum across representative generative and analytics services, and quantify how efficiency gains, accelerator memory and throughput scaling, facility-efficiency evolution, and tightening latency budgets reshape placement and total power across the continuum.

---

## Summary

This work is the extended version of a study on where AI inference should run along the core–edge–access compute continuum to minimize energy. It models computation, memory, and communication with a Cloud Network Flow formulation, derives per-request resource demands analytically from model architecture (autoregressive, diffusion, and discriminative paradigms), and obtains a closed-form, threshold-based placement rule driven by the computation-to-communication and computation-to-memory ratios.

Compared with the conference-length paper, this version adds the full service and infrastructure models, end-to-end latency constraints, facility-efficiency (PUE) scenarios, and a heterogeneous accelerator estate. In the reference setting, generative services favor the core, video analytics the access tier, and augmented reality the edge. Latency budgets act as a veto that removes tiers, while energy chooses among the remaining ones. Memory-bound services benefit from added accelerator memory, whereas added throughput at unchanged efficiency can increase power.
