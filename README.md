# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.30s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.58s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.09s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.40s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.57s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.16s |

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
| avoidablePropagation | 125.01ms | 2.40s | 198.87ms | 253.34ms | 249.22ms | 179.66ms |
| broadPropagation | 236.49ms | 4.41s | 456.10ms | 459.95ms | 438.58ms | 399.81ms |
| deepPropagation | 81.04ms | 1.48s | 163.83ms | 173.00ms | 130.97ms | 157.92ms |
| diamond | 158.09ms | 2.38s | 308.64ms | 323.91ms | 303.53ms | 222.22ms |
| mux | 293.18ms | 1.86s | 372.38ms | 375.97ms | 383.21ms | 362.66ms |
| repeatedObservers | 26.91ms | 228.72ms | 31.63ms | 41.73ms | 87.38ms | 59.07ms |
| triangle | 93.37ms | 744.59ms | 101.89ms | 110.67ms | 96.67ms | 84.14ms |
| unstable | 46.05ms | 343.09ms | 57.35ms | 73.73ms | 101.24ms | 342.87ms |
| molBench | 487.06ms | 589.78ms | 494.97ms | 482.58ms | 485.45ms | 493.18ms |
| create_signals | 23.36ms | 64.10ms | 5.82ms | 26.91ms | 114.62ms | 58.08ms |
| comp_0to1 | 19.00ms | 15.69ms | 17.87ms | 27.87ms | 21.81ms | 51.05ms |
| comp_1to1 | 19.24ms | 39.95ms | 14.42ms | 7.43ms | 24.48ms | 53.14ms |
| comp_2to1 | 19.71ms | 36.15ms | 16.37ms | 11.38ms | 13.04ms | 36.49ms |
| comp_4to1 | 4.51ms | 14.32ms | 14.91ms | 1.83ms | 12.20ms | 15.58ms |
| comp_1000to1 | 3μs | 35μs | 4μs | 5μs | 16μs | 38μs |
| comp_1to2 | 13.18ms | 38.19ms | 15.76ms | 17.04ms | 44.55ms | 43.91ms |
| comp_1to4 | 16.97ms | 31.62ms | 25.70ms | 16.14ms | 22.08ms | 44.28ms |
| comp_1to8 | 6.73ms | 20.95ms | 5.70ms | 9.09ms | 23.18ms | 42.64ms |
| comp_1to1000 | 4.78ms | 15.34ms | 5.45ms | 4.24ms | 14.56ms | 37.86ms |
| update_1to1 | 5.00ms | 23.62ms | 8.90ms | 30.57ms | 14.01ms | 6.10ms |
| update_2to1 | 4.88ms | 13.58ms | 4.48ms | 15.14ms | 7.13ms | 3.08ms |
| update_4to1 | 1.70ms | 6.93ms | 2.22ms | 7.63ms | 3.53ms | 1.60ms |
| update_1000to1 | 9μs | 68μs | 22μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.76ms | 14.05ms | 4.76ms | 15.40ms | 6.96ms | 3.07ms |
| update_1to4 | 1.55ms | 6.94ms | 2.24ms | 7.68ms | 3.59ms | 1.55ms |
| update_1to1000 | 41μs | 162μs | 968μs | 84μs | 152μs | 377μs |
| cellx1000 | 5.67ms | 88.89ms | 11.63ms | 9.41ms | 11.45ms | 10.73ms |
| cellx2500 | 18.83ms | 243.55ms | 39.92ms | 25.99ms | 28.45ms | 25.02ms |
| cellx5000 | 47.21ms | 591.38ms | 106.23ms | 67.48ms | 90.84ms | 83.13ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.22ms | 1.94s | 493.00ms | 534.61ms | 321.23ms | 240.68ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 159.69ms | 1.47s | 284.10ms | 296.32ms | 221.75ms | 199.16ms |
| 1000x12 - 4 sources - dynamic (large) | 269.30ms | 1.86s | 4.41s | 3.74s | 438.58ms | 356.57ms |
| 1000x5 - 25 sources (wide dense) | 527.45ms | 3.44s | 3.18s | 3.52s | 820.87ms | 493.53ms |
| 5x500 - 3 sources (deep) | 155.53ms | 1.10s | 230.99ms | 237.89ms | 223.73ms | 211.79ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.25ms | 1.65s | 470.49ms | 478.37ms | 330.77ms | 259.13ms |

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
