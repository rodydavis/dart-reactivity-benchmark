# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.26s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.64s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.04s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.37s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.68s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.02s |

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
| avoidablePropagation | 126.36ms | 2.35s | 204.30ms | 264.39ms | 248.94ms | 168.06ms |
| broadPropagation | 236.44ms | 4.36s | 455.39ms | 453.55ms | 439.34ms | 415.28ms |
| deepPropagation | 80.56ms | 1.50s | 162.08ms | 175.02ms | 132.06ms | 155.05ms |
| diamond | 156.19ms | 2.38s | 292.21ms | 325.24ms | 304.60ms | 217.97ms |
| mux | 300.09ms | 1.82s | 373.99ms | 380.53ms | 382.46ms | 360.03ms |
| repeatedObservers | 27.26ms | 231.10ms | 32.15ms | 43.42ms | 90.66ms | 58.48ms |
| triangle | 65.00ms | 751.12ms | 101.54ms | 112.27ms | 95.92ms | 85.50ms |
| unstable | 45.99ms | 344.86ms | 56.29ms | 76.82ms | 101.99ms | 344.17ms |
| molBench | 488.10ms | 592.46ms | 494.16ms | 483.90ms | 488.79ms | 493.24ms |
| create_signals | 26.34ms | 87.33ms | 5.75ms | 27.36ms | 67.83ms | 62.41ms |
| comp_0to1 | 11.75ms | 41.42ms | 18.21ms | 26.59ms | 18.08ms | 56.02ms |
| comp_1to1 | 15.45ms | 34.88ms | 14.43ms | 8.03ms | 27.64ms | 58.05ms |
| comp_2to1 | 12.77ms | 16.93ms | 23.26ms | 12.11ms | 13.54ms | 38.36ms |
| comp_4to1 | 2.81ms | 24.34ms | 13.62ms | 5.79ms | 4.40ms | 17.43ms |
| comp_1000to1 | 3μs | 15μs | 6μs | 5μs | 19μs | 42μs |
| comp_1to2 | 14.97ms | 34.37ms | 12.83ms | 18.41ms | 35.54ms | 49.33ms |
| comp_1to4 | 14.22ms | 25.80ms | 26.57ms | 22.18ms | 22.09ms | 48.33ms |
| comp_1to8 | 5.83ms | 24.40ms | 7.00ms | 8.72ms | 23.77ms | 46.73ms |
| comp_1to1000 | 3.04ms | 15.74ms | 4.54ms | 3.82ms | 14.41ms | 42.66ms |
| update_1to1 | 4.24ms | 27.55ms | 8.88ms | 30.47ms | 13.93ms | 6.15ms |
| update_2to1 | 4.79ms | 13.72ms | 4.50ms | 15.20ms | 7.09ms | 3.07ms |
| update_4to1 | 1.69ms | 7.23ms | 2.28ms | 7.66ms | 3.49ms | 1.60ms |
| update_1000to1 | 9μs | 66μs | 41μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.78ms | 13.85ms | 4.42ms | 15.26ms | 6.95ms | 3.09ms |
| update_1to4 | 1.54ms | 6.93ms | 2.32ms | 7.63ms | 3.57ms | 1.51ms |
| update_1to1000 | 41μs | 160μs | 157μs | 65μs | 143μs | 435μs |
| cellx1000 | 6.19ms | 69.97ms | 9.57ms | 9.52ms | 11.54ms | 10.39ms |
| cellx2500 | 15.63ms | 255.18ms | 25.76ms | 26.15ms | 27.48ms | 33.00ms |
| cellx5000 | 34.30ms | 574.79ms | 71.41ms | 61.60ms | 68.97ms | 100.80ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.08ms | 1.94s | 494.75ms | 541.81ms | 324.98ms | 241.83ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.21ms | 1.45s | 279.71ms | 300.90ms | 223.07ms | 197.72ms |
| 1000x12 - 4 sources - dynamic (large) | 272.33ms | 1.87s | 4.28s | 3.74s | 445.47ms | 361.08ms |
| 1000x5 - 25 sources (wide dense) | 541.46ms | 3.39s | 3.50s | 3.44s | 831.17ms | 491.91ms |
| 5x500 - 3 sources (deep) | 153.25ms | 1.09s | 234.30ms | 241.24ms | 231.12ms | 210.36ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 246.62ms | 1.69s | 462.81ms | 489.73ms | 331.31ms | 260.02ms |

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
