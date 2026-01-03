# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.35s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.55s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.11s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.14s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.28s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.35s |

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
| avoidablePropagation | 129.70ms | 2.40s | 201.66ms | 252.78ms | 257.00ms | 173.34ms |
| broadPropagation | 237.49ms | 4.48s | 444.26ms | 454.72ms | 446.69ms | 400.31ms |
| deepPropagation | 82.86ms | 1.52s | 166.11ms | 173.05ms | 132.39ms | 161.06ms |
| diamond | 159.33ms | 2.42s | 290.40ms | 314.82ms | 322.31ms | 206.73ms |
| mux | 297.77ms | 1.85s | 372.12ms | 379.66ms | 382.43ms | 360.62ms |
| repeatedObservers | 27.66ms | 234.44ms | 32.00ms | 41.51ms | 90.90ms | 59.00ms |
| triangle | 66.62ms | 758.13ms | 103.49ms | 112.53ms | 97.35ms | 86.43ms |
| unstable | 48.88ms | 342.63ms | 55.43ms | 74.18ms | 101.85ms | 343.71ms |
| molBench | 487.66ms | 590.63ms | 495.26ms | 487.82ms | 493.24ms | 492.83ms |
| create_signals | 28.04ms | 70.49ms | 5.14ms | 27.35ms | 124.06ms | 57.73ms |
| comp_0to1 | 11.68ms | 28.26ms | 17.91ms | 23.22ms | 18.93ms | 50.77ms |
| comp_1to1 | 16.18ms | 32.24ms | 14.34ms | 7.89ms | 42.33ms | 53.75ms |
| comp_2to1 | 24.46ms | 35.42ms | 17.38ms | 12.91ms | 19.82ms | 35.66ms |
| comp_4to1 | 2.61ms | 24.38ms | 11.36ms | 2.00ms | 4.41ms | 16.77ms |
| comp_1000to1 | 4μs | 15μs | 5μs | 5μs | 19μs | 37μs |
| comp_1to2 | 9.80ms | 34.23ms | 17.88ms | 21.89ms | 34.54ms | 46.77ms |
| comp_1to4 | 20.09ms | 18.94ms | 24.42ms | 16.27ms | 21.84ms | 46.10ms |
| comp_1to8 | 6.52ms | 23.30ms | 8.09ms | 10.66ms | 22.50ms | 42.07ms |
| comp_1to1000 | 5.88ms | 15.44ms | 6.03ms | 4.65ms | 14.27ms | 36.80ms |
| update_1to1 | 5.92ms | 29.33ms | 8.93ms | 30.62ms | 13.94ms | 6.11ms |
| update_2to1 | 4.82ms | 15.32ms | 4.48ms | 15.16ms | 7.10ms | 3.11ms |
| update_4to1 | 1.83ms | 7.75ms | 2.21ms | 7.65ms | 3.49ms | 1.62ms |
| update_1000to1 | 9μs | 70μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 6.23ms | 15.23ms | 4.42ms | 15.23ms | 6.96ms | 3.11ms |
| update_1to4 | 1.42ms | 7.75ms | 2.26ms | 7.66ms | 3.57ms | 1.56ms |
| update_1to1000 | 42μs | 163μs | 484μs | 80μs | 143μs | 361μs |
| cellx1000 | 5.68ms | 71.52ms | 9.42ms | 9.57ms | 11.08ms | 9.41ms |
| cellx2500 | 21.09ms | 246.49ms | 25.64ms | 27.07ms | 25.62ms | 28.30ms |
| cellx5000 | 45.06ms | 552.31ms | 63.83ms | 70.49ms | 60.40ms | 90.33ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.27ms | 1.98s | 500.54ms | 537.29ms | 324.35ms | 237.62ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.11ms | 1.48s | 281.97ms | 298.91ms | 218.74ms | 196.98ms |
| 1000x12 - 4 sources - dynamic (large) | 317.57ms | 1.90s | 4.09s | 3.60s | 439.75ms | 355.95ms |
| 1000x5 - 25 sources (wide dense) | 536.02ms | 3.42s | 3.29s | 3.38s | 814.97ms | 475.77ms |
| 5x500 - 3 sources (deep) | 154.54ms | 1.11s | 227.17ms | 241.35ms | 227.43ms | 207.90ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.81ms | 1.63s | 476.36ms | 485.48ms | 329.46ms | 258.95ms |

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
