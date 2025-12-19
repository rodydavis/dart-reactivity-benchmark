# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.28s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.57s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.14s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.37s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.47s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.11s |

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
| avoidablePropagation | 125.34ms | 2.40s | 200.68ms | 260.91ms | 244.44ms | 164.61ms |
| broadPropagation | 236.48ms | 4.42s | 453.98ms | 452.05ms | 449.16ms | 406.60ms |
| deepPropagation | 82.69ms | 1.49s | 162.45ms | 171.14ms | 129.25ms | 155.68ms |
| diamond | 158.63ms | 2.40s | 291.61ms | 325.90ms | 308.27ms | 213.65ms |
| mux | 296.87ms | 1.83s | 377.52ms | 380.31ms | 398.39ms | 371.82ms |
| repeatedObservers | 27.71ms | 227.78ms | 32.16ms | 41.81ms | 88.23ms | 58.67ms |
| triangle | 65.18ms | 750.12ms | 101.29ms | 112.36ms | 96.37ms | 95.56ms |
| unstable | 46.36ms | 343.51ms | 55.06ms | 76.33ms | 108.16ms | 346.52ms |
| molBench | 487.07ms | 590.53ms | 494.79ms | 483.83ms | 489.04ms | 492.75ms |
| create_signals | 26.77ms | 71.36ms | 5.45ms | 23.39ms | 130.58ms | 66.54ms |
| comp_0to1 | 11.87ms | 16.17ms | 18.03ms | 28.13ms | 39.69ms | 54.01ms |
| comp_1to1 | 18.87ms | 46.71ms | 13.12ms | 13.72ms | 24.39ms | 52.41ms |
| comp_2to1 | 16.90ms | 35.99ms | 10.24ms | 17.54ms | 17.52ms | 41.62ms |
| comp_4to1 | 2.07ms | 13.34ms | 7.83ms | 1.97ms | 17.26ms | 16.96ms |
| comp_1000to1 | 5μs | 17μs | 4μs | 4μs | 30μs | 37μs |
| comp_1to2 | 12.74ms | 35.56ms | 16.92ms | 21.47ms | 33.45ms | 43.12ms |
| comp_1to4 | 15.13ms | 18.07ms | 25.88ms | 24.03ms | 29.92ms | 43.41ms |
| comp_1to8 | 10.06ms | 20.48ms | 6.90ms | 11.64ms | 29.57ms | 41.83ms |
| comp_1to1000 | 3.14ms | 15.74ms | 4.52ms | 4.01ms | 14.34ms | 37.24ms |
| update_1to1 | 8.13ms | 24.38ms | 8.94ms | 30.50ms | 13.97ms | 6.12ms |
| update_2to1 | 4.85ms | 10.22ms | 4.50ms | 15.16ms | 6.92ms | 3.13ms |
| update_4to1 | 1.00ms | 7.24ms | 2.26ms | 7.62ms | 3.52ms | 1.53ms |
| update_1000to1 | 15μs | 68μs | 25μs | 77μs | 35μs | 15μs |
| update_1to2 | 4.83ms | 11.05ms | 4.43ms | 15.31ms | 7.54ms | 3.08ms |
| update_1to4 | 1.00ms | 6.89ms | 2.30ms | 7.66ms | 3.60ms | 1.50ms |
| update_1to1000 | 33μs | 165μs | 150μs | 67μs | 145μs | 362μs |
| cellx1000 | 8.39ms | 72.29ms | 10.88ms | 9.90ms | 9.73ms | 10.44ms |
| cellx2500 | 16.86ms | 245.41ms | 25.16ms | 25.47ms | 26.07ms | 24.39ms |
| cellx5000 | 36.52ms | 543.16ms | 62.81ms | 57.69ms | 58.19ms | 73.85ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.30ms | 1.93s | 489.65ms | 544.02ms | 324.10ms | 238.88ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 159.45ms | 1.48s | 279.86ms | 300.29ms | 218.20ms | 197.06ms |
| 1000x12 - 4 sources - dynamic (large) | 273.42ms | 1.87s | 4.12s | 3.77s | 439.92ms | 355.35ms |
| 1000x5 - 25 sources (wide dense) | 536.17ms | 3.48s | 3.39s | 3.51s | 818.03ms | 491.42ms |
| 5x500 - 3 sources (deep) | 157.05ms | 1.11s | 235.00ms | 236.05ms | 227.13ms | 206.19ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 246.33ms | 1.62s | 463.20ms | 485.61ms | 330.13ms | 257.81ms |

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
