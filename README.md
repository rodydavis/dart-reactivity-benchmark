# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.58s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.17s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.29s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.37s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.34s |

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
| avoidablePropagation | 125.49ms | 2.40s | 200.29ms | 258.16ms | 262.61ms | 170.86ms |
| broadPropagation | 244.36ms | 4.42s | 453.41ms | 445.53ms | 455.43ms | 401.24ms |
| deepPropagation | 82.01ms | 1.52s | 164.97ms | 168.65ms | 134.27ms | 157.66ms |
| diamond | 161.16ms | 2.41s | 290.26ms | 314.47ms | 320.72ms | 206.43ms |
| mux | 304.85ms | 1.87s | 369.21ms | 381.08ms | 374.66ms | 366.40ms |
| repeatedObservers | 27.65ms | 233.13ms | 31.98ms | 42.03ms | 88.19ms | 58.61ms |
| triangle | 65.71ms | 767.23ms | 101.62ms | 110.01ms | 95.50ms | 84.79ms |
| unstable | 46.19ms | 351.19ms | 54.83ms | 75.64ms | 102.67ms | 342.43ms |
| molBench | 485.33ms | 590.31ms | 494.25ms | 485.86ms | 491.80ms | 492.51ms |
| create_signals | 30.52ms | 84.74ms | 4.87ms | 30.19ms | 114.43ms | 59.41ms |
| comp_0to1 | 11.27ms | 15.60ms | 17.62ms | 26.30ms | 19.70ms | 50.87ms |
| comp_1to1 | 15.57ms | 49.52ms | 12.72ms | 7.84ms | 36.35ms | 53.73ms |
| comp_2to1 | 12.88ms | 30.16ms | 9.59ms | 11.78ms | 25.82ms | 35.82ms |
| comp_4to1 | 2.75ms | 31.38ms | 9.05ms | 4.44ms | 12.45ms | 16.08ms |
| comp_1000to1 | 4μs | 27μs | 5μs | 4μs | 31μs | 38μs |
| comp_1to2 | 16.50ms | 39.06ms | 28.34ms | 23.14ms | 35.07ms | 44.44ms |
| comp_1to4 | 18.83ms | 18.58ms | 21.53ms | 19.64ms | 30.91ms | 44.38ms |
| comp_1to8 | 6.14ms | 21.54ms | 7.76ms | 9.92ms | 32.26ms | 42.20ms |
| comp_1to1000 | 3.33ms | 15.37ms | 5.19ms | 3.96ms | 14.75ms | 38.23ms |
| update_1to1 | 3.65ms | 21.05ms | 8.97ms | 30.56ms | 13.95ms | 6.10ms |
| update_2to1 | 5.02ms | 10.85ms | 4.49ms | 15.25ms | 6.94ms | 3.05ms |
| update_4to1 | 991μs | 5.86ms | 2.28ms | 8.50ms | 3.50ms | 1.56ms |
| update_1000to1 | 9μs | 52μs | 44μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.74ms | 10.54ms | 4.48ms | 15.26ms | 7.58ms | 3.09ms |
| update_1to4 | 1.95ms | 5.25ms | 2.38ms | 7.64ms | 3.57ms | 1.58ms |
| update_1to1000 | 41μs | 155μs | 157μs | 65μs | 142μs | 380μs |
| cellx1000 | 6.22ms | 79.97ms | 9.62ms | 9.58ms | 10.23ms | 10.25ms |
| cellx2500 | 18.26ms | 277.11ms | 26.30ms | 27.61ms | 29.25ms | 30.62ms |
| cellx5000 | 36.80ms | 589.23ms | 69.75ms | 66.39ms | 68.47ms | 84.10ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.71ms | 1.93s | 491.06ms | 538.74ms | 324.77ms | 241.04ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.01ms | 1.49s | 283.72ms | 296.07ms | 218.37ms | 197.38ms |
| 1000x12 - 4 sources - dynamic (large) | 268.33ms | 1.87s | 4.30s | 3.61s | 451.61ms | 365.65ms |
| 1000x5 - 25 sources (wide dense) | 527.29ms | 3.43s | 3.19s | 3.52s | 820.05ms | 495.71ms |
| 5x500 - 3 sources (deep) | 150.92ms | 1.10s | 237.51ms | 240.70ms | 232.59ms | 210.25ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.63ms | 1.66s | 459.71ms | 482.44ms | 331.31ms | 262.48ms |

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
