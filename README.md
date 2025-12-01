# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.27s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.67s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.17s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.43s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.76s |
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
| avoidablePropagation | 126.51ms | 2.37s | 204.43ms | 254.71ms | 265.98ms | 179.98ms |
| broadPropagation | 238.16ms | 4.34s | 463.94ms | 457.58ms | 444.29ms | 397.06ms |
| deepPropagation | 80.45ms | 1.49s | 164.92ms | 173.65ms | 131.41ms | 156.44ms |
| diamond | 156.73ms | 2.35s | 289.85ms | 317.23ms | 307.99ms | 219.78ms |
| mux | 293.15ms | 1.84s | 368.69ms | 379.57ms | 383.45ms | 366.61ms |
| repeatedObservers | 27.10ms | 225.74ms | 32.19ms | 43.95ms | 88.66ms | 58.56ms |
| triangle | 65.05ms | 744.72ms | 101.34ms | 111.02ms | 99.84ms | 85.82ms |
| unstable | 46.05ms | 342.77ms | 55.29ms | 77.67ms | 104.01ms | 343.43ms |
| molBench | 482.35ms | 592.41ms | 494.35ms | 485.02ms | 490.70ms | 493.55ms |
| create_signals | 27.29ms | 52.26ms | 4.82ms | 27.48ms | 129.72ms | 65.29ms |
| comp_0to1 | 11.93ms | 18.97ms | 18.11ms | 30.20ms | 37.97ms | 58.47ms |
| comp_1to1 | 15.15ms | 24.75ms | 12.81ms | 7.81ms | 25.90ms | 56.08ms |
| comp_2to1 | 15.25ms | 17.03ms | 17.42ms | 12.06ms | 17.83ms | 43.15ms |
| comp_4to1 | 4.43ms | 21.59ms | 8.64ms | 7.49ms | 18.45ms | 16.56ms |
| comp_1000to1 | 4μs | 15μs | 6μs | 6μs | 19μs | 37μs |
| comp_1to2 | 16.12ms | 35.13ms | 32.15ms | 18.24ms | 31.71ms | 46.97ms |
| comp_1to4 | 20.27ms | 19.30ms | 21.53ms | 14.60ms | 25.29ms | 46.31ms |
| comp_1to8 | 5.87ms | 21.35ms | 7.39ms | 5.86ms | 24.33ms | 42.30ms |
| comp_1to1000 | 3.10ms | 15.54ms | 4.66ms | 4.20ms | 13.96ms | 37.63ms |
| update_1to1 | 3.67ms | 24.82ms | 8.87ms | 30.54ms | 14.01ms | 6.10ms |
| update_2to1 | 4.78ms | 13.55ms | 4.49ms | 15.19ms | 7.15ms | 3.07ms |
| update_4to1 | 999μs | 7.01ms | 2.25ms | 7.62ms | 3.49ms | 1.60ms |
| update_1000to1 | 31μs | 70μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.72ms | 13.79ms | 4.42ms | 15.22ms | 6.95ms | 3.08ms |
| update_1to4 | 985μs | 6.89ms | 2.29ms | 7.67ms | 3.57ms | 1.55ms |
| update_1to1000 | 42μs | 160μs | 158μs | 85μs | 144μs | 365μs |
| cellx1000 | 7.25ms | 72.62ms | 11.38ms | 10.89ms | 10.11ms | 10.84ms |
| cellx2500 | 15.51ms | 246.34ms | 25.74ms | 26.83ms | 32.13ms | 28.13ms |
| cellx5000 | 32.77ms | 554.41ms | 66.69ms | 60.10ms | 88.41ms | 90.91ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.95ms | 1.92s | 495.45ms | 540.87ms | 323.62ms | 244.00ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.38ms | 1.48s | 281.06ms | 297.97ms | 217.92ms | 222.91ms |
| 1000x12 - 4 sources - dynamic (large) | 278.49ms | 1.89s | 4.38s | 3.87s | 446.83ms | 364.42ms |
| 1000x5 - 25 sources (wide dense) | 544.89ms | 3.40s | 3.48s | 3.39s | 818.75ms | 501.15ms |
| 5x500 - 3 sources (deep) | 154.56ms | 1.10s | 229.46ms | 239.89ms | 229.99ms | 216.25ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.13ms | 1.64s | 468.99ms | 492.52ms | 327.10ms | 264.25ms |

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
