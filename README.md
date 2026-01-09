# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.26s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.67s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.07s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.18s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.33s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.95s |

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
| avoidablePropagation | 125.39ms | 2.34s | 200.87ms | 254.89ms | 236.33ms | 170.11ms |
| broadPropagation | 236.09ms | 4.39s | 450.91ms | 457.92ms | 441.39ms | 410.50ms |
| deepPropagation | 82.44ms | 1.50s | 163.21ms | 170.16ms | 131.12ms | 161.15ms |
| diamond | 155.97ms | 2.39s | 286.11ms | 316.22ms | 300.95ms | 232.22ms |
| mux | 294.57ms | 1.81s | 378.02ms | 381.34ms | 382.83ms | 360.33ms |
| repeatedObservers | 26.66ms | 227.22ms | 32.24ms | 40.99ms | 87.32ms | 58.68ms |
| triangle | 65.48ms | 736.63ms | 104.67ms | 109.78ms | 96.29ms | 89.55ms |
| unstable | 49.27ms | 341.82ms | 54.91ms | 73.45ms | 101.04ms | 343.90ms |
| molBench | 487.29ms | 590.20ms | 495.33ms | 483.19ms | 491.89ms | 493.03ms |
| create_signals | 25.79ms | 72.07ms | 5.67ms | 28.61ms | 122.76ms | 59.56ms |
| comp_0to1 | 16.64ms | 25.02ms | 18.31ms | 27.97ms | 36.82ms | 53.78ms |
| comp_1to1 | 17.88ms | 16.98ms | 13.94ms | 7.71ms | 24.47ms | 56.21ms |
| comp_2to1 | 21.26ms | 20.07ms | 19.93ms | 12.28ms | 17.68ms | 36.39ms |
| comp_4to1 | 1.62ms | 28.44ms | 8.82ms | 5.64ms | 15.85ms | 16.01ms |
| comp_1000to1 | 4μs | 16μs | 6μs | 5μs | 18μs | 40μs |
| comp_1to2 | 9.64ms | 45.60ms | 24.91ms | 18.09ms | 29.19ms | 45.77ms |
| comp_1to4 | 14.39ms | 25.47ms | 21.04ms | 21.69ms | 24.50ms | 45.53ms |
| comp_1to8 | 6.24ms | 24.66ms | 7.78ms | 15.00ms | 21.92ms | 43.58ms |
| comp_1to1000 | 3.15ms | 15.48ms | 8.02ms | 9.78ms | 14.14ms | 39.18ms |
| update_1to1 | 4.69ms | 26.37ms | 8.95ms | 30.79ms | 13.99ms | 6.10ms |
| update_2to1 | 4.99ms | 13.49ms | 4.50ms | 15.17ms | 7.12ms | 3.07ms |
| update_4to1 | 915μs | 7.08ms | 2.27ms | 7.61ms | 3.50ms | 1.59ms |
| update_1000to1 | 9μs | 69μs | 22μs | 1.15ms | 34μs | 15μs |
| update_1to2 | 4.78ms | 13.90ms | 4.42ms | 15.96ms | 6.97ms | 3.10ms |
| update_1to4 | 2.07ms | 6.90ms | 2.28ms | 7.68ms | 3.59ms | 1.58ms |
| update_1to1000 | 38μs | 164μs | 2.71ms | 70μs | 146μs | 392μs |
| cellx1000 | 8.72ms | 84.49ms | 9.38ms | 9.57ms | 9.44ms | 10.16ms |
| cellx2500 | 15.15ms | 271.99ms | 25.83ms | 25.61ms | 27.02ms | 33.53ms |
| cellx5000 | 34.37ms | 550.54ms | 74.58ms | 59.87ms | 59.77ms | 100.01ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.30ms | 1.93s | 493.29ms | 540.00ms | 323.81ms | 253.18ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.18ms | 1.45s | 286.03ms | 298.25ms | 217.59ms | 202.37ms |
| 1000x12 - 4 sources - dynamic (large) | 275.06ms | 1.84s | 4.21s | 3.59s | 445.34ms | 359.46ms |
| 1000x5 - 25 sources (wide dense) | 537.34ms | 3.40s | 3.20s | 3.41s | 819.10ms | 496.29ms |
| 5x500 - 3 sources (deep) | 154.15ms | 1.09s | 235.59ms | 244.33ms | 227.26ms | 218.19ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.46ms | 1.67s | 467.11ms | 490.20ms | 328.77ms | 262.82ms |

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
