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
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.14s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.25s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.82s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.17s |

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
| avoidablePropagation | 124.96ms | 2.38s | 204.90ms | 257.89ms | 254.50ms | 177.76ms |
| broadPropagation | 237.37ms | 4.33s | 457.22ms | 460.91ms | 442.48ms | 395.12ms |
| deepPropagation | 81.31ms | 1.48s | 162.66ms | 173.85ms | 133.75ms | 158.69ms |
| diamond | 157.06ms | 2.39s | 292.79ms | 315.83ms | 300.95ms | 216.12ms |
| mux | 294.69ms | 1.88s | 369.80ms | 379.82ms | 387.14ms | 366.27ms |
| repeatedObservers | 27.54ms | 230.00ms | 31.99ms | 42.27ms | 87.64ms | 58.75ms |
| triangle | 66.18ms | 754.36ms | 101.55ms | 111.22ms | 98.25ms | 90.99ms |
| unstable | 45.98ms | 348.68ms | 55.08ms | 74.78ms | 102.53ms | 344.40ms |
| molBench | 487.23ms | 590.15ms | 494.55ms | 486.97ms | 490.66ms | 493.75ms |
| create_signals | 26.48ms | 52.61ms | 4.95ms | 22.07ms | 74.43ms | 60.78ms |
| comp_0to1 | 11.79ms | 16.04ms | 20.53ms | 22.79ms | 41.03ms | 53.34ms |
| comp_1to1 | 15.42ms | 40.38ms | 14.67ms | 8.46ms | 37.82ms | 55.31ms |
| comp_2to1 | 24.24ms | 35.16ms | 19.42ms | 12.88ms | 25.05ms | 37.13ms |
| comp_4to1 | 2.50ms | 13.60ms | 18.32ms | 2.62ms | 4.38ms | 18.44ms |
| comp_1000to1 | 6μs | 20μs | 6μs | 7μs | 15μs | 40μs |
| comp_1to2 | 10.21ms | 38.75ms | 32.59ms | 24.13ms | 33.30ms | 45.81ms |
| comp_1to4 | 14.71ms | 23.65ms | 21.79ms | 21.50ms | 23.69ms | 45.48ms |
| comp_1to8 | 5.36ms | 24.18ms | 7.37ms | 10.58ms | 26.23ms | 43.41ms |
| comp_1to1000 | 3.41ms | 15.69ms | 4.81ms | 3.92ms | 14.61ms | 38.85ms |
| update_1to1 | 6.35ms | 25.71ms | 8.87ms | 30.68ms | 14.00ms | 6.10ms |
| update_2to1 | 4.85ms | 13.68ms | 4.50ms | 15.32ms | 7.14ms | 3.09ms |
| update_4to1 | 919μs | 7.29ms | 2.26ms | 7.75ms | 3.49ms | 1.59ms |
| update_1000to1 | 34μs | 69μs | 32μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.80ms | 12.41ms | 4.43ms | 15.44ms | 6.98ms | 3.12ms |
| update_1to4 | 900μs | 6.40ms | 2.29ms | 7.73ms | 3.58ms | 1.57ms |
| update_1to1000 | 43μs | 162μs | 166μs | 96μs | 141μs | 370μs |
| cellx1000 | 6.82ms | 79.28ms | 11.78ms | 10.06ms | 10.88ms | 11.39ms |
| cellx2500 | 21.78ms | 278.51ms | 28.95ms | 38.79ms | 36.38ms | 36.93ms |
| cellx5000 | 66.68ms | 641.98ms | 92.37ms | 95.96ms | 104.56ms | 128.55ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.54ms | 1.93s | 490.30ms | 537.91ms | 325.89ms | 244.90ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.97ms | 1.45s | 293.71ms | 296.48ms | 219.97ms | 200.85ms |
| 1000x12 - 4 sources - dynamic (large) | 283.50ms | 1.90s | 4.33s | 3.57s | 459.77ms | 374.75ms |
| 1000x5 - 25 sources (wide dense) | 534.75ms | 3.43s | 3.54s | 3.47s | 817.78ms | 493.33ms |
| 5x500 - 3 sources (deep) | 153.17ms | 1.10s | 231.26ms | 237.73ms | 229.53ms | 207.86ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 240.38ms | 1.64s | 465.32ms | 485.36ms | 325.64ms | 257.04ms |

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
