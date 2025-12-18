# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.36s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.67s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.28s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.47s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.55s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.59s |

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
| avoidablePropagation | 126.30ms | 2.37s | 197.46ms | 252.58ms | 237.49ms | 166.91ms |
| broadPropagation | 235.95ms | 4.46s | 459.11ms | 456.10ms | 444.13ms | 398.58ms |
| deepPropagation | 81.40ms | 1.53s | 166.74ms | 172.30ms | 129.10ms | 159.21ms |
| diamond | 157.07ms | 2.43s | 286.86ms | 313.13ms | 302.52ms | 211.54ms |
| mux | 310.13ms | 1.86s | 370.51ms | 382.37ms | 381.82ms | 360.53ms |
| repeatedObservers | 27.60ms | 226.25ms | 34.77ms | 42.00ms | 96.07ms | 58.60ms |
| triangle | 65.14ms | 773.73ms | 106.83ms | 114.97ms | 97.69ms | 83.48ms |
| unstable | 45.90ms | 347.18ms | 54.90ms | 75.29ms | 101.82ms | 343.64ms |
| molBench | 486.90ms | 592.01ms | 495.58ms | 485.38ms | 492.73ms | 493.22ms |
| create_signals | 26.97ms | 86.97ms | 5.46ms | 24.74ms | 118.15ms | 63.75ms |
| comp_0to1 | 18.20ms | 41.17ms | 18.30ms | 34.04ms | 37.26ms | 54.26ms |
| comp_1to1 | 17.46ms | 31.86ms | 21.06ms | 14.05ms | 25.88ms | 59.71ms |
| comp_2to1 | 15.54ms | 28.78ms | 19.83ms | 11.86ms | 19.56ms | 38.60ms |
| comp_4to1 | 4.96ms | 20.44ms | 8.59ms | 2.24ms | 12.54ms | 18.60ms |
| comp_1000to1 | 3μs | 33μs | 5μs | 5μs | 15μs | 66μs |
| comp_1to2 | 12.11ms | 36.94ms | 16.02ms | 33.39ms | 44.15ms | 47.80ms |
| comp_1to4 | 17.50ms | 25.06ms | 27.80ms | 19.93ms | 29.70ms | 47.73ms |
| comp_1to8 | 5.58ms | 27.32ms | 7.11ms | 11.90ms | 36.87ms | 44.84ms |
| comp_1to1000 | 3.21ms | 15.93ms | 4.89ms | 4.73ms | 14.45ms | 39.85ms |
| update_1to1 | 5.32ms | 27.49ms | 9.00ms | 30.74ms | 14.09ms | 6.14ms |
| update_2to1 | 4.92ms | 12.83ms | 4.49ms | 15.20ms | 6.93ms | 3.05ms |
| update_4to1 | 1.34ms | 7.10ms | 2.21ms | 7.62ms | 3.54ms | 1.58ms |
| update_1000to1 | 9μs | 68μs | 22μs | 128μs | 34μs | 15μs |
| update_1to2 | 4.79ms | 13.79ms | 4.51ms | 15.31ms | 7.60ms | 3.08ms |
| update_1to4 | 1.27ms | 6.93ms | 2.26ms | 7.72ms | 3.63ms | 1.52ms |
| update_1to1000 | 44μs | 161μs | 159μs | 66μs | 143μs | 408μs |
| cellx1000 | 8.59ms | 89.31ms | 9.96ms | 10.53ms | 10.66ms | 12.04ms |
| cellx2500 | 24.78ms | 314.14ms | 37.19ms | 41.65ms | 41.47ms | 37.13ms |
| cellx5000 | 70.20ms | 629.07ms | 119.42ms | 133.44ms | 167.94ms | 128.86ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.22ms | 1.99s | 488.32ms | 535.87ms | 320.01ms | 240.58ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.62ms | 1.50s | 280.25ms | 300.62ms | 219.02ms | 199.63ms |
| 1000x12 - 4 sources - dynamic (large) | 288.13ms | 1.87s | 4.18s | 3.58s | 458.86ms | 378.06ms |
| 1000x5 - 25 sources (wide dense) | 543.76ms | 3.43s | 3.41s | 3.60s | 837.22ms | 495.22ms |
| 5x500 - 3 sources (deep) | 157.82ms | 1.13s | 231.31ms | 242.58ms | 230.35ms | 210.31ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.38ms | 1.68s | 466.34ms | 494.68ms | 335.14ms | 262.84ms |

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
