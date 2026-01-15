# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.58s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.01s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.26s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.62s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.14s |

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
| avoidablePropagation | 129.19ms | 2.39s | 199.95ms | 253.43ms | 247.52ms | 166.07ms |
| broadPropagation | 237.06ms | 4.43s | 462.95ms | 464.69ms | 428.98ms | 406.56ms |
| deepPropagation | 82.89ms | 1.51s | 161.49ms | 169.47ms | 132.01ms | 157.85ms |
| diamond | 157.02ms | 2.39s | 290.51ms | 315.61ms | 298.33ms | 217.73ms |
| mux | 302.96ms | 1.86s | 370.17ms | 381.39ms | 381.69ms | 358.05ms |
| repeatedObservers | 26.98ms | 225.74ms | 31.73ms | 41.37ms | 87.70ms | 58.74ms |
| triangle | 64.53ms | 757.63ms | 101.71ms | 112.01ms | 94.38ms | 88.42ms |
| unstable | 46.06ms | 342.08ms | 57.91ms | 74.34ms | 101.46ms | 343.25ms |
| molBench | 488.30ms | 591.45ms | 495.87ms | 438.00ms | 489.35ms | 493.05ms |
| create_signals | 31.40ms | 87.98ms | 11.56ms | 28.92ms | 72.66ms | 60.22ms |
| comp_0to1 | 13.25ms | 23.17ms | 26.30ms | 27.69ms | 41.30ms | 55.92ms |
| comp_1to1 | 15.11ms | 38.08ms | 10.33ms | 7.67ms | 24.96ms | 58.66ms |
| comp_2to1 | 11.82ms | 35.02ms | 12.73ms | 12.44ms | 17.97ms | 36.94ms |
| comp_4to1 | 2.03ms | 30.86ms | 12.59ms | 6.83ms | 17.51ms | 15.74ms |
| comp_1000to1 | 3μs | 17μs | 4μs | 4μs | 17μs | 38μs |
| comp_1to2 | 12.11ms | 34.39ms | 27.26ms | 18.20ms | 28.17ms | 42.96ms |
| comp_1to4 | 15.28ms | 18.04ms | 21.24ms | 16.32ms | 18.46ms | 43.56ms |
| comp_1to8 | 6.66ms | 22.76ms | 7.60ms | 9.88ms | 21.32ms | 41.32ms |
| comp_1to1000 | 6.29ms | 15.36ms | 6.83ms | 4.78ms | 14.50ms | 37.02ms |
| update_1to1 | 6.09ms | 24.30ms | 8.88ms | 30.62ms | 13.98ms | 6.10ms |
| update_2to1 | 4.80ms | 11.24ms | 4.73ms | 15.18ms | 7.11ms | 3.06ms |
| update_4to1 | 1.50ms | 7.27ms | 2.28ms | 7.64ms | 3.51ms | 1.57ms |
| update_1000to1 | 9μs | 65μs | 22μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.51ms | 12.07ms | 4.42ms | 15.88ms | 6.97ms | 3.06ms |
| update_1to4 | 1.52ms | 6.87ms | 2.34ms | 7.77ms | 3.56ms | 1.54ms |
| update_1to1000 | 34μs | 162μs | 547μs | 94μs | 147μs | 365μs |
| cellx1000 | 5.48ms | 71.00ms | 9.53ms | 9.62ms | 10.89ms | 9.18ms |
| cellx2500 | 16.21ms | 255.29ms | 25.91ms | 27.20ms | 27.77ms | 28.13ms |
| cellx5000 | 36.13ms | 570.84ms | 68.34ms | 68.37ms | 75.16ms | 83.84ms |
| 10x5 - 2 sources - read 20.0% (simple) | 187.60ms | 1.94s | 492.44ms | 541.35ms | 324.08ms | 245.15ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.93ms | 1.46s | 281.98ms | 298.03ms | 218.82ms | 199.21ms |
| 1000x12 - 4 sources - dynamic (large) | 272.29ms | 1.86s | 4.29s | 3.77s | 440.62ms | 356.32ms |
| 1000x5 - 25 sources (wide dense) | 534.34ms | 3.37s | 3.41s | 3.36s | 808.87ms | 493.13ms |
| 5x500 - 3 sources (deep) | 153.43ms | 1.11s | 233.33ms | 240.40ms | 225.89ms | 207.94ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 241.40ms | 1.63s | 472.72ms | 489.26ms | 326.96ms | 257.96ms |

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
