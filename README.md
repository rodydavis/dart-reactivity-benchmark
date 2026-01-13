# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.23s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.58s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.06s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.27s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.54s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.48s |

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
| avoidablePropagation | 125.51ms | 2.39s | 205.29ms | 253.13ms | 247.44ms | 167.41ms |
| broadPropagation | 237.54ms | 4.47s | 446.00ms | 459.09ms | 451.78ms | 394.63ms |
| deepPropagation | 81.14ms | 1.55s | 160.77ms | 170.51ms | 129.33ms | 156.06ms |
| diamond | 155.55ms | 2.42s | 292.21ms | 314.94ms | 305.59ms | 210.03ms |
| mux | 295.81ms | 1.89s | 371.78ms | 374.78ms | 372.11ms | 362.68ms |
| repeatedObservers | 27.61ms | 228.53ms | 32.01ms | 41.72ms | 89.82ms | 58.60ms |
| triangle | 68.38ms | 759.91ms | 102.60ms | 108.37ms | 98.11ms | 84.34ms |
| unstable | 49.58ms | 341.79ms | 54.76ms | 73.89ms | 104.87ms | 342.41ms |
| molBench | 485.81ms | 591.10ms | 495.53ms | 482.54ms | 489.53ms | 492.34ms |
| create_signals | 27.40ms | 81.51ms | 4.81ms | 29.36ms | 67.52ms | 68.50ms |
| comp_0to1 | 11.67ms | 16.23ms | 17.86ms | 23.00ms | 17.98ms | 51.16ms |
| comp_1to1 | 15.32ms | 43.75ms | 14.47ms | 7.96ms | 31.62ms | 53.45ms |
| comp_2to1 | 15.21ms | 30.14ms | 18.44ms | 11.66ms | 17.96ms | 35.13ms |
| comp_4to1 | 2.71ms | 25.60ms | 8.54ms | 4.30ms | 15.17ms | 16.18ms |
| comp_1000to1 | 4μs | 15μs | 5μs | 5μs | 32μs | 38μs |
| comp_1to2 | 15.70ms | 36.23ms | 16.01ms | 23.14ms | 39.32ms | 43.73ms |
| comp_1to4 | 14.18ms | 29.51ms | 25.13ms | 28.47ms | 31.57ms | 43.27ms |
| comp_1to8 | 6.01ms | 19.95ms | 7.31ms | 8.41ms | 32.97ms | 41.04ms |
| comp_1to1000 | 3.46ms | 15.84ms | 4.91ms | 4.26ms | 14.78ms | 37.04ms |
| update_1to1 | 5.75ms | 22.08ms | 8.89ms | 30.56ms | 13.94ms | 6.10ms |
| update_2to1 | 4.86ms | 10.69ms | 4.52ms | 15.17ms | 6.93ms | 3.09ms |
| update_4to1 | 1.22ms | 5.28ms | 2.23ms | 7.66ms | 3.50ms | 1.62ms |
| update_1000to1 | 9μs | 51μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.73ms | 10.85ms | 4.41ms | 15.25ms | 7.60ms | 3.10ms |
| update_1to4 | 2.31ms | 5.32ms | 2.28ms | 7.68ms | 3.66ms | 1.57ms |
| update_1to1000 | 41μs | 157μs | 165μs | 65μs | 154μs | 376μs |
| cellx1000 | 7.03ms | 79.18ms | 9.34ms | 9.56ms | 9.60ms | 9.22ms |
| cellx2500 | 15.79ms | 235.37ms | 26.20ms | 25.85ms | 28.80ms | 27.76ms |
| cellx5000 | 36.62ms | 547.56ms | 67.36ms | 60.67ms | 69.11ms | 89.68ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.11ms | 2.01s | 493.90ms | 544.43ms | 320.69ms | 250.09ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.98ms | 1.49s | 285.86ms | 298.69ms | 219.41ms | 205.44ms |
| 1000x12 - 4 sources - dynamic (large) | 263.63ms | 1.84s | 4.25s | 3.60s | 457.59ms | 363.04ms |
| 1000x5 - 25 sources (wide dense) | 520.71ms | 3.48s | 3.41s | 3.50s | 808.19ms | 492.64ms |
| 5x500 - 3 sources (deep) | 152.86ms | 1.12s | 226.70ms | 243.20ms | 227.74ms | 208.72ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 240.59ms | 1.68s | 466.42ms | 483.34ms | 327.64ms | 263.14ms |

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
