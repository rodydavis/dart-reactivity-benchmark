# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.91s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.08s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.69s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.30s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.31s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.12s |

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
| avoidablePropagation | 131.90ms | 2.24s | 182.50ms | 229.45ms | 238.39ms | 156.33ms |
| broadPropagation | 219.75ms | 4.10s | 392.18ms | 392.98ms | 420.16ms | 354.57ms |
| deepPropagation | 88.76ms | 1.44s | 184.62ms | 177.11ms | 131.75ms | 164.57ms |
| diamond | 145.90ms | 2.25s | 290.34ms | 302.08ms | 305.09ms | 206.93ms |
| mux | 292.43ms | 1.73s | 332.07ms | 340.36ms | 374.20ms | 320.17ms |
| repeatedObservers | 23.27ms | 217.50ms | 28.68ms | 36.47ms | 84.49ms | 50.82ms |
| triangle | 62.50ms | 722.84ms | 93.75ms | 100.52ms | 100.92ms | 85.08ms |
| unstable | 41.61ms | 317.27ms | 50.29ms | 61.60ms | 102.98ms | 325.62ms |
| molBench | 358.64ms | 478.41ms | 388.28ms | 365.76ms | 369.38ms | 386.98ms |
| create_signals | 29.30ms | 59.11ms | 7.00ms | 24.26ms | 63.80ms | 60.59ms |
| comp_0to1 | 19.20ms | 15.11ms | 20.57ms | 26.83ms | 18.68ms | 52.02ms |
| comp_1to1 | 20.58ms | 44.41ms | 15.72ms | 17.62ms | 48.65ms | 54.10ms |
| comp_2to1 | 25.31ms | 31.30ms | 21.47ms | 10.51ms | 14.75ms | 35.45ms |
| comp_4to1 | 3.74ms | 22.22ms | 12.59ms | 2.61ms | 4.99ms | 16.28ms |
| comp_1000to1 | 4μs | 29μs | 6μs | 7μs | 16μs | 41μs |
| comp_1to2 | 11.24ms | 27.82ms | 33.98ms | 17.56ms | 25.63ms | 45.45ms |
| comp_1to4 | 16.44ms | 25.04ms | 33.01ms | 19.95ms | 28.60ms | 44.84ms |
| comp_1to8 | 6.84ms | 33.23ms | 8.86ms | 10.88ms | 25.51ms | 45.16ms |
| comp_1to1000 | 4.36ms | 15.91ms | 8.06ms | 5.63ms | 14.71ms | 38.46ms |
| update_1to1 | 3.01ms | 19.59ms | 7.28ms | 28.01ms | 13.67ms | 4.78ms |
| update_2to1 | 1.54ms | 9.96ms | 3.73ms | 13.21ms | 7.03ms | 2.44ms |
| update_4to1 | 774μs | 5.42ms | 1.84ms | 6.68ms | 3.48ms | 1.24ms |
| update_1000to1 | 7μs | 48μs | 21μs | 133μs | 44μs | 11μs |
| update_1to2 | 1.50ms | 9.86ms | 3.88ms | 13.52ms | 6.83ms | 2.47ms |
| update_1to4 | 865μs | 4.91ms | 2.00ms | 6.85ms | 3.48ms | 1.27ms |
| update_1to1000 | 38μs | 160μs | 570μs | 87μs | 151μs | 376μs |
| cellx1000 | 8.24ms | 81.60ms | 11.69ms | 10.99ms | 17.64ms | 13.90ms |
| cellx2500 | 24.64ms | 257.96ms | 29.49ms | 30.54ms | 42.34ms | 34.80ms |
| cellx5000 | 50.81ms | 588.86ms | 82.07ms | 71.22ms | 86.48ms | 90.26ms |
| 10x5 - 2 sources - read 20.0% (simple) | 172.69ms | 2.00s | 410.97ms | 449.78ms | 320.57ms | 227.27ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 152.49ms | 1.47s | 242.26ms | 252.01ms | 234.50ms | 170.72ms |
| 1000x12 - 4 sources - dynamic (large) | 236.32ms | 1.73s | 3.18s | 3.04s | 386.02ms | 285.04ms |
| 1000x5 - 25 sources (wide dense) | 381.35ms | 3.39s | 2.60s | 2.62s | 631.42ms | 380.35ms |
| 5x500 - 3 sources (deep) | 174.65ms | 1.15s | 221.77ms | 214.26ms | 270.02ms | 206.67ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 201.25ms | 1.63s | 397.63ms | 403.56ms | 288.64ms | 216.28ms |

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
