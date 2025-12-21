# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.29s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.65s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.05s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.41s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.43s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.15s |

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
| avoidablePropagation | 125.81ms | 2.38s | 200.66ms | 250.83ms | 235.96ms | 166.16ms |
| broadPropagation | 239.45ms | 4.34s | 447.81ms | 458.68ms | 443.69ms | 400.73ms |
| deepPropagation | 81.79ms | 1.51s | 161.04ms | 170.52ms | 131.99ms | 154.53ms |
| diamond | 159.29ms | 2.36s | 285.42ms | 313.47ms | 302.17ms | 248.54ms |
| mux | 293.20ms | 1.87s | 368.55ms | 379.05ms | 379.33ms | 359.78ms |
| repeatedObservers | 27.98ms | 224.90ms | 32.16ms | 41.70ms | 87.93ms | 62.52ms |
| triangle | 65.83ms | 743.80ms | 101.51ms | 110.28ms | 100.71ms | 90.89ms |
| unstable | 48.38ms | 336.70ms | 55.43ms | 73.80ms | 102.88ms | 352.17ms |
| molBench | 487.73ms | 590.31ms | 493.98ms | 483.79ms | 490.78ms | 494.09ms |
| create_signals | 26.33ms | 78.17ms | 5.53ms | 24.03ms | 71.88ms | 68.91ms |
| comp_0to1 | 12.46ms | 35.03ms | 18.03ms | 32.43ms | 41.12ms | 54.02ms |
| comp_1to1 | 15.92ms | 52.24ms | 11.04ms | 14.17ms | 37.96ms | 53.26ms |
| comp_2to1 | 15.48ms | 23.52ms | 18.36ms | 4.97ms | 27.31ms | 35.59ms |
| comp_4to1 | 3.11ms | 28.19ms | 15.65ms | 20.85ms | 4.34ms | 16.18ms |
| comp_1000to1 | 3μs | 15μs | 4μs | 6μs | 18μs | 39μs |
| comp_1to2 | 15.31ms | 38.85ms | 31.12ms | 22.25ms | 33.55ms | 44.24ms |
| comp_1to4 | 19.45ms | 24.08ms | 22.01ms | 11.55ms | 20.84ms | 43.77ms |
| comp_1to8 | 6.02ms | 23.85ms | 8.74ms | 6.14ms | 22.43ms | 41.91ms |
| comp_1to1000 | 3.10ms | 15.53ms | 8.75ms | 5.18ms | 14.40ms | 36.74ms |
| update_1to1 | 4.89ms | 27.49ms | 8.87ms | 30.59ms | 13.94ms | 6.10ms |
| update_2to1 | 4.80ms | 12.97ms | 4.59ms | 15.15ms | 7.18ms | 3.06ms |
| update_4to1 | 953μs | 7.38ms | 2.26ms | 7.66ms | 3.49ms | 1.52ms |
| update_1000to1 | 23μs | 85μs | 27μs | 76μs | 34μs | 15μs |
| update_1to2 | 3.30ms | 13.74ms | 4.41ms | 15.29ms | 6.98ms | 3.05ms |
| update_1to4 | 2.38ms | 6.95ms | 2.29ms | 7.64ms | 3.60ms | 1.50ms |
| update_1to1000 | 42μs | 173μs | 1.54ms | 66μs | 144μs | 373μs |
| cellx1000 | 7.78ms | 74.36ms | 9.50ms | 10.05ms | 9.40ms | 9.58ms |
| cellx2500 | 17.19ms | 267.06ms | 29.54ms | 28.90ms | 30.36ms | 28.13ms |
| cellx5000 | 39.09ms | 594.63ms | 87.63ms | 82.57ms | 86.86ms | 94.35ms |
| 10x5 - 2 sources - read 20.0% (simple) | 185.44ms | 1.96s | 494.79ms | 549.64ms | 320.92ms | 253.28ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.65ms | 1.47s | 285.93ms | 298.30ms | 219.84ms | 201.07ms |
| 1000x12 - 4 sources - dynamic (large) | 275.66ms | 1.85s | 4.12s | 3.74s | 446.56ms | 357.31ms |
| 1000x5 - 25 sources (wide dense) | 541.76ms | 3.44s | 3.40s | 3.47s | 798.88ms | 495.98ms |
| 5x500 - 3 sources (deep) | 154.04ms | 1.10s | 233.12ms | 239.29ms | 227.68ms | 207.38ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.10ms | 1.67s | 466.13ms | 487.79ms | 328.74ms | 259.09ms |

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
