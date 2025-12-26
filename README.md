# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.30s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.67s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.10s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.06s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.80s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.24s |

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
| avoidablePropagation | 125.79ms | 2.37s | 205.18ms | 253.87ms | 241.55ms | 167.85ms |
| broadPropagation | 237.40ms | 4.40s | 458.77ms | 462.68ms | 442.48ms | 401.42ms |
| deepPropagation | 81.70ms | 1.52s | 163.38ms | 176.00ms | 127.73ms | 156.81ms |
| diamond | 156.10ms | 2.42s | 296.81ms | 315.57ms | 300.15ms | 244.73ms |
| mux | 298.39ms | 1.84s | 375.87ms | 380.21ms | 380.83ms | 378.50ms |
| repeatedObservers | 27.62ms | 230.90ms | 32.15ms | 41.87ms | 87.94ms | 60.60ms |
| triangle | 65.18ms | 766.76ms | 103.99ms | 110.59ms | 95.39ms | 99.56ms |
| unstable | 45.97ms | 350.11ms | 55.56ms | 74.56ms | 101.75ms | 350.91ms |
| molBench | 486.75ms | 591.82ms | 494.78ms | 482.47ms | 489.54ms | 492.74ms |
| create_signals | 23.42ms | 70.20ms | 5.09ms | 27.96ms | 72.69ms | 62.45ms |
| comp_0to1 | 17.97ms | 28.07ms | 18.01ms | 23.48ms | 41.13ms | 52.02ms |
| comp_1to1 | 22.36ms | 31.96ms | 14.53ms | 7.74ms | 37.86ms | 52.39ms |
| comp_2to1 | 16.97ms | 37.11ms | 16.33ms | 12.30ms | 25.03ms | 35.35ms |
| comp_4to1 | 2.25ms | 16.06ms | 13.73ms | 6.82ms | 4.47ms | 15.55ms |
| comp_1000to1 | 4μs | 16μs | 5μs | 6μs | 15μs | 37μs |
| comp_1to2 | 9.73ms | 30.14ms | 32.98ms | 17.50ms | 29.81ms | 43.51ms |
| comp_1to4 | 22.96ms | 22.83ms | 21.39ms | 14.50ms | 34.99ms | 43.33ms |
| comp_1to8 | 5.42ms | 24.52ms | 6.79ms | 6.10ms | 28.82ms | 41.42ms |
| comp_1to1000 | 3.02ms | 15.35ms | 5.63ms | 4.30ms | 14.34ms | 36.97ms |
| update_1to1 | 5.77ms | 26.61ms | 9.02ms | 30.94ms | 13.97ms | 6.11ms |
| update_2to1 | 3.56ms | 13.15ms | 4.54ms | 15.40ms | 6.98ms | 3.15ms |
| update_4to1 | 2.22ms | 7.58ms | 2.27ms | 7.73ms | 3.53ms | 1.56ms |
| update_1000to1 | 23μs | 69μs | 23μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.76ms | 14.46ms | 4.44ms | 15.41ms | 7.57ms | 3.06ms |
| update_1to4 | 1.93ms | 7.01ms | 2.29ms | 7.74ms | 3.60ms | 1.52ms |
| update_1to1000 | 33μs | 164μs | 2.60ms | 93μs | 141μs | 359μs |
| cellx1000 | 5.58ms | 82.17ms | 9.81ms | 10.50ms | 10.01ms | 9.99ms |
| cellx2500 | 16.51ms | 261.76ms | 28.41ms | 29.67ms | 30.82ms | 34.63ms |
| cellx5000 | 46.33ms | 567.89ms | 84.74ms | 70.64ms | 107.14ms | 97.25ms |
| 10x5 - 2 sources - read 20.0% (simple) | 185.69ms | 1.92s | 495.75ms | 539.61ms | 320.86ms | 249.49ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.63ms | 1.46s | 280.79ms | 296.71ms | 217.93ms | 198.65ms |
| 1000x12 - 4 sources - dynamic (large) | 279.47ms | 1.93s | 4.33s | 3.56s | 445.80ms | 364.35ms |
| 1000x5 - 25 sources (wide dense) | 538.55ms | 3.42s | 3.51s | 3.33s | 819.45ms | 497.75ms |
| 5x500 - 3 sources (deep) | 155.10ms | 1.11s | 235.57ms | 237.49ms | 228.01ms | 208.76ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 246.47ms | 1.65s | 477.36ms | 492.09ms | 324.97ms | 257.62ms |

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
