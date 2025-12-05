# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.91s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.03s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.73s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.19s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.35s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 25.70s |

<!-- ranking end -->

### **Failed Tests**

<!-- fail start -->
| Framework | Success Rate | Tests | Time |
|-----------|--------------|-------|------|

<!-- fail end -->

## Benchmark results of each framework

<!-- test-case start -->
| Test Case | [alien_signals](https://github.com/medz/alien-signals-dart) | [mobx](https://github.com/mobxjs/mobx.dart) | [preact_signals](https://pub.dev/packages/preact_signals) | [signals_core](https://github.com/rodydavis/signals.dart) | [solidart](https://github.com/nank1ro/solidart) | [state_beacon](https://github.com/jinyus/dart_beacon) |
|---|---|---|---|---|---|---|
| avoidablePropagation | 132.59ms | 2.22s | 182.04ms | 229.52ms | 238.06ms | 156.22ms |
| broadPropagation | 219.19ms | 4.12s | 404.82ms | 384.30ms | 426.83ms | 351.16ms |
| deepPropagation | 86.75ms | 1.44s | 182.03ms | 177.39ms | 132.18ms | 163.12ms |
| diamond | 146.76ms | 2.24s | 253.98ms | 302.69ms | 304.48ms | 205.68ms |
| mux | 285.76ms | 1.72s | 333.32ms | 336.90ms | 379.22ms | 309.43ms |
| repeatedObservers | 22.57ms | 218.25ms | 28.59ms | 36.41ms | 93.20ms | 50.84ms |
| triangle | 61.14ms | 726.76ms | 93.98ms | 100.76ms | 102.19ms | 83.64ms |
| unstable | 41.67ms | 314.99ms | 50.32ms | 61.41ms | 110.38ms | 324.42ms |
| molBench | 360.06ms | 475.71ms | 387.66ms | 367.22ms | 369.09ms | 386.81ms |
| create_signals | 26.78ms | 69.09ms | 15.29ms | 31.95ms | 66.68ms | 58.64ms |
| comp_0to1 | 18.21ms | 27.88ms | 16.41ms | 28.32ms | 43.48ms | 49.75ms |
| comp_1to1 | 20.02ms | 34.80ms | 18.00ms | 10.22ms | 40.18ms | 52.26ms |
| comp_2to1 | 10.97ms | 20.50ms | 17.70ms | 9.60ms | 13.62ms | 34.52ms |
| comp_4to1 | 2.78ms | 26.21ms | 18.53ms | 2.68ms | 15.75ms | 16.03ms |
| comp_1000to1 | 5μs | 20μs | 5μs | 8μs | 15μs | 38μs |
| comp_1to2 | 9.90ms | 33.18ms | 16.50ms | 27.04ms | 28.36ms | 44.47ms |
| comp_1to4 | 20.06ms | 23.82ms | 22.51ms | 21.63ms | 32.73ms | 44.58ms |
| comp_1to8 | 7.08ms | 23.89ms | 9.55ms | 14.05ms | 24.41ms | 42.91ms |
| comp_1to1000 | 8.00ms | 14.90ms | 7.78ms | 5.40ms | 14.40ms | 37.80ms |
| update_1to1 | 4.04ms | 19.31ms | 7.69ms | 26.65ms | 13.67ms | 5.15ms |
| update_2to1 | 1.62ms | 9.81ms | 3.87ms | 13.19ms | 7.07ms | 2.49ms |
| update_4to1 | 854μs | 5.22ms | 2.00ms | 6.76ms | 3.52ms | 1.19ms |
| update_1000to1 | 9μs | 50μs | 17μs | 70μs | 35μs | 12μs |
| update_1to2 | 1.65ms | 9.70ms | 3.78ms | 13.32ms | 6.86ms | 2.79ms |
| update_1to4 | 867μs | 4.93ms | 2.08ms | 6.72ms | 3.45ms | 1.20ms |
| update_1to1000 | 63μs | 184μs | 423μs | 77μs | 149μs | 378μs |
| cellx1000 | 9.45ms | 75.22ms | 9.42ms | 11.47ms | 13.85ms | 11.09ms |
| cellx2500 | 25.60ms | 232.04ms | 25.47ms | 32.27ms | 37.28ms | 33.41ms |
| cellx5000 | 57.52ms | 517.92ms | 66.83ms | 86.62ms | 86.26ms | 85.66ms |
| 10x5 - 2 sources - read 20.0% (simple) | 172.96ms | 1.94s | 411.76ms | 450.12ms | 313.10ms | 225.12ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 152.31ms | 1.44s | 240.11ms | 254.10ms | 232.66ms | 170.41ms |
| 1000x12 - 4 sources - dynamic (large) | 240.18ms | 1.57s | 3.16s | 3.04s | 379.73ms | 283.86ms |
| 1000x5 - 25 sources (wide dense) | 382.57ms | 3.36s | 2.59s | 2.63s | 631.17ms | 377.91ms |
| 5x500 - 3 sources (deep) | 176.29ms | 1.14s | 218.05ms | 213.96ms | 271.29ms | 204.48ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 202.49ms | 1.63s | 386.41ms | 422.45ms | 290.34ms | 213.41ms |

<!-- test-case end -->

> [!TIP]
> - `(fail)`: Test case failed
> - `(partial)`: Partial of the test cases failed

## Integrate into your project

You can easily integrate Dart reactivity benchmark into your project to provide benchmarking.

### Install it

```bash
dart pub add dev:reactivity_benchmark
```

### Writing Tests

```dart
class YourReactiveFramework extends ReactiveFramework {
  ...
}

void main() {
  final framework = YourReactiveFramework();
  runFrameworkBench(framework);
}
```

## Local run benchmarks

Dart VM
```bash
dart run frameworks/[framework_name].dart
```

Run all benchamrks
```bash
bash bench.sh
```
