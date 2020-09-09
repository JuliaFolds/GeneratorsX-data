# Benchmark result

* Pull request commit: [`4d7d7153b8449a6605eabb1e98b336720adb83b9`](https://github.com/JuliaFolds/GeneratorsX.jl/commit/4d7d7153b8449a6605eabb1e98b336720adb83b9)
* Pull request: <https://github.com/JuliaFolds/GeneratorsX.jl/pull/16> (Move foldl definition to FGenerators.jl)

# Judge result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 9 Sep 2020 - 05:05
    - Baseline: 9 Sep 2020 - 05:06
* Package commits:
    - Target: b1b59a
    - Baseline: 6c368d
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

| ID                                                                      | time ratio                   | memory ratio                 |
|-------------------------------------------------------------------------|------------------------------|------------------------------|
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |                1.22 (5%) :x: |                   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |                1.08 (5%) :x: |                   1.00 (1%)  |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   | 0.58 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 0.87 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       | 0.84 (5%) :white_check_mark: |                   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       | 0.23 (5%) :white_check_mark: | 0.00 (1%) :white_check_mark: |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 0.05 (5%) :white_check_mark: | 0.00 (1%) :white_check_mark: |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      11819 s          0 s       1109 s      39033 s          0 s
       #2  2397 MHz       9408 s          0 s       1697 s      41219 s          0 s
       
  Memory: 6.764892578125 GB (3146.515625 MB free)
  Uptime: 538.0 sec
  Load Avg:  1.0322265625  0.7607421875  0.4140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

### Baseline
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.4.0-1023-azure #23~18.04.1-Ubuntu SMP Thu Aug 20 14:46:48 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      18046 s          0 s       1172 s      40229 s          0 s
       #2  2397 MHz      10619 s          0 s       1736 s      47489 s          0 s
       
  Memory: 6.764892578125 GB (3114.08203125 MB free)
  Uptime: 614.0 sec
  Load Avg:  1.0068359375  0.81689453125  0.4638671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Target result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 9 Sep 2020 - 5:5
* Package commit: b1b59a
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   5.750 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 301.314 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   8.100 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |   6.775 μs (5%) |         |  32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 873.115 ns (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 375.218 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.350 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   2.222 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.070 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 437.904 ns (5%) |         |                 |             |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      11819 s          0 s       1109 s      39033 s          0 s
       #2  2397 MHz       9408 s          0 s       1697 s      41219 s          0 s
       
  Memory: 6.764892578125 GB (3146.515625 MB free)
  Uptime: 538.0 sec
  Load Avg:  1.0322265625  0.7607421875  0.4140625
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 9 Sep 2020 - 5:6
* Package commit: 6c368d
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.700 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 299.611 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   7.500 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |  11.600 μs (5%) |         |  40.70 KiB (1%) |         533 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     |   1.000 μs (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 383.714 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.600 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   9.500 μs (5%) |         |  11.67 KiB (1%) |         486 |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |   1.100 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  |   8.900 μs (5%) |         |  11.67 KiB (1%) |         486 |

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
  CPU: Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz: 
              speed         user         nice          sys         idle          irq
       #1  2397 MHz      18046 s          0 s       1172 s      40229 s          0 s
       #2  2397 MHz      10619 s          0 s       1736 s      47489 s          0 s
       
  Memory: 6.764892578125 GB (3114.08203125 MB free)
  Uptime: 614.0 sec
  Load Avg:  1.0068359375  0.81689453125  0.4638671875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, haswell)
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
    Model:               63
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz
    Stepping:            2
    CPU MHz:             2397.225
    BogoMIPS:            4794.45
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            30720K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm invpcid_single pti fsgsbase bmi1 avx2 smep bmi2 erms invpcid xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v3 @ 2.40GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Haswell                                                |
| Model              | Family: 0x06, Model: 0x3f, Stepping: 0x02, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 30720) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 44 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

