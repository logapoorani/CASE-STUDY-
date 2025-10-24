# CASE-STUDY-
## 212223060136

Case Study Title: Resource Allocation and Cost Optimization in an OpenStack Private Cloud

Case Overview:

ABC Cloud Services runs a private cloud using OpenStack to host virtual machines (VMs) for internal development, testing, and production workloads. Their cloud infrastructure comprises:

5 Compute Nodes, each with:
64 vCPUs
256 GB RAM
2 TB SSD storage
OpenStack Services Deployed:
Nova (Compute)
Neutron (Networking)
Cinder (Block Storage)
Glance (Image Management)
Keystone (Identity)
Horizon (Dashboard)
Heat (Orchestration)

They are considering expanding their cloud but want to first evaluate current capacity usage, VM density, and cost efficiency. The goal is to calculate whether their resource usage aligns with business needs and how to optimize it.

Case Study Questions – OpenStack Calculation in Cloud Computing

1. Resource Utilization:

Based on the current infrastructure, what is the total available compute capacity in terms of:
Total vCPUs
Total RAM
Total storage

2.Storage Allocation:

Given 10 TB of total block storage across the cloud, how many VMs can be supported if:
a) Each VM is allocated 100 GB block storage
b) Snapshot storage consumes 20% extra on average

*SOLUTIONS:*

Problem 1 — Encryption Time Calculation
Scenario: A company uses AES-256 encryption to secure data before uploading it to the cloud. It takes 0.05 seconds to encrypt 1 MB of data. We must calculate how long it takes to encrypt 2 TB.
Step 1: Convert 2 TB into MB.
1 TB = 1024 GB and 1 GB = 1024 MB.
2 TB = 2 × 1024 × 1024 = 2,097,152 MB.
Step 2: Calculate total time.
Time = 0.05 × 2,097,152 = 104,857.6 seconds.
Step 3: Convert seconds to hours.
104,857.6 ÷ 3600 = 29.13 hours ≈ 29 hours, 7 minutes, 38 seconds.
Interpretation:
It will take about 29 hours to encrypt 2 TB of data. The process can be optimized by parallel encryption or hardware acceleration.
Final Answer: ≈ 29 hours (104,857.6 seconds).

Problem 2 — CPU Utilization Efficiency
Scenario: A virtual machine (VM) is allocated 8 vCPUs but uses only 5.5 on average. Find its CPU utilization efficiency.
Step 1: Use the formula:
Efficiency = (Used ÷ Allocated) × 100
= (5.5 ÷ 8) × 100 = 68.75%.
Interpretation:
The VM uses around 69% of its available CPU power. The remaining 31% is idle. This indicates under-utilization, and the company could reduce vCPU allocation to save costs.
Final Answer: 68.75% CPU utilization efficiency.


Problem 3 — Network Throughput Efficiency
Scenario: A cloud server has 1 Gbps bandwidth but uses only 600 Mbps during peak hours.
Step 1: Formula:
Efficiency = (Used ÷ Maximum) × 100
= (600 ÷ 1000) × 100 = 60%.
Interpretation:
Only 60% of the network’s potential is used. The rest (40%) acts as a buffer for traffic spikes. In practice, maintaining some headroom helps ensure stability, but continuous 60% usage means resources could be optimized.
Final Answer: 60% network throughput efficiency.

Problem 4 — Energy Efficiency
Scenario: Two setups complete the same workload: - Setup A: 500W for 2 hours.
- Setup B: 300W for 3.5 hours.
Step 1: Calculate total energy used.
Energy (Wh) = Power × Time. - Setup A = 500 × 2 = 1000 Wh (1.00 kWh). - Setup B = 300 × 3.5 = 1050 Wh (1.05 kWh).
Step 2: Compare the results.
Setup A consumes less energy for the same task.
Interpretation:
Setup A is slightly more efficient, using 0.05 kWh less. Although it draws higher power, it finishes faster, leading to less overall energy use.
Final Answer: Setup A is more energy-efficient.

Problem 5 — CPU Utilization Efficiency (Server Hosting)
Scenario: A physical server has 16 cores. Each virtual machine (VM) uses 2 cores, and optimal CPU utilization is 75%. We must find how many VMs can be efficiently hosted.
Step 1: Find total usable cores at 75% utilization.
Usable cores = 16 × 0.75 = 12 cores.
Step 2: Find maximum number of VMs.
Each VM uses 2 cores → 12 ÷ 2 = 6 VMs.
Interpretation:
At 75% utilization, the server can efficiently handle up to 6 virtual machines without overloading. Adding more VMs could lead to CPU contention and performance drops.
Final Answer: 6 VMs can be efficiently hosted.
