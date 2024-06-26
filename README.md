# Description
This repository is a dataset of profiled pytorch modules on different GPUs. The dataset is created for research purposes.
# Dataset Organization
The dataset is organized in CSV format, where each row is a profiled kernel for a test case and the columns are:

|GPU|Module|Batch Size|Data size|kernel|Duration|Memory Throughput|DRAM Throughput|L1/TEX Cache Throughput|L2 Cache Throughput|Compute (SM) Throughput|Block Size|Grid Size|Waves Per SM|Achieved Occupancy|Registers Per Thread|Shared Memory Configuration Size|Driver Shared Memory Per Block|Dynamic Shared Memory Per Block|Static Shared Memory Per Block|
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|

* where:
  - GPU: GPU name where module is executed
  - Module: Module invocation as described in pytorch documentation [here](https://pytorch.org/docs/stable/nn.html)
  - Batch Size: batch size of input data
  - Data Size: width x height of 2d data (for ReLU it is width x height x channels)
  - kernel: Name of launched kernel
  - Duration: Exection time in (nsec)
  - Memory Throughput: refer to NCU documentation [here](https://docs.nvidia.com/nsight-compute/ProfilingGuide/), measured as (%)
  - DRAM Throughput: refer to NCU documentation [here](https://docs.nvidia.com/nsight-compute/ProfilingGuide/), measured as (%)
  - L1/TEX Cache Throughput: refer to NCU documentation [here](https://docs.nvidia.com/nsight-compute/ProfilingGuide/), measured as (%)
  - L2 Cache Throughput: refer to NCU documentation [here](https://docs.nvidia.com/nsight-compute/ProfilingGuide/), measured as (%)
  - Compute (SM) Throughput: refer to NCU documentation [here](https://docs.nvidia.com/nsight-compute/ProfilingGuide/), measured as (%)
  - Block Size: Number of threads in a 3D block (x,y,z)
  - Grid Size: Number of blocks in 3D grid (x,y,z)
  - Waves Per SM: refer to [here](https://developer.nvidia.com/blog/cuda-pro-tip-minimize-the-tail-effect/)
  - Achieved Occupancy: refer to [here](https://docs.nvidia.com/gameworks/content/developertools/desktop/analysis/report/cudaexperiments/kernellevel/achievedoccupancy.htm)

# Contact:
For inquiry and contribution contact:
- Mahmoud Alasmar (m.r.m.alasmar@rug.nl)

