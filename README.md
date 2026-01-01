# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.26s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.65s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.09s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.25s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.29s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.85s |

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
| avoidablePropagation | 125.38ms | 2.35s | 205.28ms | 254.46ms | 239.41ms | 169.94ms |
| broadPropagation | 236.98ms | 4.34s | 457.36ms | 458.15ms | 442.26ms | 407.17ms |
| deepPropagation | 82.19ms | 1.49s | 162.55ms | 172.56ms | 129.81ms | 156.63ms |
| diamond | 159.58ms | 2.37s | 286.18ms | 313.23ms | 306.75ms | 221.43ms |
| mux | 296.25ms | 1.85s | 372.00ms | 382.16ms | 380.45ms | 362.16ms |
| repeatedObservers | 27.20ms | 229.61ms | 31.92ms | 41.34ms | 94.99ms | 58.51ms |
| triangle | 64.83ms | 750.49ms | 102.70ms | 110.80ms | 94.68ms | 86.72ms |
| unstable | 46.03ms | 343.24ms | 54.80ms | 73.98ms | 103.08ms | 342.59ms |
| molBench | 487.50ms | 588.46ms | 493.82ms | 487.93ms | 491.46ms | 492.96ms |
| create_signals | 28.84ms | 62.33ms | 5.47ms | 26.98ms | 74.59ms | 56.90ms |
| comp_0to1 | 13.83ms | 15.78ms | 17.67ms | 28.21ms | 41.09ms | 50.80ms |
| comp_1to1 | 15.58ms | 43.80ms | 14.32ms | 7.58ms | 37.32ms | 52.51ms |
| comp_2to1 | 12.62ms | 34.53ms | 15.55ms | 8.61ms | 29.80ms | 36.75ms |
| comp_4to1 | 2.48ms | 13.43ms | 14.29ms | 6.83ms | 4.42ms | 17.56ms |
| comp_1000to1 | 3μs | 19μs | 4μs | 5μs | 18μs | 38μs |
| comp_1to2 | 10.28ms | 38.43ms | 15.88ms | 21.31ms | 30.36ms | 46.36ms |
| comp_1to4 | 14.39ms | 21.16ms | 27.07ms | 23.07ms | 28.16ms | 45.95ms |
| comp_1to8 | 4.51ms | 23.81ms | 6.95ms | 8.73ms | 26.75ms | 42.47ms |
| comp_1to1000 | 3.30ms | 15.84ms | 5.54ms | 4.29ms | 14.19ms | 37.03ms |
| update_1to1 | 5.03ms | 25.37ms | 8.97ms | 30.66ms | 14.01ms | 6.15ms |
| update_2to1 | 4.35ms | 11.66ms | 4.50ms | 15.23ms | 7.14ms | 3.05ms |
| update_4to1 | 987μs | 7.00ms | 2.21ms | 7.59ms | 3.54ms | 1.53ms |
| update_1000to1 | 15μs | 69μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.76ms | 13.54ms | 4.42ms | 15.28ms | 7.03ms | 3.07ms |
| update_1to4 | 1.55ms | 7.57ms | 2.26ms | 7.69ms | 3.99ms | 1.50ms |
| update_1to1000 | 36μs | 162μs | 1.09ms | 99μs | 167μs | 385μs |
| cellx1000 | 5.69ms | 80.24ms | 10.65ms | 9.64ms | 10.31ms | 9.51ms |
| cellx2500 | 17.59ms | 260.81ms | 25.89ms | 26.74ms | 27.48ms | 27.13ms |
| cellx5000 | 47.95ms | 578.35ms | 66.14ms | 65.78ms | 68.46ms | 84.73ms |
| 10x5 - 2 sources - read 20.0% (simple) | 187.69ms | 1.91s | 542.35ms | 536.26ms | 325.94ms | 263.93ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.53ms | 1.45s | 283.74ms | 296.34ms | 223.68ms | 216.40ms |
| 1000x12 - 4 sources - dynamic (large) | 270.88ms | 1.77s | 4.06s | 3.57s | 452.30ms | 370.67ms |
| 1000x5 - 25 sources (wide dense) | 529.39ms | 3.38s | 3.30s | 3.51s | 822.22ms | 501.46ms |
| 5x500 - 3 sources (deep) | 154.98ms | 1.10s | 233.50ms | 242.34ms | 229.28ms | 210.59ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 242.56ms | 1.67s | 462.12ms | 492.40ms | 326.67ms | 266.47ms |

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
