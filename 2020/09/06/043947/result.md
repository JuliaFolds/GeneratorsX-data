# Benchmark result

* Pull request commit: [`8415b1a390ea2fc555ea9b1bb1720cde0d394684`](https://github.com/JuliaFolds/GeneratorsX.jl/commit/8415b1a390ea2fc555ea9b1bb1720cde0d394684)
* Pull request: <https://github.com/JuliaFolds/GeneratorsX.jl/pull/16> (Move foldl definition to FGenerators.jl)

# Judge result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmarks:
    - Target: 6 Sep 2020 - 04:38
    - Baseline: 6 Sep 2020 - 04:39
* Package commits:
    - Target: 6648e3
    - Baseline: b8038e
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
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   | 0.56 (5%) :white_check_mark: | 0.80 (1%) :white_check_mark: |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |                1.07 (5%) :x: |                   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       | 0.26 (5%) :white_check_mark: | 0.00 (1%) :white_check_mark: |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  |                1.09 (5%) :x: |                   1.00 (1%)  |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 0.07 (5%) :white_check_mark: | 0.00 (1%) :white_check_mark: |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      14716 s          0 s       1503 s      11030 s          0 s
       #2  2294 MHz       5758 s          0 s       1492 s      20066 s          0 s
       
  Memory: 6.7913818359375 GB (3267.796875 MB free)
  Uptime: 290.0 sec
  Load Avg:  1.021484375  0.6982421875  0.3115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

### Baseline
```
Julia Version 1.5.0-beta1.0
Commit 6443f6c95a (2020-05-28 17:42 UTC)
Platform Info:
  OS: Linux (x86_64-pc-linux-gnu)
      Ubuntu 18.04.5 LTS
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      18937 s          0 s       1564 s      13867 s          0 s
       #2  2294 MHz       8676 s          0 s       1552 s      24189 s          0 s
       
  Memory: 6.7913818359375 GB (3217.4921875 MB free)
  Uptime: 361.0 sec
  Load Avg:  1.072265625  0.78466796875  0.37451171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Target result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 6 Sep 2020 - 4:38
* Package commit: 6648e3
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.129 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 257.704 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   8.433 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |   6.300 μs (5%) |         |  32.50 KiB (1%) |         269 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 775.377 ns (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 350.207 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.290 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   1.920 μs (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  | 978.261 ns (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  | 472.198 ns (5%) |         |                 |             |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      14716 s          0 s       1503 s      11030 s          0 s
       #2  2294 MHz       5758 s          0 s       1492 s      20066 s          0 s
       
  Memory: 6.7913818359375 GB (3267.796875 MB free)
  Uptime: 290.0 sec
  Load Avg:  1.021484375  0.6982421875  0.3115234375
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
```

---
# Baseline result
# Benchmark Report for */home/runner/work/GeneratorsX.jl/GeneratorsX.jl*

## Job Properties
* Time of benchmark: 6 Sep 2020 - 4:39
* Package commit: b8038e
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
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :base"]` |   4.100 μs (5%) |         |  24.44 KiB (1%) |          10 |
| `["filter", ":reducer => :collect", ":impl => :base", ":src => :genx"]` | 265.703 μs (5%) |         |   1.26 MiB (1%) |        5056 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :base"]`   |   8.200 μs (5%) |         |  25.36 KiB (1%) |          43 |
| `["filter", ":reducer => :collect", ":impl => :xf", ":src => :genx"]`   |  11.300 μs (5%) |         |  40.70 KiB (1%) |         533 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :base"]`     | 800.000 ns (5%) |         |  704 bytes (1%) |          22 |
| `["filter", ":reducer => :sum", ":impl => :base", ":src => :genx"]`     | 348.303 μs (5%) |         | 851.80 KiB (1%) |        3721 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :base"]`       |   1.200 μs (5%) |         |  256 bytes (1%) |           9 |
| `["filter", ":reducer => :sum", ":impl => :xf", ":src => :genx"]`       |   7.300 μs (5%) |         |  11.67 KiB (1%) |         486 |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :base"]`  | 900.000 ns (5%) |         |                 |             |
| `["filter", ":reducer => :sum", ":impl => :xf_init", ":src => :genx"]`  |   6.500 μs (5%) |         |  11.67 KiB (1%) |         486 |

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
  uname: Linux 5.3.0-1035-azure #36-Ubuntu SMP Thu Aug 6 09:21:33 UTC 2020 x86_64 x86_64
  CPU: Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz: 
              speed         user         nice          sys         idle          irq
       #1  2294 MHz      18937 s          0 s       1564 s      13867 s          0 s
       #2  2294 MHz       8676 s          0 s       1552 s      24189 s          0 s
       
  Memory: 6.7913818359375 GB (3217.4921875 MB free)
  Uptime: 361.0 sec
  Load Avg:  1.072265625  0.78466796875  0.37451171875
  WORD_SIZE: 64
  LIBM: libopenlibm
  LLVM: libLLVM-9.0.1 (ORCJIT, broadwell)
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
    Model:               79
    Model name:          Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz
    Stepping:            1
    CPU MHz:             2294.682
    BogoMIPS:            4589.36
    Hypervisor vendor:   Microsoft
    Virtualization type: full
    L1d cache:           32K
    L1i cache:           32K
    L2 cache:            256K
    L3 cache:            51200K
    NUMA node0 CPU(s):   0,1
    Flags:               fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc rep_good nopl xtopology cpuid pni pclmulqdq ssse3 fma cx16 pcid sse4_1 sse4_2 movbe popcnt aes xsave avx f16c rdrand hypervisor lahf_lm abm 3dnowprefetch invpcid_single pti fsgsbase bmi1 hle avx2 smep bmi2 erms invpcid rtm rdseed adx smap xsaveopt md_clear
    

| Cpu Property       | Value                                                   |
|:------------------ |:------------------------------------------------------- |
| Brand              | Intel(R) Xeon(R) CPU E5-2673 v4 @ 2.30GHz               |
| Vendor             | :Intel                                                  |
| Architecture       | :Broadwell                                              |
| Model              | Family: 0x06, Model: 0x4f, Stepping: 0x01, Type: 0x00   |
| Cores              | 2 physical cores, 2 logical cores (on executing CPU)    |
|                    | No Hyperthreading detected                              |
| Clock Frequencies  | Not supported by CPU                                    |
| Data Cache         | Level 1:3 : (32, 256, 51200) kbytes                     |
|                    | 64 byte cache line size                                 |
| Address Size       | 48 bits virtual, 46 bits physical                       |
| SIMD               | 256 bit = 32 byte max. SIMD vector size                 |
| Time Stamp Counter | TSC is accessible via `rdtsc`                           |
|                    | TSC increased at every clock cycle (non-invariant TSC)  |
| Perf. Monitoring   | Performance Monitoring Counters (PMC) are not supported |
| Hypervisor         | Yes, Microsoft                                          |

