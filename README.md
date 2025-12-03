# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.29s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.64s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.04s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.11s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.50s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.10s |

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
| avoidablePropagation | 125.88ms | 2.40s | 201.80ms | 254.06ms | 237.53ms | 168.73ms |
| broadPropagation | 238.50ms | 4.50s | 453.67ms | 463.30ms | 445.49ms | 412.13ms |
| deepPropagation | 80.83ms | 1.49s | 161.48ms | 170.18ms | 128.75ms | 162.07ms |
| diamond | 157.18ms | 2.36s | 286.34ms | 320.24ms | 302.69ms | 214.33ms |
| mux | 293.29ms | 1.84s | 368.70ms | 380.40ms | 371.21ms | 358.36ms |
| repeatedObservers | 27.58ms | 231.84ms | 32.84ms | 42.72ms | 87.86ms | 58.75ms |
| triangle | 65.26ms | 742.53ms | 101.69ms | 110.49ms | 97.33ms | 83.73ms |
| unstable | 46.30ms | 343.22ms | 54.66ms | 74.68ms | 102.15ms | 343.63ms |
| molBench | 486.87ms | 587.77ms | 495.12ms | 482.09ms | 489.09ms | 492.69ms |
| create_signals | 27.87ms | 70.72ms | 5.70ms | 24.15ms | 107.96ms | 65.54ms |
| comp_0to1 | 15.38ms | 28.68ms | 17.66ms | 26.49ms | 24.39ms | 59.67ms |
| comp_1to1 | 19.93ms | 38.84ms | 14.53ms | 7.76ms | 36.80ms | 60.69ms |
| comp_2to1 | 23.40ms | 34.97ms | 20.25ms | 9.57ms | 27.31ms | 41.68ms |
| comp_4to1 | 2.94ms | 13.66ms | 11.74ms | 6.62ms | 8.94ms | 15.76ms |
| comp_1000to1 | 6μs | 16μs | 8μs | 5μs | 18μs | 38μs |
| comp_1to2 | 13.89ms | 36.33ms | 15.60ms | 21.82ms | 33.68ms | 43.35ms |
| comp_1to4 | 19.25ms | 17.95ms | 30.70ms | 16.28ms | 22.26ms | 43.54ms |
| comp_1to8 | 5.61ms | 21.12ms | 7.94ms | 10.29ms | 23.99ms | 41.67ms |
| comp_1to1000 | 3.10ms | 15.43ms | 5.03ms | 4.13ms | 14.22ms | 37.52ms |
| update_1to1 | 4.00ms | 24.54ms | 8.91ms | 30.64ms | 14.37ms | 6.10ms |
| update_2to1 | 4.78ms | 13.68ms | 4.50ms | 15.21ms | 7.28ms | 3.05ms |
| update_4to1 | 1.60ms | 6.75ms | 2.21ms | 7.63ms | 3.58ms | 1.55ms |
| update_1000to1 | 9μs | 75μs | 33μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.78ms | 13.59ms | 4.41ms | 15.33ms | 7.13ms | 3.05ms |
| update_1to4 | 1.53ms | 6.82ms | 2.25ms | 7.71ms | 3.70ms | 1.50ms |
| update_1to1000 | 42μs | 160μs | 149μs | 65μs | 159μs | 363μs |
| cellx1000 | 5.79ms | 81.09ms | 9.53ms | 9.63ms | 11.74ms | 9.29ms |
| cellx2500 | 15.77ms | 284.19ms | 26.97ms | 28.23ms | 28.84ms | 26.92ms |
| cellx5000 | 42.51ms | 590.72ms | 67.59ms | 68.93ms | 63.23ms | 81.72ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.53ms | 1.95s | 494.46ms | 539.44ms | 320.80ms | 241.90ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.75ms | 1.46s | 279.63ms | 296.96ms | 219.22ms | 199.60ms |
| 1000x12 - 4 sources - dynamic (large) | 284.14ms | 1.84s | 4.23s | 3.43s | 440.45ms | 359.99ms |
| 1000x5 - 25 sources (wide dense) | 530.47ms | 3.32s | 3.39s | 3.51s | 811.00ms | 496.91ms |
| 5x500 - 3 sources (deep) | 154.57ms | 1.08s | 228.11ms | 239.43ms | 221.50ms | 205.30ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 246.36ms | 1.65s | 462.63ms | 486.52ms | 327.50ms | 293.95ms |

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
