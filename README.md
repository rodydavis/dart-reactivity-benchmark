# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.28s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.64s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.15s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.34s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.66s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.31s |

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
| avoidablePropagation | 125.47ms | 2.39s | 196.31ms | 258.65ms | 238.43ms | 170.50ms |
| broadPropagation | 235.30ms | 4.41s | 458.92ms | 454.90ms | 460.25ms | 396.65ms |
| deepPropagation | 80.48ms | 1.50s | 172.83ms | 178.80ms | 129.23ms | 156.45ms |
| diamond | 158.32ms | 2.40s | 290.99ms | 317.05ms | 312.73ms | 217.07ms |
| mux | 296.79ms | 1.85s | 381.49ms | 377.82ms | 386.28ms | 367.39ms |
| repeatedObservers | 27.13ms | 229.70ms | 32.11ms | 42.57ms | 88.50ms | 87.34ms |
| triangle | 66.00ms | 758.08ms | 106.40ms | 108.53ms | 110.49ms | 85.08ms |
| unstable | 45.53ms | 344.13ms | 54.81ms | 75.44ms | 103.42ms | 343.82ms |
| molBench | 484.07ms | 591.71ms | 494.65ms | 483.18ms | 485.37ms | 492.61ms |
| create_signals | 30.59ms | 52.12ms | 5.55ms | 25.43ms | 70.85ms | 61.68ms |
| comp_0to1 | 16.70ms | 15.66ms | 17.98ms | 23.79ms | 18.61ms | 54.90ms |
| comp_1to1 | 18.52ms | 40.94ms | 11.35ms | 7.78ms | 38.37ms | 57.03ms |
| comp_2to1 | 10.43ms | 23.72ms | 11.93ms | 8.09ms | 32.20ms | 37.30ms |
| comp_4to1 | 2.29ms | 33.82ms | 12.07ms | 1.83ms | 4.38ms | 16.82ms |
| comp_1000to1 | 7μs | 17μs | 5μs | 5μs | 30μs | 41μs |
| comp_1to2 | 10.70ms | 36.47ms | 26.62ms | 20.53ms | 40.72ms | 47.42ms |
| comp_1to4 | 13.42ms | 25.86ms | 22.28ms | 15.80ms | 31.81ms | 46.73ms |
| comp_1to8 | 9.40ms | 23.96ms | 9.25ms | 10.03ms | 32.30ms | 49.46ms |
| comp_1to1000 | 3.19ms | 17.56ms | 7.80ms | 4.29ms | 14.89ms | 40.01ms |
| update_1to1 | 4.79ms | 25.30ms | 10.36ms | 30.75ms | 13.97ms | 6.10ms |
| update_2to1 | 4.79ms | 13.82ms | 5.17ms | 15.22ms | 6.95ms | 3.09ms |
| update_4to1 | 1.24ms | 7.64ms | 2.26ms | 7.64ms | 3.47ms | 1.59ms |
| update_1000to1 | 15μs | 68μs | 30μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.75ms | 13.51ms | 4.42ms | 15.33ms | 7.61ms | 3.10ms |
| update_1to4 | 1.70ms | 7.16ms | 2.28ms | 7.67ms | 3.63ms | 1.56ms |
| update_1to1000 | 46μs | 163μs | 2.69ms | 65μs | 160μs | 395μs |
| cellx1000 | 5.40ms | 76.44ms | 9.96ms | 9.40ms | 9.58ms | 9.35ms |
| cellx2500 | 15.34ms | 295.17ms | 28.21ms | 25.66ms | 29.02ms | 31.56ms |
| cellx5000 | 51.92ms | 596.02ms | 87.90ms | 67.71ms | 81.56ms | 96.18ms |
| 10x5 - 2 sources - read 20.0% (simple) | 192.34ms | 1.96s | 495.24ms | 528.49ms | 323.31ms | 241.41ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.06ms | 1.46s | 287.62ms | 289.48ms | 220.74ms | 197.79ms |
| 1000x12 - 4 sources - dynamic (large) | 281.00ms | 1.91s | 4.22s | 3.81s | 462.37ms | 362.42ms |
| 1000x5 - 25 sources (wide dense) | 526.18ms | 3.41s | 3.49s | 3.41s | 826.40ms | 491.42ms |
| 5x500 - 3 sources (deep) | 153.25ms | 1.12s | 234.44ms | 234.08ms | 231.12ms | 206.98ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 245.53ms | 1.67s | 466.82ms | 482.08ms | 335.35ms | 261.10ms |

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
