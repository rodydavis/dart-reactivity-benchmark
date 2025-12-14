# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.34s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.59s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.12s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.51s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.73s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.28s |

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
| avoidablePropagation | 128.94ms | 2.33s | 204.63ms | 254.58ms | 261.35ms | 165.57ms |
| broadPropagation | 244.19ms | 4.43s | 455.97ms | 465.50ms | 440.63ms | 391.08ms |
| deepPropagation | 81.78ms | 1.50s | 161.36ms | 174.73ms | 132.73ms | 153.94ms |
| diamond | 166.35ms | 2.42s | 286.56ms | 337.46ms | 343.65ms | 216.33ms |
| mux | 315.77ms | 1.87s | 372.77ms | 380.31ms | 381.60ms | 370.28ms |
| repeatedObservers | 27.42ms | 235.79ms | 31.81ms | 42.04ms | 91.66ms | 61.67ms |
| triangle | 65.67ms | 762.34ms | 101.39ms | 136.74ms | 96.87ms | 89.21ms |
| unstable | 47.70ms | 350.21ms | 55.31ms | 73.74ms | 103.63ms | 344.15ms |
| molBench | 487.94ms | 592.68ms | 494.39ms | 483.43ms | 489.44ms | 493.47ms |
| create_signals | 32.20ms | 74.69ms | 5.57ms | 23.12ms | 74.68ms | 57.67ms |
| comp_0to1 | 6.70ms | 26.35ms | 18.11ms | 31.91ms | 41.59ms | 51.54ms |
| comp_1to1 | 23.05ms | 17.22ms | 13.15ms | 13.46ms | 38.63ms | 53.17ms |
| comp_2to1 | 17.20ms | 19.47ms | 17.64ms | 18.04ms | 13.37ms | 35.35ms |
| comp_4to1 | 2.60ms | 31.28ms | 8.65ms | 1.93ms | 4.43ms | 16.40ms |
| comp_1000to1 | 3μs | 15μs | 7μs | 5μs | 30μs | 38μs |
| comp_1to2 | 12.10ms | 39.60ms | 14.23ms | 22.27ms | 27.11ms | 43.87ms |
| comp_1to4 | 15.04ms | 24.66ms | 20.68ms | 16.85ms | 19.34ms | 43.76ms |
| comp_1to8 | 6.77ms | 26.09ms | 13.30ms | 14.33ms | 26.98ms | 41.69ms |
| comp_1to1000 | 3.75ms | 15.74ms | 6.62ms | 5.73ms | 19.65ms | 37.28ms |
| update_1to1 | 6.65ms | 26.42ms | 8.98ms | 30.54ms | 14.10ms | 6.10ms |
| update_2to1 | 4.79ms | 13.24ms | 4.48ms | 15.19ms | 7.22ms | 3.06ms |
| update_4to1 | 1.59ms | 7.45ms | 2.25ms | 7.63ms | 3.49ms | 1.56ms |
| update_1000to1 | 22μs | 69μs | 27μs | 76μs | 34μs | 15μs |
| update_1to2 | 6.73ms | 13.57ms | 4.46ms | 15.26ms | 6.98ms | 3.10ms |
| update_1to4 | 1.13ms | 6.73ms | 2.28ms | 7.64ms | 3.57ms | 1.53ms |
| update_1to1000 | 45μs | 160μs | 448μs | 66μs | 145μs | 371μs |
| cellx1000 | 6.52ms | 78.23ms | 9.62ms | 9.58ms | 9.51ms | 10.12ms |
| cellx2500 | 20.26ms | 258.58ms | 29.57ms | 26.34ms | 28.68ms | 35.93ms |
| cellx5000 | 56.27ms | 581.18ms | 84.31ms | 71.98ms | 68.15ms | 96.64ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.68ms | 1.91s | 490.93ms | 536.83ms | 329.53ms | 238.21ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.35ms | 1.48s | 280.96ms | 297.45ms | 220.87ms | 197.67ms |
| 1000x12 - 4 sources - dynamic (large) | 279.54ms | 1.89s | 4.34s | 3.79s | 449.05ms | 370.96ms |
| 1000x5 - 25 sources (wide dense) | 530.80ms | 3.47s | 3.51s | 3.48s | 812.16ms | 495.57ms |
| 5x500 - 3 sources (deep) | 155.73ms | 1.10s | 228.28ms | 237.70ms | 226.64ms | 208.66ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 245.68ms | 1.68s | 455.43ms | 483.85ms | 334.10ms | 257.50ms |

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
