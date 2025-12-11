# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.98s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.18s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.84s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.41s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.47s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.89s |

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
| avoidablePropagation | 133.97ms | 2.27s | 183.53ms | 232.28ms | 241.82ms | 157.40ms |
| broadPropagation | 221.52ms | 4.13s | 395.38ms | 387.99ms | 444.23ms | 357.54ms |
| deepPropagation | 86.45ms | 1.48s | 183.33ms | 178.51ms | 132.91ms | 164.81ms |
| diamond | 149.18ms | 2.27s | 257.15ms | 309.12ms | 309.79ms | 212.47ms |
| mux | 290.12ms | 1.83s | 341.80ms | 340.96ms | 379.72ms | 321.73ms |
| repeatedObservers | 22.80ms | 226.91ms | 28.73ms | 37.10ms | 91.04ms | 51.25ms |
| triangle | 61.97ms | 761.72ms | 95.57ms | 101.66ms | 103.46ms | 86.27ms |
| unstable | 42.33ms | 330.72ms | 50.85ms | 62.29ms | 112.38ms | 334.54ms |
| molBench | 363.41ms | 485.36ms | 390.93ms | 369.44ms | 371.64ms | 390.46ms |
| create_signals | 30.25ms | 76.04ms | 9.92ms | 30.92ms | 65.72ms | 62.84ms |
| comp_0to1 | 17.68ms | 25.44ms | 24.81ms | 28.63ms | 17.98ms | 52.08ms |
| comp_1to1 | 24.95ms | 49.52ms | 16.28ms | 9.70ms | 39.81ms | 54.89ms |
| comp_2to1 | 19.31ms | 12.64ms | 14.83ms | 13.36ms | 13.17ms | 36.74ms |
| comp_4to1 | 3.31ms | 36.09ms | 15.27ms | 8.08ms | 7.63ms | 16.68ms |
| comp_1000to1 | 7μs | 26μs | 18μs | 7μs | 15μs | 41μs |
| comp_1to2 | 9.97ms | 35.90ms | 22.97ms | 25.51ms | 24.77ms | 45.33ms |
| comp_1to4 | 25.00ms | 34.13ms | 31.32ms | 19.05ms | 16.20ms | 46.07ms |
| comp_1to8 | 6.39ms | 25.52ms | 7.61ms | 13.85ms | 31.11ms | 44.18ms |
| comp_1to1000 | 5.37ms | 17.13ms | 7.49ms | 7.56ms | 19.09ms | 39.55ms |
| update_1to1 | 3.33ms | 20.21ms | 7.66ms | 26.88ms | 13.90ms | 4.75ms |
| update_2to1 | 1.52ms | 10.41ms | 3.70ms | 13.35ms | 6.94ms | 2.51ms |
| update_4to1 | 803μs | 4.92ms | 1.96ms | 6.80ms | 3.51ms | 1.23ms |
| update_1000to1 | 7μs | 50μs | 20μs | 64μs | 34μs | 12μs |
| update_1to2 | 1.53ms | 10.45ms | 3.98ms | 13.48ms | 7.02ms | 2.34ms |
| update_1to4 | 778μs | 5.00ms | 2.92ms | 6.83ms | 3.41ms | 1.17ms |
| update_1to1000 | 49μs | 172μs | 669μs | 88μs | 147μs | 400μs |
| cellx1000 | 8.96ms | 114.74ms | 12.16ms | 12.35ms | 17.93ms | 15.55ms |
| cellx2500 | 31.74ms | 300.15ms | 36.94ms | 40.45ms | 63.81ms | 46.90ms |
| cellx5000 | 70.67ms | 656.88ms | 104.30ms | 103.50ms | 140.24ms | 135.21ms |
| 10x5 - 2 sources - read 20.0% (simple) | 174.61ms | 2.11s | 418.07ms | 453.10ms | 319.91ms | 226.27ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 152.94ms | 1.52s | 243.68ms | 254.02ms | 236.81ms | 172.04ms |
| 1000x12 - 4 sources - dynamic (large) | 246.90ms | 1.70s | 3.21s | 3.07s | 385.95ms | 293.63ms |
| 1000x5 - 25 sources (wide dense) | 391.22ms | 3.47s | 2.67s | 2.66s | 646.30ms | 382.58ms |
| 5x500 - 3 sources (deep) | 172.37ms | 1.21s | 219.30ms | 216.69ms | 272.41ms | 205.95ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 204.88ms | 1.65s | 398.75ms | 408.22ms | 296.60ms | 218.77ms |

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
