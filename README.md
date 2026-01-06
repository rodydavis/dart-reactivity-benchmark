# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.29s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.63s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.02s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.27s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.67s |
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
| avoidablePropagation | 126.13ms | 2.40s | 211.13ms | 256.36ms | 247.01ms | 173.70ms |
| broadPropagation | 237.26ms | 4.43s | 457.77ms | 463.86ms | 440.41ms | 404.61ms |
| deepPropagation | 83.61ms | 1.48s | 164.93ms | 173.54ms | 127.73ms | 157.59ms |
| diamond | 158.38ms | 2.40s | 295.33ms | 317.73ms | 299.55ms | 212.21ms |
| mux | 294.48ms | 1.87s | 375.55ms | 380.05ms | 378.98ms | 370.50ms |
| repeatedObservers | 27.33ms | 232.69ms | 31.85ms | 41.55ms | 87.92ms | 62.68ms |
| triangle | 66.21ms | 749.91ms | 101.93ms | 112.12ms | 96.91ms | 87.14ms |
| unstable | 45.98ms | 345.29ms | 55.59ms | 76.76ms | 101.19ms | 348.98ms |
| molBench | 486.93ms | 591.98ms | 495.27ms | 487.12ms | 491.96ms | 493.16ms |
| create_signals | 32.98ms | 69.45ms | 19.10ms | 26.73ms | 67.94ms | 57.19ms |
| comp_0to1 | 14.05ms | 27.80ms | 15.21ms | 27.87ms | 17.90ms | 52.87ms |
| comp_1to1 | 15.65ms | 36.72ms | 6.97ms | 7.83ms | 27.82ms | 54.38ms |
| comp_2to1 | 25.34ms | 30.66ms | 10.49ms | 11.53ms | 27.38ms | 35.53ms |
| comp_4to1 | 2.55ms | 15.80ms | 13.54ms | 3.18ms | 11.06ms | 16.23ms |
| comp_1000to1 | 3μs | 15μs | 10μs | 6μs | 14μs | 39μs |
| comp_1to2 | 8.00ms | 33.84ms | 20.45ms | 20.08ms | 36.35ms | 45.34ms |
| comp_1to4 | 17.68ms | 22.48ms | 28.45ms | 16.57ms | 28.66ms | 45.35ms |
| comp_1to8 | 4.66ms | 23.45ms | 8.34ms | 10.21ms | 28.54ms | 43.92ms |
| comp_1to1000 | 3.14ms | 14.84ms | 6.40ms | 4.36ms | 14.93ms | 39.26ms |
| update_1to1 | 4.34ms | 24.88ms | 8.88ms | 30.60ms | 14.18ms | 6.10ms |
| update_2to1 | 4.70ms | 13.61ms | 4.48ms | 16.15ms | 6.96ms | 3.07ms |
| update_4to1 | 990μs | 6.96ms | 2.23ms | 7.63ms | 3.60ms | 1.58ms |
| update_1000to1 | 9μs | 69μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.77ms | 13.20ms | 4.41ms | 15.23ms | 7.55ms | 3.09ms |
| update_1to4 | 1.08ms | 6.90ms | 2.26ms | 7.84ms | 3.58ms | 1.58ms |
| update_1to1000 | 41μs | 160μs | 895μs | 90μs | 153μs | 388μs |
| cellx1000 | 5.60ms | 70.07ms | 9.31ms | 9.58ms | 9.21ms | 9.16ms |
| cellx2500 | 17.65ms | 257.78ms | 25.03ms | 25.50ms | 27.09ms | 26.54ms |
| cellx5000 | 43.58ms | 564.73ms | 63.62ms | 83.29ms | 65.93ms | 83.13ms |
| 10x5 - 2 sources - read 20.0% (simple) | 181.88ms | 1.90s | 492.26ms | 531.77ms | 317.15ms | 253.47ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.09ms | 1.43s | 284.62ms | 293.81ms | 217.23ms | 203.57ms |
| 1000x12 - 4 sources - dynamic (large) | 284.04ms | 1.81s | 4.29s | 3.56s | 436.78ms | 364.24ms |
| 1000x5 - 25 sources (wide dense) | 537.89ms | 3.40s | 3.46s | 3.52s | 812.71ms | 498.93ms |
| 5x500 - 3 sources (deep) | 153.73ms | 1.13s | 234.53ms | 238.56ms | 233.60ms | 213.55ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.55ms | 1.70s | 465.31ms | 487.10ms | 328.53ms | 262.71ms |

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
