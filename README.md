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
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.18s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.24s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.49s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.91s |

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
| avoidablePropagation | 126.65ms | 2.38s | 204.78ms | 253.78ms | 251.44ms | 166.09ms |
| broadPropagation | 236.04ms | 4.38s | 451.95ms | 456.08ms | 452.14ms | 392.22ms |
| deepPropagation | 80.17ms | 1.49s | 160.74ms | 169.58ms | 129.65ms | 157.39ms |
| diamond | 156.29ms | 2.38s | 285.59ms | 312.75ms | 305.89ms | 209.68ms |
| mux | 295.52ms | 1.84s | 375.87ms | 382.62ms | 391.43ms | 363.58ms |
| repeatedObservers | 27.67ms | 224.41ms | 32.25ms | 41.58ms | 89.75ms | 58.56ms |
| triangle | 65.60ms | 753.48ms | 101.58ms | 109.07ms | 95.94ms | 87.09ms |
| unstable | 45.99ms | 344.33ms | 55.39ms | 74.21ms | 103.88ms | 340.39ms |
| molBench | 488.35ms | 591.54ms | 495.80ms | 483.48ms | 492.01ms | 493.43ms |
| create_signals | 31.62ms | 62.66ms | 5.51ms | 25.51ms | 127.33ms | 65.71ms |
| comp_0to1 | 23.44ms | 15.70ms | 17.94ms | 23.25ms | 40.20ms | 58.03ms |
| comp_1to1 | 11.90ms | 51.70ms | 11.05ms | 7.71ms | 24.29ms | 61.94ms |
| comp_2to1 | 24.35ms | 24.03ms | 11.71ms | 8.17ms | 18.39ms | 40.17ms |
| comp_4to1 | 3.12ms | 31.26ms | 9.89ms | 6.90ms | 15.50ms | 16.27ms |
| comp_1000to1 | 5μs | 28μs | 4μs | 4μs | 30μs | 41μs |
| comp_1to2 | 12.04ms | 35.51ms | 26.34ms | 18.04ms | 33.32ms | 47.12ms |
| comp_1to4 | 22.73ms | 23.11ms | 24.69ms | 14.28ms | 30.77ms | 46.93ms |
| comp_1to8 | 5.54ms | 25.48ms | 16.52ms | 6.12ms | 31.76ms | 44.74ms |
| comp_1to1000 | 3.21ms | 15.80ms | 4.96ms | 4.25ms | 14.91ms | 40.62ms |
| update_1to1 | 4.32ms | 26.75ms | 9.25ms | 30.45ms | 13.94ms | 6.13ms |
| update_2to1 | 4.79ms | 11.17ms | 4.47ms | 15.14ms | 6.92ms | 3.05ms |
| update_4to1 | 1.38ms | 6.52ms | 2.27ms | 7.62ms | 3.48ms | 1.55ms |
| update_1000to1 | 9μs | 69μs | 22μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.80ms | 12.45ms | 4.42ms | 15.22ms | 7.60ms | 3.06ms |
| update_1to4 | 1.64ms | 6.86ms | 2.27ms | 7.64ms | 3.59ms | 1.53ms |
| update_1to1000 | 42μs | 169μs | 54μs | 82μs | 141μs | 397μs |
| cellx1000 | 6.09ms | 76.46ms | 9.53ms | 10.12ms | 9.45ms | 8.99ms |
| cellx2500 | 16.25ms | 274.95ms | 25.41ms | 25.96ms | 31.36ms | 26.92ms |
| cellx5000 | 35.11ms | 563.25ms | 68.17ms | 59.44ms | 82.16ms | 79.88ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.48ms | 1.95s | 490.70ms | 539.82ms | 322.85ms | 248.43ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.50ms | 1.45s | 282.18ms | 299.88ms | 225.30ms | 201.28ms |
| 1000x12 - 4 sources - dynamic (large) | 276.14ms | 1.79s | 4.09s | 3.79s | 455.28ms | 356.56ms |
| 1000x5 - 25 sources (wide dense) | 532.06ms | 3.31s | 3.51s | 3.33s | 816.36ms | 472.75ms |
| 5x500 - 3 sources (deep) | 153.63ms | 1.12s | 226.43ms | 235.94ms | 227.50ms | 206.57ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 244.97ms | 1.64s | 469.86ms | 479.11ms | 328.94ms | 266.96ms |

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
