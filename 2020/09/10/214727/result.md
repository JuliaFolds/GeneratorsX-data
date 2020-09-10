# Benchmark result

* Pull request commit: [`17ba88ca07ab869be45c2ff876adba38166a0a8d`](https://github.com/JuliaFolds/GeneratorsX.jl/commit/17ba88ca07ab869be45c2ff876adba38166a0a8d)
* Pull request: <https://github.com/JuliaFolds/GeneratorsX.jl/pull/22> (Setup Aqua)

# Judge result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 10 Sep 2020 - 21:45
    - Baseline: 10 Sep 2020 - 21:47
* Package commits:
    - Target: 25507a
    - Baseline: 0b9332
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

| ID                                                                      | time ratio    | memory ratio |
|-------------------------------------------------------------------------|---------------|--------------|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` | 1.12 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       | 1.08 (5%) :x: |   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 1.31 (5%) :x: |   1.00 (1%)  |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15903 s          0 s       1823 s      75486 s          0 s
       #2  2095 MHz       6110 s          0 s       1714 s      85862 s          0 s
       
  Memory: 6.791389465332031 GB (3048.23046875 MB free)
  Uptime: 954.0 sec
  Load Avg:  0.87158203125  0.42529296875  0.2333984375
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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      16609 s          0 s       1848 s      81459 s          0 s
       #2  2095 MHz      12112 s          0 s       1756 s      86541 s          0 s
       
  Memory: 6.791389465332031 GB (3027.08203125 MB free)
  Uptime: 1021.0 sec
  Load Avg:  0.9619140625  0.54833984375  0.29248046875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Target result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 10 Sep 2020 - 21:45
* Package commit: 25507a
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.700 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 301.602 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.100 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |   6.775 μs (5%) |         |  32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.010 μs (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 389.601 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.620 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   1.860 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.300 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 784.615 ns (5%) |         |                 |             |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      15903 s          0 s       1823 s      75486 s          0 s
       #2  2095 MHz       6110 s          0 s       1714 s      85862 s          0 s
       
  Memory: 6.791389465332031 GB (3048.23046875 MB free)
  Uptime: 954.0 sec
  Load Avg:  0.87158203125  0.42529296875  0.2333984375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, skylake)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 10 Sep 2020 - 21:47
* Package commit: 0b9332
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.100 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 303.400 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   9.200 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |   6.700 μs (5%) |         |  32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.000 μs (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 388.200 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.500 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   1.800 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.300 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 600.000 ns (5%) |         |                 |             |

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
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) Platinum 8171M CPU @ 2.60GHz: 
              speed         user         nice          sys         idle          irq
       #1  2095 MHz      16609 s          0 s       1848 s      81459 s          0 s
       #2  2095 MHz      12112 s          0 s       1756 s      86541 s          0 s
       
  Memory: 6.791389465332031 GB (3027.08203125 MB free)
  Uptime: 1021.0 sec
  Load Avg:  0.9619140625  0.54833984375  0.29248046875
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
    CPU MHz:             2095.082
    BogoMIPS:            4190.16
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
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 512 bit = 64 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

