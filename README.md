# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.99s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.13s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.89s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.41s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.45s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.96s |

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
| avoidablePropagation | 132.01ms | 2.25s | 182.35ms | 229.81ms | 239.13ms | 157.03ms |
| broadPropagation | 223.13ms | 4.13s | 390.82ms | 386.98ms | 435.46ms | 346.60ms |
| deepPropagation | 85.89ms | 1.46s | 184.84ms | 179.22ms | 131.84ms | 163.64ms |
| diamond | 148.40ms | 2.27s | 255.43ms | 302.92ms | 306.37ms | 208.08ms |
| mux | 297.57ms | 1.93s | 337.89ms | 335.52ms | 376.91ms | 318.35ms |
| repeatedObservers | 22.90ms | 228.45ms | 28.64ms | 36.50ms | 94.73ms | 50.87ms |
| triangle | 61.57ms | 751.63ms | 96.68ms | 101.66ms | 102.63ms | 83.91ms |
| unstable | 41.72ms | 320.16ms | 51.25ms | 61.96ms | 114.20ms | 326.90ms |
| molBench | 360.76ms | 483.65ms | 389.74ms | 369.27ms | 374.89ms | 387.65ms |
| create_signals | 36.50ms | 56.51ms | 6.85ms | 27.50ms | 101.26ms | 71.86ms |
| comp_0to1 | 17.20ms | 20.38ms | 25.37ms | 21.89ms | 26.93ms | 59.82ms |
| comp_1to1 | 18.78ms | 43.36ms | 19.40ms | 10.41ms | 25.95ms | 53.94ms |
| comp_2to1 | 16.97ms | 32.17ms | 20.48ms | 15.16ms | 13.43ms | 39.73ms |
| comp_4to1 | 2.72ms | 22.94ms | 12.51ms | 2.66ms | 11.59ms | 16.78ms |
| comp_1000to1 | 4μs | 18μs | 6μs | 7μs | 15μs | 38μs |
| comp_1to2 | 12.87ms | 32.67ms | 18.61ms | 25.42ms | 31.17ms | 45.41ms |
| comp_1to4 | 25.12ms | 40.05ms | 40.81ms | 19.01ms | 32.10ms | 44.42ms |
| comp_1to8 | 8.24ms | 24.31ms | 9.01ms | 14.78ms | 32.26ms | 43.20ms |
| comp_1to1000 | 5.51ms | 17.70ms | 6.65ms | 9.68ms | 15.91ms | 38.42ms |
| update_1to1 | 2.83ms | 19.73ms | 7.57ms | 27.11ms | 14.23ms | 4.54ms |
| update_2to1 | 1.52ms | 10.32ms | 3.80ms | 13.41ms | 7.85ms | 2.26ms |
| update_4to1 | 1.05ms | 5.39ms | 2.08ms | 6.53ms | 5.46ms | 1.20ms |
| update_1000to1 | 8μs | 50μs | 19μs | 69μs | 35μs | 12μs |
| update_1to2 | 1.53ms | 10.34ms | 4.21ms | 13.66ms | 7.50ms | 2.40ms |
| update_1to4 | 730μs | 5.05ms | 2.15ms | 6.73ms | 3.45ms | 1.19ms |
| update_1to1000 | 49μs | 213μs | 269μs | 83μs | 151μs | 370μs |
| cellx1000 | 10.31ms | 108.17ms | 12.72ms | 12.64ms | 19.60ms | 14.36ms |
| cellx2500 | 34.80ms | 336.80ms | 36.65ms | 35.07ms | 59.22ms | 40.19ms |
| cellx5000 | 79.61ms | 673.13ms | 90.75ms | 93.86ms | 144.19ms | 117.21ms |
| 10x5 - 2 sources - read 20.0% (simple) | 172.70ms | 2.05s | 411.83ms | 450.74ms | 322.76ms | 223.51ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 152.99ms | 1.49s | 241.22ms | 255.71ms | 236.08ms | 171.10ms |
| 1000x12 - 4 sources - dynamic (large) | 246.36ms | 1.75s | 3.24s | 3.08s | 387.48ms | 287.64ms |
| 1000x5 - 25 sources (wide dense) | 388.01ms | 3.49s | 2.65s | 2.66s | 643.81ms | 380.99ms |
| 5x500 - 3 sources (deep) | 177.06ms | 1.21s | 226.97ms | 220.77ms | 281.78ms | 208.69ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 203.59ms | 1.69s | 404.86ms | 416.64ms | 292.29ms | 214.32ms |

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
