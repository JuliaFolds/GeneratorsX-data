# Benchmark result

* Pull request commit: [`763602f50bf0a158b06438da3a78f598f42f0a71`](https://github.com/JuliaFolds/GeneratorsX.jl/commit/763602f50bf0a158b06438da3a78f598f42f0a71)
* Pull request: <https://github.com/JuliaFolds/GeneratorsX.jl/pull/13> (Use BenchmarkCI.pushresult)

# Judge result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 27 Jul 2020 - 05:23
    - Baseline: 27 Jul 2020 - 05:24
* Package commits:
    - Target: 6f082b
    - Baseline: 6b41f8
* Julia commits:
    - Target: 6443f6
    - Baseline: 6443f6
* Julia command flags:
    - Target: None
    - Baseline: None
* Environment variables:
    - Target: None
    - Baseline: None

## Results
A ratio greater than `1.0` denotes a possible regression (marked with :x:), while a ratio less
than `1.0` denotes a possible improvement (marked with :white_check_mark:). Only significant results - results
that indicate possible regressions or improvements - are shown below (thus, an empty table means that all
benchmark results remained invariant between builds).

| ID                                                                      | time ratio                   | memory ratio |
|-------------------------------------------------------------------------|------------------------------|--------------|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |                1.15 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   | 0.94 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       | 0.92 (5%) :white_check_mark: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 0.87 (5%) :white_check_mark: |   1.00 (1%)  |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo

### Target
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8724 s          0 s       1350 s      13554 s          0 s
       #2  2095 MHz      11674 s          0 s       1446 s      11139 s          0 s
       
  Memory: 6.764884948730469 GB (3154.39453125 MB free)
  Uptime: 257.0 sec
  Load Avg:  1.1005859375  0.76806640625  0.3447265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

### Baseline
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      14491 s          0 s       1406 s      14918 s          0 s
       #2  2095 MHz      13068 s          0 s       1477 s      16906 s          0 s
       
  Memory: 6.764884948730469 GB (3128.328125 MB free)
  Uptime: 329.0 sec
  Load Avg:  1.029296875  0.8193359375  0.39501953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 27 Jul 2020 - 5:23
* Package commit: 6f082b
* Julia commit: 6443f6
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                      | time            | GC time | memory          | allocations |
|-------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.520 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 276.507 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.101 μs (5%) |         |  26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |  12.300 μs (5%) |         |  40.70 KiB (1%) |         533 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 920.033 ns (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 352.409 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.478 μs (5%) |         |  912 bytes (1%) |          31 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   9.600 μs (5%) |         |  11.67 KiB (1%) |         486 |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.220 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  |   7.600 μs (5%) |         |  11.67 KiB (1%) |         486 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz       8724 s          0 s       1350 s      13554 s          0 s
       #2  2095 MHz      11674 s          0 s       1446 s      11139 s          0 s
       
  Memory: 6.764884948730469 GB (3154.39453125 MB free)
  Uptime: 257.0 sec
  Load Avg:  1.1005859375  0.76806640625  0.3447265625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 27 Jul 2020 - 5:24
* Package commit: 6b41f8
* Julia commit: 6443f6
* Julia command flags: None
* Environment variables: None

## Results
Below is a table of this job's results, obtained by running the benchmarks.
The values listed in the `ID` column have the structure `[parent_group, child_group, ..., key]`, and can be used to
index into the BaseBenchmarks suite to retrieve the corresponding benchmarks.
The percentages accompanying time and memory values in the below table are noise tolerances. The "true"
time/memory value for a given benchmark is expected to fall within this percentage of the reported value.
An empty cell means that the value was zero.

| ID                                                                      | time            | GC time | memory          | allocations |
|-------------------------------------------------------------------------|----------------:|--------:|----------------:|------------:|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.800 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 281.104 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.700 μs (5%) |         |  26.11 KiB (1%) |          67 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |  12.500 μs (5%) |         |  40.70 KiB (1%) |         533 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.000 μs (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 367.105 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   2.700 μs (5%) |         |  912 bytes (1%) |          31 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   9.800 μs (5%) |         |  11.67 KiB (1%) |         486 |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.200 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  |   8.700 μs (5%) |         |  11.67 KiB (1%) |         486 |

## Benchmark Group List
Here's a list of all the benchmark groups executed by this job:

- `["filter", ":reducer => :collect", ":impl => :base"]`
- `["filter", ":reducer => :collect", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :base"]`
- `["filter", ":reducer => :sum", ":impl => :xf"]`
- `["filter", ":reducer => :sum", ":impl => :xf_init"]`

## Julia versioninfo
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.4 LTS
  uname: Linux 5.3.0-1032-azure #33~18.04.1-Ubuntu SMP Fri Jun 26 15:01:15 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      14491 s          0 s       1406 s      14918 s          0 s
       #2  2095 MHz      13068 s          0 s       1477 s      16906 s          0 s
       
  Memory: 6.764884948730469 GB (3128.328125 MB free)
  Uptime: 329.0 sec
  Load Avg:  1.029296875  0.8193359375  0.39501953125
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Runtime information
| Runtime Info | |
|:--|:--|
| BLAS #threads | 2 |
| `BLAS.vendor()` | `openblas64` |
| `Sys.CPU_THREADS` | 2 |

`lscpu` output:

    Architecture:        x86_64
    CPU op-mode(s):      32-bit, 64-bit
    Byte Order:          Little Endian
    CPU(s):              2
    On-line CPU(s) list: 0,1
    Thread(s) per core:  1
    Core(s) per socket:  2
    Socket(s):           1
    NUMA node(s):        1
    Vendor ID:           GenuineIntel
    CPU family:          6
    Model:               85
    Model name:          Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz
    Stepping:            4
    CPU MHz:             2095.077
    BogoMIPS:            4190.15
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            1024K
    L3 cache:            36608K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm mpx avx512f avx512dq rdseed adx smap clflushopt avx512cd avx512bw avx512vl xsaveopt xsavec xsaves md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz           |
| Vendor             | :Intel                                                  |
| Architecture       | :Skylake                                                |
| Model              | Family: 0x06, Model: 0x55, Stepping: 0x04, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 1024, 36608) kbytes                    |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

