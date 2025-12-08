# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.61s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.01s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.45s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.92s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.43s |

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
| avoidablePropagation | 125.90ms | 2.39s | 203.82ms | 256.08ms | 239.35ms | 175.69ms |
| broadPropagation | 235.72ms | 4.39s | 449.03ms | 458.27ms | 441.40ms | 416.60ms |
| deepPropagation | 84.78ms | 1.51s | 167.62ms | 177.39ms | 130.30ms | 158.66ms |
| diamond | 155.47ms | 2.38s | 290.88ms | 319.83ms | 311.63ms | 214.16ms |
| mux | 300.05ms | 1.85s | 379.97ms | 378.46ms | 375.62ms | 364.50ms |
| repeatedObservers | 27.16ms | 228.80ms | 32.16ms | 42.35ms | 87.85ms | 59.05ms |
| triangle | 67.46ms | 764.61ms | 101.53ms | 112.27ms | 97.47ms | 84.51ms |
| unstable | 45.87ms | 342.60ms | 55.12ms | 74.45ms | 103.20ms | 342.78ms |
| molBench | 488.52ms | 594.19ms | 494.04ms | 481.84ms | 485.34ms | 492.56ms |
| create_signals | 26.69ms | 63.92ms | 4.98ms | 26.83ms | 68.42ms | 63.05ms |
| comp_0to1 | 11.06ms | 15.77ms | 17.98ms | 20.38ms | 19.35ms | 51.22ms |
| comp_1to1 | 15.20ms | 56.88ms | 14.62ms | 8.01ms | 29.95ms | 54.98ms |
| comp_2to1 | 12.88ms | 22.95ms | 16.94ms | 17.93ms | 15.30ms | 41.93ms |
| comp_4to1 | 2.90ms | 27.80ms | 16.57ms | 1.80ms | 4.83ms | 17.53ms |
| comp_1000to1 | 3μs | 27μs | 4μs | 5μs | 20μs | 42μs |
| comp_1to2 | 11.60ms | 38.70ms | 18.42ms | 16.66ms | 33.79ms | 44.18ms |
| comp_1to4 | 16.04ms | 18.59ms | 59.60ms | 12.19ms | 23.59ms | 45.96ms |
| comp_1to8 | 7.26ms | 21.47ms | 8.18ms | 5.68ms | 24.61ms | 42.19ms |
| comp_1to1000 | 4.06ms | 15.66ms | 5.44ms | 5.13ms | 15.74ms | 36.91ms |
| update_1to1 | 4.76ms | 27.22ms | 8.92ms | 33.03ms | 13.94ms | 6.09ms |
| update_2to1 | 4.04ms | 13.65ms | 4.52ms | 15.19ms | 7.09ms | 3.05ms |
| update_4to1 | 979μs | 7.07ms | 2.25ms | 7.63ms | 3.51ms | 1.55ms |
| update_1000to1 | 23μs | 68μs | 22μs | 75μs | 35μs | 15μs |
| update_1to2 | 4.78ms | 13.88ms | 4.42ms | 16.21ms | 6.96ms | 3.06ms |
| update_1to4 | 2.10ms | 6.91ms | 2.25ms | 7.68ms | 3.61ms | 1.52ms |
| update_1to1000 | 55μs | 172μs | 178μs | 83μs | 160μs | 370μs |
| cellx1000 | 6.05ms | 75.19ms | 9.60ms | 9.30ms | 10.88ms | 9.01ms |
| cellx2500 | 15.50ms | 261.40ms | 26.80ms | 26.06ms | 26.89ms | 29.69ms |
| cellx5000 | 34.69ms | 582.18ms | 74.81ms | 64.43ms | 75.85ms | 95.73ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.06ms | 2.03s | 495.17ms | 542.58ms | 321.41ms | 235.81ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.91ms | 1.52s | 284.02ms | 298.05ms | 217.59ms | 197.58ms |
| 1000x12 - 4 sources - dynamic (large) | 284.50ms | 1.88s | 4.44s | 3.77s | 453.16ms | 361.56ms |
| 1000x5 - 25 sources (wide dense) | 529.68ms | 3.48s | 3.53s | 3.51s | 808.38ms | 493.68ms |
| 5x500 - 3 sources (deep) | 156.04ms | 1.13s | 229.70ms | 238.69ms | 226.13ms | 205.57ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 244.90ms | 1.67s | 470.18ms | 491.84ms | 327.60ms | 258.18ms |

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
