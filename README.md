# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.34s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.65s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.19s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.41s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.53s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.37s |

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
| avoidablePropagation | 125.06ms | 2.37s | 204.19ms | 265.84ms | 250.14ms | 169.58ms |
| broadPropagation | 237.11ms | 4.55s | 446.41ms | 456.88ms | 440.20ms | 405.56ms |
| deepPropagation | 82.41ms | 1.50s | 161.97ms | 172.57ms | 131.60ms | 154.84ms |
| diamond | 158.59ms | 2.40s | 287.82ms | 321.46ms | 302.23ms | 221.61ms |
| mux | 299.20ms | 1.86s | 370.67ms | 378.56ms | 392.37ms | 362.75ms |
| repeatedObservers | 26.92ms | 229.21ms | 31.83ms | 41.91ms | 88.10ms | 59.89ms |
| triangle | 64.82ms | 759.82ms | 100.87ms | 111.97ms | 98.20ms | 86.13ms |
| unstable | 45.95ms | 344.55ms | 54.59ms | 76.20ms | 103.32ms | 344.23ms |
| molBench | 487.55ms | 591.00ms | 494.59ms | 484.27ms | 488.95ms | 492.68ms |
| create_signals | 23.40ms | 52.17ms | 5.49ms | 27.92ms | 116.48ms | 68.19ms |
| comp_0to1 | 18.79ms | 19.69ms | 18.48ms | 23.21ms | 46.50ms | 60.34ms |
| comp_1to1 | 19.54ms | 29.82ms | 12.14ms | 7.46ms | 25.33ms | 59.18ms |
| comp_2to1 | 21.30ms | 11.92ms | 12.05ms | 11.81ms | 18.57ms | 39.40ms |
| comp_4to1 | 6.02ms | 28.18ms | 9.20ms | 5.83ms | 12.49ms | 16.27ms |
| comp_1000to1 | 3μs | 16μs | 5μs | 5μs | 15μs | 38μs |
| comp_1to2 | 13.24ms | 47.27ms | 23.74ms | 20.60ms | 43.97ms | 44.30ms |
| comp_1to4 | 15.56ms | 23.23ms | 30.11ms | 28.63ms | 28.07ms | 43.88ms |
| comp_1to8 | 7.14ms | 23.13ms | 14.31ms | 10.60ms | 32.76ms | 42.58ms |
| comp_1to1000 | 6.55ms | 15.97ms | 8.80ms | 6.14ms | 14.83ms | 37.40ms |
| update_1to1 | 4.98ms | 22.40ms | 8.90ms | 30.67ms | 13.95ms | 6.14ms |
| update_2to1 | 4.69ms | 12.07ms | 4.54ms | 15.14ms | 6.91ms | 3.39ms |
| update_4to1 | 984μs | 6.90ms | 2.25ms | 7.59ms | 3.50ms | 1.56ms |
| update_1000to1 | 23μs | 69μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.73ms | 14.34ms | 4.49ms | 15.23ms | 7.60ms | 3.07ms |
| update_1to4 | 1.01ms | 6.88ms | 2.33ms | 7.64ms | 3.58ms | 1.56ms |
| update_1to1000 | 42μs | 164μs | 1.49ms | 66μs | 140μs | 370μs |
| cellx1000 | 5.99ms | 86.38ms | 9.80ms | 12.67ms | 10.70ms | 10.39ms |
| cellx2500 | 20.92ms | 278.09ms | 32.71ms | 29.33ms | 32.58ms | 34.75ms |
| cellx5000 | 56.05ms | 584.13ms | 78.64ms | 77.00ms | 84.34ms | 108.22ms |
| 10x5 - 2 sources - read 20.0% (simple) | 185.19ms | 1.93s | 489.70ms | 541.43ms | 322.83ms | 243.92ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.03ms | 1.46s | 284.37ms | 299.00ms | 221.32ms | 197.86ms |
| 1000x12 - 4 sources - dynamic (large) | 298.00ms | 1.91s | 4.12s | 3.71s | 461.88ms | 365.22ms |
| 1000x5 - 25 sources (wide dense) | 535.43ms | 3.42s | 3.50s | 3.49s | 828.27ms | 494.34ms |
| 5x500 - 3 sources (deep) | 156.27ms | 1.10s | 231.02ms | 239.44ms | 232.75ms | 209.35ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.61ms | 1.67s | 464.58ms | 486.55ms | 329.65ms | 262.21ms |

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
