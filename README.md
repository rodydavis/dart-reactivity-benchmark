# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.94s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.12s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.86s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.26s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.41s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.27s |

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
| avoidablePropagation | 132.24ms | 2.21s | 182.21ms | 229.84ms | 238.26ms | 156.36ms |
| broadPropagation | 221.58ms | 4.08s | 393.82ms | 388.36ms | 430.11ms | 352.28ms |
| deepPropagation | 87.15ms | 1.44s | 182.68ms | 176.18ms | 131.75ms | 163.53ms |
| diamond | 145.77ms | 2.21s | 255.79ms | 304.19ms | 306.36ms | 206.09ms |
| mux | 287.23ms | 1.79s | 330.85ms | 338.75ms | 377.64ms | 317.59ms |
| repeatedObservers | 22.64ms | 220.87ms | 28.86ms | 36.42ms | 90.46ms | 50.85ms |
| triangle | 60.94ms | 740.71ms | 93.65ms | 106.06ms | 101.47ms | 84.92ms |
| unstable | 41.60ms | 319.04ms | 49.83ms | 62.37ms | 109.60ms | 325.25ms |
| molBench | 360.00ms | 481.54ms | 389.39ms | 367.86ms | 369.85ms | 387.69ms |
| create_signals | 33.97ms | 71.84ms | 9.15ms | 33.83ms | 73.09ms | 62.07ms |
| comp_0to1 | 14.50ms | 20.69ms | 21.29ms | 19.85ms | 40.48ms | 57.39ms |
| comp_1to1 | 26.69ms | 31.36ms | 15.94ms | 9.56ms | 41.70ms | 62.11ms |
| comp_2to1 | 17.92ms | 23.26ms | 26.87ms | 16.99ms | 13.57ms | 40.04ms |
| comp_4to1 | 2.77ms | 29.72ms | 12.70ms | 2.45ms | 11.36ms | 17.00ms |
| comp_1000to1 | 4μs | 16μs | 9μs | 6μs | 16μs | 48μs |
| comp_1to2 | 12.81ms | 44.50ms | 37.44ms | 16.94ms | 34.29ms | 44.83ms |
| comp_1to4 | 17.02ms | 25.74ms | 30.34ms | 27.74ms | 30.00ms | 45.14ms |
| comp_1to8 | 11.81ms | 25.64ms | 11.71ms | 12.67ms | 32.98ms | 43.41ms |
| comp_1to1000 | 5.28ms | 16.44ms | 8.12ms | 6.83ms | 16.18ms | 38.34ms |
| update_1to1 | 3.41ms | 19.61ms | 7.92ms | 26.88ms | 14.19ms | 4.49ms |
| update_2to1 | 1.65ms | 10.25ms | 3.93ms | 13.28ms | 6.95ms | 2.40ms |
| update_4to1 | 892μs | 5.42ms | 1.88ms | 6.70ms | 3.41ms | 1.13ms |
| update_1000to1 | 8μs | 48μs | 18μs | 81μs | 35μs | 15μs |
| update_1to2 | 1.62ms | 10.13ms | 3.71ms | 13.83ms | 7.47ms | 2.36ms |
| update_1to4 | 878μs | 4.94ms | 1.95ms | 6.61ms | 3.45ms | 1.40ms |
| update_1to1000 | 44μs | 164μs | 337μs | 82μs | 266μs | 392μs |
| cellx1000 | 9.20ms | 93.86ms | 11.81ms | 12.26ms | 40.30ms | 14.98ms |
| cellx2500 | 29.28ms | 301.40ms | 31.45ms | 33.51ms | 51.36ms | 40.24ms |
| cellx5000 | 68.03ms | 622.50ms | 90.63ms | 91.16ms | 131.24ms | 109.74ms |
| 10x5 - 2 sources - read 20.0% (simple) | 173.21ms | 2.05s | 411.67ms | 450.93ms | 317.43ms | 226.54ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 153.24ms | 1.49s | 241.79ms | 252.28ms | 233.12ms | 171.48ms |
| 1000x12 - 4 sources - dynamic (large) | 245.01ms | 1.70s | 3.16s | 3.08s | 382.98ms | 288.66ms |
| 1000x5 - 25 sources (wide dense) | 383.34ms | 3.36s | 2.59s | 2.63s | 642.00ms | 380.61ms |
| 5x500 - 3 sources (deep) | 171.35ms | 1.16s | 217.85ms | 219.03ms | 281.25ms | 203.37ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 200.98ms | 1.66s | 394.18ms | 412.58ms | 292.60ms | 215.38ms |

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
