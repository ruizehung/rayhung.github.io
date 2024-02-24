---
title: "Pareto-Secure Machine Learning (PSML): Fingerprinting and Securing Inference Serving Systems"
collection: publications
permalink: /publication/psml
excerpt: 'With the emergence of large foundational models, model-serving systems are becoming popular. In such a system, users send the queries to the server and specify the desired performance metrics (e.g., accuracy, latency, etc.). The server maintains a set of models (model zoo) in the back-end and serves the queries based on the specified metrics. This paper examines the security, specifically robustness against model extraction attacks, of such systems. We propose a query-efficient fingerprinting algorithm to enable the attacker to trigger any desired model consistently. We show that by using our fingerprinting algorithm, model extraction can have fidelity and accuracy scores within 1% of the scores obtained if attacking in a single-model setting and up to 14.6% gain in accuracy and up to 7.7% gain in fidelity compared to the naive attack.....'
date: 2023-07-20
venue: "arXiv preprint arXiv:2307.01292"
paperurl: 'https://arxiv.org/abs/2307.01292'
citation: 'arXiv:2307.01292'
---

With the emergence of large foundational models, model-serving systems are becoming popular. In such a system, users send the queries to the server and specify the desired performance metrics (e.g., accuracy, latency, etc.). The server maintains a set of models (model zoo) in the back-end and serves the queries based on the specified metrics. This paper examines the security, specifically robustness against model extraction attacks, of such systems. Existing black-box attacks cannot be directly applied to extract a victim model, as models hide among the model zoo behind the inference serving interface, and attackers cannot identify which model is being used. An intermediate step is required to ensure that every input query gets the output from the victim model. To this end, we propose a query-efficient fingerprinting algorithm to enable the attacker to trigger any desired model consistently. We show that by using our fingerprinting algorithm, model extraction can have fidelity and accuracy scores within 1% of the scores obtained if attacking in a single-model setting and up to 14.6% gain in accuracy and up to 7.7% gain in fidelity compared to the naive attack. Finally, we counter the proposed attack with a noise-based defense mechanism that thwarts fingerprinting by adding noise to the specified performance metrics. Our defense strategy reduces the attack's accuracy and fidelity by up to 9.8% and 4.8%, respectively (on medium-sized model extraction). We show that the proposed defense induces a fundamental trade-off between the level of protection and system goodput, achieving configurable and significant victim model extraction protection while maintaining acceptable goodput (>80%). We provide anonymous access to our code.


[Download paper here](https://arxiv.org/abs/2307.01292)
