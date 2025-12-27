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
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.05s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.21s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.37s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.49s |

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
| avoidablePropagation | 124.82ms | 2.46s | 204.55ms | 256.76ms | 240.48ms | 164.94ms |
| broadPropagation | 236.07ms | 4.47s | 449.07ms | 454.07ms | 437.53ms | 391.80ms |
| deepPropagation | 82.00ms | 1.50s | 163.09ms | 173.36ms | 126.50ms | 156.47ms |
| diamond | 159.13ms | 2.38s | 288.55ms | 328.36ms | 299.60ms | 207.63ms |
| mux | 300.70ms | 1.83s | 378.13ms | 383.74ms | 376.26ms | 357.94ms |
| repeatedObservers | 26.79ms | 227.14ms | 31.98ms | 42.75ms | 88.05ms | 59.26ms |
| triangle | 66.21ms | 760.62ms | 103.15ms | 109.58ms | 93.26ms | 84.02ms |
| unstable | 46.11ms | 343.73ms | 55.04ms | 75.05ms | 101.60ms | 343.06ms |
| molBench | 487.52ms | 590.35ms | 495.52ms | 489.55ms | 487.27ms | 493.22ms |
| create_signals | 29.43ms | 73.39ms | 5.47ms | 24.47ms | 71.68ms | 68.29ms |
| comp_0to1 | 18.27ms | 25.62ms | 18.52ms | 27.91ms | 18.35ms | 61.35ms |
| comp_1to1 | 18.82ms | 27.68ms | 13.09ms | 13.65ms | 29.03ms | 60.94ms |
| comp_2to1 | 23.83ms | 8.96ms | 10.52ms | 10.92ms | 13.96ms | 37.95ms |
| comp_4to1 | 5.09ms | 30.22ms | 13.95ms | 1.95ms | 4.49ms | 16.32ms |
| comp_1000to1 | 4μs | 15μs | 4μs | 5μs | 15μs | 39μs |
| comp_1to2 | 14.51ms | 35.62ms | 29.79ms | 24.69ms | 30.54ms | 44.42ms |
| comp_1to4 | 19.86ms | 19.39ms | 22.31ms | 23.60ms | 35.41ms | 44.98ms |
| comp_1to8 | 6.55ms | 21.94ms | 7.87ms | 7.47ms | 34.16ms | 42.34ms |
| comp_1to1000 | 3.17ms | 15.13ms | 9.38ms | 5.93ms | 14.91ms | 37.92ms |
| update_1to1 | 4.98ms | 27.28ms | 8.96ms | 30.54ms | 13.98ms | 6.10ms |
| update_2to1 | 4.86ms | 11.45ms | 4.59ms | 15.27ms | 6.95ms | 3.05ms |
| update_4to1 | 1.32ms | 7.07ms | 2.28ms | 7.64ms | 3.53ms | 1.55ms |
| update_1000to1 | 9μs | 69μs | 31μs | 77μs | 35μs | 15μs |
| update_1to2 | 4.72ms | 13.89ms | 4.42ms | 15.21ms | 7.63ms | 3.07ms |
| update_1to4 | 1.03ms | 6.96ms | 2.30ms | 7.67ms | 3.67ms | 1.52ms |
| update_1to1000 | 43μs | 161μs | 1.09ms | 64μs | 145μs | 371μs |
| cellx1000 | 5.87ms | 78.29ms | 9.55ms | 10.25ms | 12.86ms | 10.63ms |
| cellx2500 | 18.74ms | 269.28ms | 28.46ms | 28.74ms | 31.70ms | 36.81ms |
| cellx5000 | 57.88ms | 577.61ms | 86.19ms | 77.47ms | 96.69ms | 130.07ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.42ms | 1.92s | 490.58ms | 538.24ms | 318.30ms | 246.39ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.66ms | 1.50s | 285.32ms | 296.54ms | 213.63ms | 200.62ms |
| 1000x12 - 4 sources - dynamic (large) | 285.52ms | 1.95s | 4.10s | 3.58s | 458.22ms | 369.29ms |
| 1000x5 - 25 sources (wide dense) | 535.20ms | 3.49s | 3.35s | 3.42s | 821.32ms | 497.27ms |
| 5x500 - 3 sources (deep) | 156.13ms | 1.11s | 233.95ms | 242.28ms | 229.34ms | 206.10ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.79ms | 1.70s | 455.98ms | 486.76ms | 328.10ms | 259.84ms |

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
