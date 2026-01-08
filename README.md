# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.26s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.69s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.11s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.50s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.75s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.19s |

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
| avoidablePropagation | 125.56ms | 2.36s | 205.05ms | 253.26ms | 242.53ms | 171.42ms |
| broadPropagation | 237.11ms | 4.42s | 446.56ms | 455.69ms | 439.68ms | 399.85ms |
| deepPropagation | 82.70ms | 1.48s | 165.16ms | 168.39ms | 129.29ms | 156.96ms |
| diamond | 157.32ms | 2.36s | 287.05ms | 322.24ms | 303.48ms | 230.82ms |
| mux | 298.56ms | 1.86s | 369.04ms | 377.92ms | 382.62ms | 372.48ms |
| repeatedObservers | 26.91ms | 229.79ms | 31.92ms | 42.14ms | 87.67ms | 59.41ms |
| triangle | 64.66ms | 741.48ms | 100.92ms | 110.07ms | 95.47ms | 89.28ms |
| unstable | 45.68ms | 340.38ms | 54.98ms | 73.71ms | 101.95ms | 345.53ms |
| molBench | 487.09ms | 590.06ms | 494.51ms | 489.08ms | 487.13ms | 493.59ms |
| create_signals | 27.01ms | 70.95ms | 5.46ms | 31.10ms | 122.59ms | 64.27ms |
| comp_0to1 | 12.02ms | 24.27ms | 17.64ms | 24.69ms | 46.00ms | 57.11ms |
| comp_1to1 | 15.52ms | 17.08ms | 14.41ms | 7.89ms | 25.00ms | 60.19ms |
| comp_2to1 | 16.00ms | 18.84ms | 17.27ms | 16.27ms | 12.80ms | 36.30ms |
| comp_4to1 | 4.60ms | 28.04ms | 8.52ms | 1.82ms | 12.21ms | 15.54ms |
| comp_1000to1 | 3μs | 14μs | 4μs | 5μs | 15μs | 38μs |
| comp_1to2 | 13.89ms | 37.50ms | 25.10ms | 16.61ms | 43.30ms | 43.71ms |
| comp_1to4 | 14.24ms | 24.84ms | 21.91ms | 12.58ms | 28.19ms | 43.48ms |
| comp_1to8 | 5.68ms | 24.30ms | 8.89ms | 5.87ms | 28.54ms | 41.59ms |
| comp_1to1000 | 2.94ms | 15.23ms | 11.90ms | 4.81ms | 14.55ms | 37.33ms |
| update_1to1 | 5.69ms | 27.54ms | 8.92ms | 30.56ms | 13.96ms | 6.10ms |
| update_2to1 | 3.47ms | 12.85ms | 4.54ms | 15.19ms | 6.94ms | 3.05ms |
| update_4to1 | 947μs | 7.28ms | 2.27ms | 7.72ms | 3.47ms | 1.55ms |
| update_1000to1 | 19μs | 65μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.79ms | 13.72ms | 4.41ms | 15.47ms | 7.58ms | 3.07ms |
| update_1to4 | 1.26ms | 6.87ms | 2.28ms | 7.76ms | 3.64ms | 1.52ms |
| update_1to1000 | 40μs | 165μs | 2.66ms | 64μs | 152μs | 365μs |
| cellx1000 | 5.46ms | 70.92ms | 9.46ms | 9.51ms | 9.12ms | 9.11ms |
| cellx2500 | 15.71ms | 256.25ms | 26.15ms | 26.23ms | 25.91ms | 27.54ms |
| cellx5000 | 34.73ms | 574.25ms | 81.53ms | 71.48ms | 85.37ms | 95.24ms |
| 10x5 - 2 sources - read 20.0% (simple) | 191.70ms | 1.92s | 499.65ms | 533.33ms | 320.15ms | 249.83ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.33ms | 1.49s | 285.34ms | 298.50ms | 220.94ms | 219.84ms |
| 1000x12 - 4 sources - dynamic (large) | 275.10ms | 1.88s | 4.32s | 3.84s | 438.85ms | 368.39ms |
| 1000x5 - 25 sources (wide dense) | 526.90ms | 3.49s | 3.52s | 3.51s | 814.70ms | 503.98ms |
| 5x500 - 3 sources (deep) | 154.56ms | 1.11s | 231.89ms | 231.85ms | 227.18ms | 211.20ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 245.69ms | 1.69s | 470.59ms | 490.03ms | 328.45ms | 266.08ms |

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
