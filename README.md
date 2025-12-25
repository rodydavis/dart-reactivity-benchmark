# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.25s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.53s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.13s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.21s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.66s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.12s |

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
| avoidablePropagation | 125.99ms | 2.35s | 201.20ms | 260.82ms | 265.64ms | 177.69ms |
| broadPropagation | 236.17ms | 4.39s | 454.24ms | 457.73ms | 443.59ms | 396.95ms |
| deepPropagation | 81.96ms | 1.52s | 162.59ms | 171.47ms | 132.51ms | 155.74ms |
| diamond | 161.97ms | 2.40s | 285.75ms | 322.23ms | 313.49ms | 221.76ms |
| mux | 296.03ms | 1.86s | 375.02ms | 378.75ms | 388.99ms | 377.10ms |
| repeatedObservers | 27.63ms | 228.65ms | 32.21ms | 42.18ms | 91.72ms | 57.80ms |
| triangle | 65.36ms | 743.79ms | 100.99ms | 126.30ms | 99.74ms | 84.94ms |
| unstable | 46.56ms | 342.57ms | 57.51ms | 76.25ms | 105.88ms | 342.92ms |
| molBench | 483.86ms | 590.35ms | 494.20ms | 489.50ms | 491.15ms | 488.29ms |
| create_signals | 31.98ms | 81.27ms | 5.70ms | 23.79ms | 126.69ms | 56.74ms |
| comp_0to1 | 11.60ms | 28.05ms | 17.43ms | 29.24ms | 37.96ms | 50.51ms |
| comp_1to1 | 14.82ms | 30.91ms | 12.94ms | 13.63ms | 24.21ms | 51.72ms |
| comp_2to1 | 12.45ms | 30.14ms | 18.54ms | 10.18ms | 17.76ms | 34.41ms |
| comp_4to1 | 1.71ms | 17.45ms | 8.65ms | 2.03ms | 17.08ms | 15.46ms |
| comp_1000to1 | 4μs | 20μs | 7μs | 4μs | 30μs | 38μs |
| comp_1to2 | 11.53ms | 37.56ms | 21.98ms | 20.10ms | 38.37ms | 42.77ms |
| comp_1to4 | 12.35ms | 24.78ms | 21.89ms | 27.24ms | 27.15ms | 43.42ms |
| comp_1to8 | 6.61ms | 23.76ms | 6.56ms | 9.22ms | 32.32ms | 40.85ms |
| comp_1to1000 | 6.71ms | 15.92ms | 5.88ms | 5.92ms | 14.61ms | 37.20ms |
| update_1to1 | 6.04ms | 21.76ms | 8.96ms | 30.64ms | 14.36ms | 6.10ms |
| update_2to1 | 4.80ms | 10.86ms | 4.53ms | 15.11ms | 7.08ms | 3.07ms |
| update_4to1 | 1.53ms | 5.37ms | 2.25ms | 7.63ms | 3.58ms | 1.57ms |
| update_1000to1 | 16μs | 52μs | 26μs | 76μs | 36μs | 26μs |
| update_1to2 | 3.38ms | 10.59ms | 4.42ms | 15.27ms | 7.71ms | 3.09ms |
| update_1to4 | 1.63ms | 5.30ms | 2.29ms | 7.68ms | 3.69ms | 1.55ms |
| update_1to1000 | 42μs | 156μs | 923μs | 69μs | 143μs | 359μs |
| cellx1000 | 5.48ms | 70.12ms | 9.45ms | 10.04ms | 11.54ms | 8.57ms |
| cellx2500 | 15.06ms | 241.72ms | 24.70ms | 24.89ms | 25.80ms | 23.83ms |
| cellx5000 | 33.68ms | 547.58ms | 65.01ms | 60.90ms | 56.33ms | 75.33ms |
| 10x5 - 2 sources - read 20.0% (simple) | 189.91ms | 1.97s | 494.56ms | 537.69ms | 320.04ms | 248.06ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.82ms | 1.49s | 287.76ms | 297.66ms | 217.65ms | 197.65ms |
| 1000x12 - 4 sources - dynamic (large) | 270.10ms | 1.84s | 4.39s | 3.56s | 438.47ms | 356.05ms |
| 1000x5 - 25 sources (wide dense) | 525.91ms | 3.46s | 3.38s | 3.45s | 801.09ms | 467.19ms |
| 5x500 - 3 sources (deep) | 154.67ms | 1.11s | 225.03ms | 236.53ms | 224.35ms | 201.47ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.75ms | 1.63s | 471.87ms | 486.50ms | 326.30ms | 256.35ms |

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
