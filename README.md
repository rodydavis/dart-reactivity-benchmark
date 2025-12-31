# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.31s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.61s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.14s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.40s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.42s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.92s |

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
| avoidablePropagation | 126.12ms | 2.36s | 204.70ms | 263.20ms | 254.64ms | 169.52ms |
| broadPropagation | 236.54ms | 4.31s | 449.37ms | 457.01ms | 452.80ms | 405.76ms |
| deepPropagation | 81.78ms | 1.47s | 162.92ms | 182.42ms | 129.78ms | 157.52ms |
| diamond | 158.63ms | 2.35s | 288.48ms | 316.70ms | 325.86ms | 215.47ms |
| mux | 302.88ms | 1.84s | 366.79ms | 389.33ms | 392.39ms | 367.58ms |
| repeatedObservers | 27.02ms | 224.55ms | 31.94ms | 42.16ms | 87.88ms | 58.71ms |
| triangle | 64.45ms | 730.98ms | 102.53ms | 117.95ms | 94.62ms | 84.06ms |
| unstable | 46.70ms | 342.19ms | 55.28ms | 74.11ms | 101.54ms | 342.66ms |
| molBench | 486.61ms | 589.88ms | 495.81ms | 486.67ms | 490.51ms | 492.50ms |
| create_signals | 33.58ms | 90.91ms | 5.51ms | 24.34ms | 71.36ms | 58.24ms |
| comp_0to1 | 12.25ms | 37.33ms | 17.89ms | 33.27ms | 41.01ms | 51.67ms |
| comp_1to1 | 16.59ms | 17.34ms | 12.49ms | 15.16ms | 25.63ms | 54.16ms |
| comp_2to1 | 13.83ms | 25.80ms | 14.24ms | 11.06ms | 13.61ms | 35.49ms |
| comp_4to1 | 2.31ms | 18.59ms | 8.77ms | 1.88ms | 4.37ms | 16.99ms |
| comp_1000to1 | 3μs | 16μs | 5μs | 26μs | 19μs | 38μs |
| comp_1to2 | 9.93ms | 39.52ms | 30.56ms | 32.64ms | 34.88ms | 46.30ms |
| comp_1to4 | 16.05ms | 23.59ms | 13.99ms | 25.48ms | 22.49ms | 46.66ms |
| comp_1to8 | 6.28ms | 21.75ms | 13.04ms | 9.96ms | 27.51ms | 43.62ms |
| comp_1to1000 | 6.35ms | 15.55ms | 3.77ms | 3.87ms | 14.53ms | 37.10ms |
| update_1to1 | 4.79ms | 25.33ms | 8.99ms | 31.02ms | 14.03ms | 6.10ms |
| update_2to1 | 4.78ms | 13.50ms | 4.49ms | 15.54ms | 7.27ms | 3.05ms |
| update_4to1 | 1.62ms | 6.16ms | 2.25ms | 7.76ms | 3.50ms | 1.55ms |
| update_1000to1 | 9μs | 67μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.71ms | 13.90ms | 4.42ms | 15.50ms | 6.97ms | 3.06ms |
| update_1to4 | 1.72ms | 7.05ms | 2.32ms | 7.79ms | 3.63ms | 1.52ms |
| update_1to1000 | 49μs | 162μs | 67μs | 66μs | 150μs | 374μs |
| cellx1000 | 5.93ms | 69.55ms | 9.58ms | 9.67ms | 12.13ms | 9.60ms |
| cellx2500 | 19.32ms | 268.69ms | 27.51ms | 27.50ms | 34.19ms | 34.60ms |
| cellx5000 | 49.95ms | 592.95ms | 71.82ms | 73.69ms | 97.96ms | 101.46ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.83ms | 1.93s | 495.79ms | 539.81ms | 319.91ms | 232.84ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.88ms | 1.45s | 285.73ms | 296.19ms | 220.86ms | 198.50ms |
| 1000x12 - 4 sources - dynamic (large) | 281.23ms | 1.79s | 4.15s | 3.66s | 448.41ms | 363.99ms |
| 1000x5 - 25 sources (wide dense) | 539.11ms | 3.46s | 3.35s | 3.52s | 828.96ms | 501.23ms |
| 5x500 - 3 sources (deep) | 158.35ms | 1.08s | 234.90ms | 238.50ms | 227.58ms | 205.60ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 246.52ms | 1.70s | 472.26ms | 494.21ms | 329.02ms | 260.66ms |

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
