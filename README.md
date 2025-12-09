# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.28s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.61s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.13s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.34s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.38s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.25s |

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
| avoidablePropagation | 125.69ms | 2.31s | 204.30ms | 263.49ms | 281.33ms | 166.49ms |
| broadPropagation | 237.10ms | 4.41s | 456.22ms | 453.51ms | 445.40ms | 392.04ms |
| deepPropagation | 80.98ms | 1.52s | 160.76ms | 171.56ms | 139.06ms | 158.10ms |
| diamond | 159.03ms | 2.33s | 291.54ms | 328.40ms | 304.50ms | 221.17ms |
| mux | 293.73ms | 1.86s | 369.73ms | 385.36ms | 387.89ms | 352.03ms |
| repeatedObservers | 27.91ms | 223.73ms | 32.00ms | 42.82ms | 87.66ms | 59.20ms |
| triangle | 65.58ms | 754.53ms | 107.39ms | 112.03ms | 96.60ms | 84.22ms |
| unstable | 46.22ms | 338.29ms | 55.70ms | 74.75ms | 102.58ms | 350.85ms |
| molBench | 487.30ms | 589.49ms | 494.48ms | 510.72ms | 487.44ms | 493.38ms |
| create_signals | 26.88ms | 70.66ms | 15.69ms | 28.93ms | 110.14ms | 59.34ms |
| comp_0to1 | 11.91ms | 28.65ms | 21.93ms | 20.48ms | 18.35ms | 52.48ms |
| comp_1to1 | 15.44ms | 40.84ms | 7.11ms | 8.10ms | 38.41ms | 53.46ms |
| comp_2to1 | 15.60ms | 36.16ms | 12.08ms | 15.12ms | 13.06ms | 39.13ms |
| comp_4to1 | 4.68ms | 24.28ms | 26.24ms | 1.86ms | 11.19ms | 15.86ms |
| comp_1000to1 | 3μs | 15μs | 10μs | 5μs | 17μs | 38μs |
| comp_1to2 | 11.44ms | 35.89ms | 20.33ms | 16.64ms | 26.16ms | 43.85ms |
| comp_1to4 | 16.44ms | 26.08ms | 29.06ms | 12.60ms | 19.14ms | 43.57ms |
| comp_1to8 | 4.60ms | 24.24ms | 7.82ms | 6.86ms | 22.17ms | 41.48ms |
| comp_1to1000 | 3.09ms | 15.56ms | 7.07ms | 4.96ms | 13.86ms | 36.98ms |
| update_1to1 | 4.92ms | 23.13ms | 8.89ms | 30.63ms | 13.93ms | 6.14ms |
| update_2to1 | 3.29ms | 10.21ms | 4.48ms | 15.16ms | 7.11ms | 3.10ms |
| update_4to1 | 1.75ms | 7.04ms | 2.22ms | 7.90ms | 3.48ms | 1.61ms |
| update_1000to1 | 9μs | 66μs | 33μs | 77μs | 35μs | 15μs |
| update_1to2 | 4.74ms | 13.84ms | 4.46ms | 15.23ms | 6.99ms | 3.14ms |
| update_1to4 | 1.52ms | 6.94ms | 2.26ms | 7.67ms | 3.58ms | 1.59ms |
| update_1to1000 | 44μs | 162μs | 929μs | 64μs | 148μs | 370μs |
| cellx1000 | 6.29ms | 77.30ms | 9.49ms | 10.09ms | 9.36ms | 9.66ms |
| cellx2500 | 16.38ms | 266.76ms | 29.46ms | 29.72ms | 30.73ms | 32.34ms |
| cellx5000 | 40.08ms | 581.12ms | 86.42ms | 91.97ms | 88.73ms | 124.02ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.90ms | 1.96s | 494.48ms | 538.09ms | 327.21ms | 231.99ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.78ms | 1.47s | 283.62ms | 298.29ms | 218.13ms | 193.22ms |
| 1000x12 - 4 sources - dynamic (large) | 283.90ms | 1.93s | 4.25s | 3.76s | 449.30ms | 374.57ms |
| 1000x5 - 25 sources (wide dense) | 538.58ms | 3.51s | 3.19s | 3.35s | 817.85ms | 494.73ms |
| 5x500 - 3 sources (deep) | 155.78ms | 1.12s | 231.21ms | 235.57ms | 227.19ms | 205.61ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 248.34ms | 1.63s | 460.87ms | 484.59ms | 325.70ms | 260.90ms |

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
