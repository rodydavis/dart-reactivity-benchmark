# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.29s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.61s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.07s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.24s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.37s |
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
| avoidablePropagation | 126.12ms | 2.37s | 202.70ms | 258.74ms | 249.16ms | 166.18ms |
| broadPropagation | 236.60ms | 4.47s | 448.85ms | 447.58ms | 440.66ms | 397.02ms |
| deepPropagation | 82.11ms | 1.52s | 164.11ms | 168.53ms | 129.56ms | 159.35ms |
| diamond | 157.63ms | 2.37s | 292.12ms | 315.66ms | 305.62ms | 221.60ms |
| mux | 295.98ms | 1.87s | 369.38ms | 383.04ms | 381.26ms | 374.69ms |
| repeatedObservers | 26.83ms | 226.44ms | 31.58ms | 41.80ms | 88.74ms | 61.24ms |
| triangle | 64.86ms | 753.98ms | 101.40ms | 108.49ms | 98.57ms | 86.00ms |
| unstable | 46.57ms | 346.48ms | 54.81ms | 74.44ms | 101.86ms | 343.15ms |
| molBench | 487.02ms | 590.69ms | 494.34ms | 485.00ms | 492.81ms | 494.40ms |
| create_signals | 30.14ms | 52.74ms | 5.50ms | 23.38ms | 73.67ms | 64.80ms |
| comp_0to1 | 6.75ms | 19.40ms | 17.95ms | 28.63ms | 41.26ms | 54.14ms |
| comp_1to1 | 22.36ms | 26.63ms | 13.97ms | 13.56ms | 26.14ms | 52.89ms |
| comp_2to1 | 17.07ms | 9.14ms | 17.05ms | 17.79ms | 13.63ms | 35.47ms |
| comp_4to1 | 3.32ms | 24.80ms | 11.23ms | 1.84ms | 4.48ms | 16.14ms |
| comp_1000to1 | 4μs | 24μs | 5μs | 4μs | 18μs | 37μs |
| comp_1to2 | 12.79ms | 38.05ms | 23.26ms | 17.85ms | 30.73ms | 43.44ms |
| comp_1to4 | 15.12ms | 26.66ms | 30.09ms | 16.30ms | 25.47ms | 43.82ms |
| comp_1to8 | 6.77ms | 24.72ms | 5.67ms | 13.97ms | 23.82ms | 41.45ms |
| comp_1to1000 | 3.65ms | 15.69ms | 5.46ms | 7.82ms | 14.22ms | 36.97ms |
| update_1to1 | 9.40ms | 27.08ms | 9.03ms | 32.18ms | 14.00ms | 6.19ms |
| update_2to1 | 4.71ms | 11.39ms | 4.52ms | 15.94ms | 7.16ms | 3.08ms |
| update_4to1 | 1.42ms | 6.89ms | 2.36ms | 8.15ms | 3.50ms | 1.56ms |
| update_1000to1 | 15μs | 68μs | 22μs | 81μs | 33μs | 15μs |
| update_1to2 | 4.71ms | 11.42ms | 4.46ms | 15.95ms | 6.94ms | 3.11ms |
| update_1to4 | 1.53ms | 6.95ms | 2.29ms | 8.13ms | 3.59ms | 1.58ms |
| update_1to1000 | 44μs | 162μs | 891μs | 67μs | 144μs | 368μs |
| cellx1000 | 5.94ms | 73.86ms | 10.08ms | 9.48ms | 9.58ms | 9.32ms |
| cellx2500 | 16.02ms | 257.13ms | 25.91ms | 28.82ms | 29.89ms | 29.11ms |
| cellx5000 | 34.33ms | 570.79ms | 81.57ms | 71.84ms | 83.52ms | 99.01ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.38ms | 1.95s | 490.82ms | 535.29ms | 325.48ms | 238.99ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.18ms | 1.46s | 281.12ms | 297.21ms | 219.37ms | 197.09ms |
| 1000x12 - 4 sources - dynamic (large) | 279.71ms | 1.85s | 4.17s | 3.54s | 442.76ms | 364.57ms |
| 1000x5 - 25 sources (wide dense) | 545.78ms | 3.40s | 3.30s | 3.51s | 821.36ms | 495.23ms |
| 5x500 - 3 sources (deep) | 159.30ms | 1.12s | 231.63ms | 240.66ms | 229.70ms | 207.48ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.23ms | 1.62s | 464.45ms | 491.33ms | 334.18ms | 260.23ms |

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
