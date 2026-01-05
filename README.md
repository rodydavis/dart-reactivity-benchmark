# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.60s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.28s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.34s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.36s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.98s |

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
| avoidablePropagation | 126.01ms | 2.34s | 202.99ms | 258.32ms | 250.72ms | 166.99ms |
| broadPropagation | 238.07ms | 4.39s | 454.31ms | 452.52ms | 445.15ms | 397.61ms |
| deepPropagation | 80.51ms | 1.50s | 160.44ms | 173.96ms | 129.80ms | 161.64ms |
| diamond | 156.62ms | 2.38s | 285.71ms | 318.06ms | 303.55ms | 212.36ms |
| mux | 299.68ms | 1.84s | 371.44ms | 380.41ms | 387.16ms | 368.17ms |
| repeatedObservers | 27.72ms | 236.89ms | 31.84ms | 43.06ms | 88.08ms | 60.01ms |
| triangle | 66.42ms | 752.08ms | 101.19ms | 111.75ms | 97.98ms | 86.27ms |
| unstable | 46.10ms | 341.01ms | 54.67ms | 75.81ms | 102.37ms | 343.54ms |
| molBench | 487.15ms | 589.01ms | 494.06ms | 483.87ms | 488.76ms | 492.05ms |
| create_signals | 27.52ms | 78.41ms | 4.98ms | 28.33ms | 126.96ms | 58.47ms |
| comp_0to1 | 18.43ms | 21.22ms | 17.73ms | 33.53ms | 54.01ms | 51.86ms |
| comp_1to1 | 18.97ms | 17.20ms | 13.06ms | 8.40ms | 26.40ms | 53.83ms |
| comp_2to1 | 22.25ms | 20.40ms | 12.06ms | 13.27ms | 16.76ms | 36.15ms |
| comp_4to1 | 4.59ms | 22.43ms | 10.15ms | 2.48ms | 4.34ms | 17.18ms |
| comp_1000to1 | 4μs | 15μs | 5μs | 5μs | 17μs | 38μs |
| comp_1to2 | 11.64ms | 37.43ms | 26.48ms | 24.34ms | 30.28ms | 44.30ms |
| comp_1to4 | 16.91ms | 25.17ms | 27.66ms | 16.78ms | 25.39ms | 44.50ms |
| comp_1to8 | 6.37ms | 24.20ms | 15.43ms | 11.62ms | 25.53ms | 41.70ms |
| comp_1to1000 | 4.67ms | 15.32ms | 5.18ms | 4.70ms | 14.32ms | 37.82ms |
| update_1to1 | 6.82ms | 27.33ms | 8.98ms | 30.55ms | 13.98ms | 6.11ms |
| update_2to1 | 4.75ms | 13.69ms | 4.48ms | 15.09ms | 7.15ms | 3.10ms |
| update_4to1 | 1.19ms | 7.04ms | 2.22ms | 7.62ms | 3.56ms | 1.60ms |
| update_1000to1 | 9μs | 70μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 3.33ms | 12.32ms | 4.45ms | 15.47ms | 6.96ms | 3.13ms |
| update_1to4 | 1.47ms | 6.94ms | 2.27ms | 7.76ms | 3.62ms | 1.57ms |
| update_1to1000 | 40μs | 161μs | 40μs | 68μs | 157μs | 373μs |
| cellx1000 | 7.48ms | 70.19ms | 9.48ms | 11.16ms | 11.81ms | 9.92ms |
| cellx2500 | 16.25ms | 254.58ms | 25.00ms | 37.62ms | 53.83ms | 30.84ms |
| cellx5000 | 32.90ms | 565.84ms | 64.32ms | 117.23ms | 161.38ms | 100.17ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.18ms | 1.93s | 492.30ms | 532.58ms | 327.26ms | 239.07ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.44ms | 1.45s | 282.45ms | 297.56ms | 217.48ms | 198.67ms |
| 1000x12 - 4 sources - dynamic (large) | 269.83ms | 1.81s | 4.17s | 3.59s | 456.85ms | 370.81ms |
| 1000x5 - 25 sources (wide dense) | 524.41ms | 3.47s | 3.31s | 3.50s | 830.11ms | 490.20ms |
| 5x500 - 3 sources (deep) | 153.54ms | 1.09s | 225.83ms | 236.22ms | 232.08ms | 208.99ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 244.49ms | 1.66s | 462.36ms | 488.95ms | 331.56ms | 260.41ms |

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
