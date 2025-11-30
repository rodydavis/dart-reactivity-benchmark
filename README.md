# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.16s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 3.54s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.03s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 8.18s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 8.45s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 17.65s |

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
| avoidablePropagation | 82.56ms | 1.42s | 118.30ms | 143.71ms | 162.27ms | 164.72ms |
| broadPropagation | 128.67ms | 2.73s | 269.43ms | 261.75ms | 237.27ms | 427.55ms |
| deepPropagation | 57.64ms | 957.29ms | 125.66ms | 126.32ms | 87.24ms | 182.76ms |
| diamond | 102.37ms | 1.51s | 182.56ms | 195.64ms | 196.10ms | 232.80ms |
| mux | 185.77ms | 1.19s | 240.15ms | 239.88ms | 275.56ms | 262.52ms |
| repeatedObservers | 16.14ms | 137.78ms | 19.82ms | 23.18ms | 53.15ms | 39.30ms |
| triangle | 43.41ms | 517.67ms | 71.31ms | 72.13ms | 67.47ms | 60.26ms |
| unstable | 32.22ms | 214.39ms | 35.45ms | 41.04ms | 68.96ms | 238.93ms |
| molBench | 327.36ms | 395.33ms | 332.70ms | 329.94ms | 339.63ms | 328.46ms |
| create_signals | 18.93ms | 41.63ms | 6.96ms | 19.37ms | 98.37ms | 39.34ms |
| comp_0to1 | 3.21ms | 18.31ms | 17.76ms | 10.06ms | 26.11ms | 33.13ms |
| comp_1to1 | 10.20ms | 27.26ms | 5.22ms | 4.12ms | 15.41ms | 35.92ms |
| comp_2to1 | 15.41ms | 23.50ms | 8.88ms | 6.85ms | 13.06ms | 24.74ms |
| comp_4to1 | 2.52ms | 8.61ms | 6.59ms | 2.02ms | 3.49ms | 11.41ms |
| comp_1000to1 | 2μs | 10μs | 4μs | 3μs | 16μs | 26μs |
| comp_1to2 | 5.50ms | 25.56ms | 8.82ms | 13.87ms | 24.25ms | 29.96ms |
| comp_1to4 | 10.06ms | 11.25ms | 13.30ms | 12.73ms | 13.27ms | 28.88ms |
| comp_1to8 | 3.31ms | 14.50ms | 7.98ms | 5.51ms | 13.58ms | 28.41ms |
| comp_1to1000 | 2.41ms | 10.43ms | 2.56ms | 2.96ms | 9.42ms | 25.61ms |
| update_1to1 | 2.15ms | 11.84ms | 4.75ms | 15.65ms | 6.90ms | 3.34ms |
| update_2to1 | 1.06ms | 5.95ms | 2.29ms | 7.70ms | 3.77ms | 1.60ms |
| update_4to1 | 549μs | 2.98ms | 1.17ms | 3.48ms | 1.74ms | 1.05ms |
| update_1000to1 | 5μs | 27μs | 12μs | 34μs | 18μs | 8μs |
| update_1to2 | 1.05ms | 5.66ms | 2.41ms | 7.03ms | 3.42ms | 1.62ms |
| update_1to4 | 545μs | 2.79ms | 1.21ms | 3.45ms | 1.81ms | 791μs |
| update_1to1000 | 17μs | 127μs | 22μs | 31μs | 90μs | 253μs |
| cellx1000 | 3.88ms | 47.70ms | 6.24ms | 6.28ms | 7.19ms | 10.79ms |
| cellx2500 | 12.68ms | 167.65ms | 20.34ms | 16.77ms | 28.65ms | 35.21ms |
| cellx5000 | 49.31ms | 373.17ms | 61.39ms | 59.41ms | 81.75ms | 110.05ms |
| 10x5 - 2 sources - read 20.0% (simple) | 144.52ms | 1.36s | 327.62ms | 334.03ms | 383.88ms | 170.41ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 108.31ms | 1.02s | 162.27ms | 168.82ms | 281.36ms | 128.21ms |
| 1000x12 - 4 sources - dynamic (large) | 207.14ms | 1.17s | 3.30s | 2.93s | 612.00ms | 264.57ms |
| 1000x5 - 25 sources (wide dense) | 322.86ms | 2.41s | 2.65s | 2.67s | 1.07s | 300.74ms |
| 5x500 - 3 sources (deep) | 100.32ms | 703.26ms | 139.51ms | 134.39ms | 314.82ms | 137.83ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 162.57ms | 1.11s | 301.36ms | 310.25ms | 528.35ms | 181.24ms |

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
