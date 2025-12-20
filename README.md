# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.35s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.69s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.25s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.53s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.81s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.66s |

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
| avoidablePropagation | 125.58ms | 2.38s | 207.17ms | 257.32ms | 249.61ms | 171.05ms |
| broadPropagation | 236.86ms | 4.42s | 461.66ms | 462.43ms | 448.50ms | 407.48ms |
| deepPropagation | 81.83ms | 1.52s | 163.78ms | 174.37ms | 132.00ms | 153.69ms |
| diamond | 157.73ms | 2.40s | 289.84ms | 317.01ms | 317.09ms | 211.26ms |
| mux | 293.70ms | 1.89s | 377.61ms | 379.89ms | 399.00ms | 359.81ms |
| repeatedObservers | 27.84ms | 236.88ms | 35.32ms | 41.91ms | 89.13ms | 58.43ms |
| triangle | 76.27ms | 753.50ms | 101.88ms | 112.19ms | 97.22ms | 84.82ms |
| unstable | 46.06ms | 346.48ms | 55.17ms | 77.43ms | 103.41ms | 344.88ms |
| molBench | 487.44ms | 592.88ms | 496.17ms | 482.54ms | 492.50ms | 493.42ms |
| create_signals | 30.13ms | 69.86ms | 9.89ms | 28.34ms | 74.77ms | 59.73ms |
| comp_0to1 | 9.31ms | 25.63ms | 26.51ms | 24.50ms | 41.07ms | 52.09ms |
| comp_1to1 | 23.01ms | 32.98ms | 6.94ms | 7.98ms | 40.72ms | 60.70ms |
| comp_2to1 | 18.45ms | 37.29ms | 10.56ms | 9.69ms | 13.27ms | 44.59ms |
| comp_4to1 | 3.90ms | 29.30ms | 14.13ms | 6.93ms | 4.38ms | 18.73ms |
| comp_1000to1 | 5μs | 15μs | 6μs | 5μs | 19μs | 38μs |
| comp_1to2 | 9.91ms | 35.84ms | 29.60ms | 17.32ms | 34.39ms | 43.82ms |
| comp_1to4 | 16.45ms | 18.19ms | 22.83ms | 18.82ms | 21.05ms | 43.99ms |
| comp_1to8 | 6.80ms | 21.95ms | 9.30ms | 12.20ms | 24.13ms | 42.06ms |
| comp_1to1000 | 6.00ms | 15.73ms | 6.63ms | 7.25ms | 14.35ms | 37.60ms |
| update_1to1 | 10.04ms | 27.32ms | 9.05ms | 30.99ms | 13.99ms | 6.10ms |
| update_2to1 | 4.65ms | 13.02ms | 4.65ms | 15.19ms | 7.16ms | 3.10ms |
| update_4to1 | 1.27ms | 7.44ms | 2.31ms | 7.62ms | 3.50ms | 1.59ms |
| update_1000to1 | 15μs | 67μs | 32μs | 1.28ms | 35μs | 15μs |
| update_1to2 | 4.51ms | 13.47ms | 4.46ms | 16.06ms | 6.98ms | 3.12ms |
| update_1to4 | 1.60ms | 6.98ms | 2.32ms | 7.77ms | 3.58ms | 1.57ms |
| update_1to1000 | 35μs | 171μs | 2.54ms | 100μs | 144μs | 364μs |
| cellx1000 | 6.14ms | 92.29ms | 10.74ms | 10.24ms | 12.63ms | 11.61ms |
| cellx2500 | 24.21ms | 293.42ms | 36.05ms | 32.35ms | 43.52ms | 45.61ms |
| cellx5000 | 61.97ms | 641.56ms | 98.77ms | 86.76ms | 147.09ms | 146.96ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.33ms | 1.96s | 496.43ms | 538.81ms | 330.24ms | 246.19ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 155.90ms | 1.49s | 279.91ms | 299.21ms | 219.91ms | 198.66ms |
| 1000x12 - 4 sources - dynamic (large) | 294.76ms | 1.91s | 4.39s | 3.75s | 457.40ms | 371.58ms |
| 1000x5 - 25 sources (wide dense) | 541.71ms | 3.52s | 3.45s | 3.56s | 845.75ms | 494.31ms |
| 5x500 - 3 sources (deep) | 155.22ms | 1.13s | 230.60ms | 240.98ms | 229.27ms | 208.47ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.10ms | 1.72s | 470.85ms | 494.76ms | 336.80ms | 260.27ms |

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
