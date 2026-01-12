# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 2.96s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.22s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 4.87s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 9.60s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 9.71s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.94s |

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
| avoidablePropagation | 133.04ms | 2.26s | 182.67ms | 231.36ms | 241.31ms | 157.95ms |
| broadPropagation | 221.12ms | 4.13s | 393.61ms | 382.79ms | 440.61ms | 352.57ms |
| deepPropagation | 86.16ms | 1.45s | 183.67ms | 177.89ms | 132.34ms | 166.13ms |
| diamond | 148.63ms | 2.28s | 257.42ms | 305.36ms | 309.56ms | 211.87ms |
| mux | 293.20ms | 1.91s | 338.50ms | 341.69ms | 374.86ms | 321.96ms |
| repeatedObservers | 22.90ms | 223.75ms | 28.99ms | 36.63ms | 92.97ms | 50.97ms |
| triangle | 61.95ms | 750.52ms | 94.88ms | 101.50ms | 101.97ms | 84.90ms |
| unstable | 43.17ms | 332.04ms | 50.49ms | 62.26ms | 111.31ms | 336.43ms |
| molBench | 361.95ms | 483.22ms | 390.16ms | 368.52ms | 370.30ms | 389.44ms |
| create_signals | 31.48ms | 62.69ms | 7.67ms | 37.69ms | 66.77ms | 62.11ms |
| comp_0to1 | 17.26ms | 18.10ms | 21.25ms | 19.41ms | 19.23ms | 51.41ms |
| comp_1to1 | 26.53ms | 45.69ms | 15.56ms | 10.06ms | 27.08ms | 54.49ms |
| comp_2to1 | 18.93ms | 25.62ms | 19.27ms | 12.29ms | 23.64ms | 41.09ms |
| comp_4to1 | 2.70ms | 14.69ms | 26.52ms | 4.55ms | 13.22ms | 16.76ms |
| comp_1000to1 | 6μs | 19μs | 7μs | 6μs | 26μs | 56μs |
| comp_1to2 | 10.48ms | 42.69ms | 21.83ms | 19.11ms | 23.15ms | 45.58ms |
| comp_1to4 | 15.41ms | 26.32ms | 41.03ms | 26.95ms | 43.83ms | 46.35ms |
| comp_1to8 | 6.69ms | 25.41ms | 10.19ms | 10.33ms | 25.16ms | 43.52ms |
| comp_1to1000 | 5.45ms | 16.80ms | 7.43ms | 6.14ms | 16.73ms | 38.89ms |
| update_1to1 | 3.94ms | 19.79ms | 7.64ms | 26.75ms | 14.08ms | 4.88ms |
| update_2to1 | 1.62ms | 10.24ms | 3.81ms | 13.44ms | 6.87ms | 2.54ms |
| update_4to1 | 895μs | 5.50ms | 1.90ms | 6.62ms | 3.47ms | 1.27ms |
| update_1000to1 | 7μs | 48μs | 21μs | 65μs | 34μs | 11μs |
| update_1to2 | 1.66ms | 9.97ms | 3.98ms | 13.38ms | 6.89ms | 2.55ms |
| update_1to4 | 921μs | 5.02ms | 1.92ms | 6.64ms | 3.63ms | 1.15ms |
| update_1to1000 | 52μs | 171μs | 194μs | 80μs | 182μs | 373μs |
| cellx1000 | 9.13ms | 112.20ms | 12.89ms | 13.80ms | 19.70ms | 17.54ms |
| cellx2500 | 32.52ms | 301.05ms | 35.56ms | 36.60ms | 72.22ms | 55.73ms |
| cellx5000 | 68.38ms | 660.30ms | 109.20ms | 101.03ms | 164.36ms | 157.54ms |
| 10x5 - 2 sources - read 20.0% (simple) | 173.35ms | 2.05s | 413.21ms | 450.46ms | 315.67ms | 227.31ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 152.58ms | 1.49s | 242.25ms | 251.56ms | 234.37ms | 171.82ms |
| 1000x12 - 4 sources - dynamic (large) | 243.09ms | 1.75s | 3.27s | 3.13s | 389.07ms | 293.65ms |
| 1000x5 - 25 sources (wide dense) | 387.85ms | 3.46s | 2.77s | 2.86s | 638.79ms | 380.73ms |
| 5x500 - 3 sources (deep) | 172.03ms | 1.27s | 226.70ms | 228.90ms | 272.18ms | 210.81ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 202.07ms | 1.70s | 406.26ms | 422.17ms | 293.60ms | 216.81ms |

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
