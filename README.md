# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.34s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.72s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.15s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.40s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.62s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.57s |

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
| avoidablePropagation | 129.15ms | 2.38s | 203.04ms | 257.78ms | 251.38ms | 164.94ms |
| broadPropagation | 249.71ms | 4.43s | 451.52ms | 455.24ms | 442.33ms | 407.76ms |
| deepPropagation | 83.70ms | 1.51s | 163.10ms | 177.06ms | 131.31ms | 157.58ms |
| diamond | 157.83ms | 2.40s | 295.86ms | 318.97ms | 303.63ms | 220.55ms |
| mux | 307.44ms | 1.88s | 378.41ms | 377.33ms | 383.43ms | 372.24ms |
| repeatedObservers | 26.89ms | 233.40ms | 31.79ms | 42.01ms | 89.02ms | 58.72ms |
| triangle | 65.06ms | 759.57ms | 101.89ms | 111.48ms | 95.27ms | 86.10ms |
| unstable | 50.60ms | 347.56ms | 56.37ms | 75.27ms | 104.45ms | 343.60ms |
| molBench | 489.36ms | 590.53ms | 494.94ms | 488.08ms | 487.69ms | 494.03ms |
| create_signals | 27.72ms | 53.28ms | 4.95ms | 25.26ms | 73.68ms | 63.61ms |
| comp_0to1 | 14.18ms | 15.50ms | 18.59ms | 30.75ms | 18.14ms | 58.32ms |
| comp_1to1 | 15.92ms | 47.45ms | 13.33ms | 7.98ms | 29.45ms | 59.76ms |
| comp_2to1 | 16.23ms | 35.78ms | 17.46ms | 14.23ms | 25.66ms | 39.32ms |
| comp_4to1 | 4.19ms | 25.85ms | 12.75ms | 1.86ms | 8.66ms | 18.96ms |
| comp_1000to1 | 4μs | 15μs | 4μs | 4μs | 45μs | 44μs |
| comp_1to2 | 15.70ms | 36.51ms | 31.48ms | 16.98ms | 24.87ms | 49.99ms |
| comp_1to4 | 19.86ms | 18.10ms | 22.76ms | 15.36ms | 28.02ms | 49.86ms |
| comp_1to8 | 6.00ms | 21.64ms | 8.22ms | 6.38ms | 20.92ms | 48.48ms |
| comp_1to1000 | 3.28ms | 15.52ms | 9.82ms | 4.54ms | 14.38ms | 43.97ms |
| update_1to1 | 7.81ms | 23.12ms | 9.08ms | 30.61ms | 13.98ms | 6.09ms |
| update_2to1 | 4.73ms | 11.18ms | 4.51ms | 15.21ms | 6.94ms | 3.05ms |
| update_4to1 | 989μs | 6.23ms | 2.28ms | 7.62ms | 3.52ms | 2.07ms |
| update_1000to1 | 9μs | 55μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.72ms | 10.97ms | 4.43ms | 15.31ms | 6.98ms | 3.06ms |
| update_1to4 | 1.58ms | 8.22ms | 2.29ms | 7.75ms | 3.62ms | 1.49ms |
| update_1to1000 | 44μs | 157μs | 1.85ms | 99μs | 150μs | 424μs |
| cellx1000 | 5.75ms | 82.19ms | 9.83ms | 11.65ms | 16.96ms | 12.64ms |
| cellx2500 | 18.30ms | 279.84ms | 33.04ms | 31.99ms | 51.98ms | 43.84ms |
| cellx5000 | 42.18ms | 644.85ms | 88.40ms | 101.81ms | 127.51ms | 128.91ms |
| 10x5 - 2 sources - read 20.0% (simple) | 191.27ms | 1.99s | 494.33ms | 537.97ms | 323.24ms | 245.25ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.17ms | 1.51s | 284.43ms | 298.58ms | 220.72ms | 198.37ms |
| 1000x12 - 4 sources - dynamic (large) | 279.65ms | 1.86s | 4.26s | 3.78s | 456.34ms | 378.49ms |
| 1000x5 - 25 sources (wide dense) | 533.67ms | 3.49s | 3.40s | 3.41s | 816.77ms | 491.35ms |
| 5x500 - 3 sources (deep) | 157.89ms | 1.18s | 232.46ms | 239.04ms | 232.22ms | 208.69ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 250.10ms | 1.68s | 468.09ms | 485.07ms | 336.02ms | 262.55ms |

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
