# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.56s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.11s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.25s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.42s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.02s |

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
| avoidablePropagation | 125.75ms | 2.35s | 204.00ms | 252.22ms | 263.45ms | 164.71ms |
| broadPropagation | 245.03ms | 4.42s | 449.93ms | 459.31ms | 443.03ms | 393.88ms |
| deepPropagation | 81.34ms | 1.49s | 161.45ms | 178.03ms | 133.62ms | 157.56ms |
| diamond | 155.85ms | 2.35s | 285.83ms | 314.10ms | 313.97ms | 214.50ms |
| mux | 295.24ms | 1.84s | 374.88ms | 385.14ms | 378.05ms | 366.41ms |
| repeatedObservers | 27.20ms | 227.17ms | 32.25ms | 41.65ms | 89.48ms | 58.60ms |
| triangle | 67.46ms | 748.72ms | 104.20ms | 110.51ms | 97.49ms | 86.51ms |
| unstable | 45.70ms | 341.19ms | 55.73ms | 73.48ms | 103.66ms | 341.90ms |
| molBench | 487.31ms | 589.46ms | 495.87ms | 488.16ms | 490.08ms | 492.49ms |
| create_signals | 31.20ms | 49.45ms | 4.79ms | 26.59ms | 72.07ms | 60.60ms |
| comp_0to1 | 10.37ms | 15.63ms | 21.75ms | 30.67ms | 40.41ms | 55.46ms |
| comp_1to1 | 20.18ms | 38.48ms | 14.69ms | 7.56ms | 28.94ms | 58.82ms |
| comp_2to1 | 16.97ms | 42.70ms | 16.46ms | 11.26ms | 29.15ms | 38.03ms |
| comp_4to1 | 2.45ms | 15.06ms | 14.71ms | 2.00ms | 12.44ms | 15.83ms |
| comp_1000to1 | 3μs | 15μs | 4μs | 5μs | 15μs | 38μs |
| comp_1to2 | 14.18ms | 34.48ms | 15.54ms | 20.32ms | 36.19ms | 43.16ms |
| comp_1to4 | 13.90ms | 17.78ms | 21.99ms | 16.03ms | 21.80ms | 43.13ms |
| comp_1to8 | 5.11ms | 20.48ms | 7.56ms | 10.15ms | 24.00ms | 41.54ms |
| comp_1to1000 | 6.29ms | 15.68ms | 5.93ms | 4.66ms | 13.96ms | 37.48ms |
| update_1to1 | 3.96ms | 23.07ms | 8.92ms | 30.57ms | 13.98ms | 6.09ms |
| update_2to1 | 3.60ms | 11.53ms | 4.48ms | 15.23ms | 7.08ms | 3.08ms |
| update_4to1 | 1.08ms | 7.39ms | 2.25ms | 7.62ms | 3.52ms | 1.58ms |
| update_1000to1 | 9μs | 64μs | 23μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.79ms | 13.78ms | 4.45ms | 15.48ms | 6.97ms | 3.10ms |
| update_1to4 | 2.32ms | 6.96ms | 2.30ms | 7.76ms | 3.59ms | 1.55ms |
| update_1to1000 | 45μs | 157μs | 906μs | 84μs | 146μs | 362μs |
| cellx1000 | 5.46ms | 74.17ms | 9.36ms | 9.47ms | 11.28ms | 10.02ms |
| cellx2500 | 14.85ms | 256.86ms | 24.72ms | 25.43ms | 29.96ms | 24.45ms |
| cellx5000 | 31.20ms | 555.85ms | 62.86ms | 58.87ms | 83.28ms | 76.48ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.49ms | 1.93s | 490.97ms | 536.13ms | 321.53ms | 242.31ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 163.00ms | 1.49s | 280.38ms | 297.57ms | 219.76ms | 197.87ms |
| 1000x12 - 4 sources - dynamic (large) | 276.09ms | 1.88s | 4.18s | 3.57s | 445.77ms | 357.93ms |
| 1000x5 - 25 sources (wide dense) | 533.16ms | 3.43s | 3.37s | 3.51s | 820.83ms | 497.33ms |
| 5x500 - 3 sources (deep) | 152.61ms | 1.09s | 233.08ms | 234.28ms | 226.20ms | 203.84ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.09ms | 1.65s | 462.94ms | 486.96ms | 329.08ms | 259.39ms |

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
