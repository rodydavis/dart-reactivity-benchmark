# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.34s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.91s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.51s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.51s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 12.37s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 28.94s |

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
| avoidablePropagation | 125.68ms | 2.35s | 201.86ms | 254.41ms | 249.46ms | 169.75ms |
| broadPropagation | 236.26ms | 4.53s | 452.20ms | 459.26ms | 443.62ms | 399.24ms |
| deepPropagation | 82.62ms | 1.54s | 161.99ms | 179.94ms | 131.14ms | 158.30ms |
| diamond | 162.50ms | 2.36s | 290.63ms | 314.48ms | 308.60ms | 221.92ms |
| mux | 294.77ms | 1.88s | 380.93ms | 400.50ms | 380.57ms | 367.09ms |
| repeatedObservers | 27.17ms | 237.43ms | 31.87ms | 43.46ms | 88.42ms | 58.63ms |
| triangle | 65.71ms | 771.45ms | 102.67ms | 112.91ms | 96.59ms | 86.85ms |
| unstable | 46.69ms | 345.39ms | 55.05ms | 76.30ms | 101.71ms | 344.80ms |
| molBench | 487.53ms | 589.89ms | 496.15ms | 486.99ms | 493.50ms | 493.98ms |
| create_signals | 33.00ms | 80.74ms | 25.06ms | 28.46ms | 86.80ms | 60.08ms |
| comp_0to1 | 12.38ms | 28.76ms | 30.15ms | 30.00ms | 44.31ms | 52.35ms |
| comp_1to1 | 15.79ms | 22.73ms | 10.69ms | 7.96ms | 28.79ms | 65.41ms |
| comp_2to1 | 17.32ms | 39.04ms | 32.91ms | 14.11ms | 25.71ms | 42.80ms |
| comp_4to1 | 3.08ms | 40.46ms | 16.96ms | 2.04ms | 4.42ms | 20.18ms |
| comp_1000to1 | 4μs | 30μs | 11μs | 5μs | 22μs | 40μs |
| comp_1to2 | 16.27ms | 46.92ms | 45.05ms | 22.41ms | 33.78ms | 52.47ms |
| comp_1to4 | 21.22ms | 27.04ms | 45.00ms | 17.45ms | 27.50ms | 52.58ms |
| comp_1to8 | 6.40ms | 31.63ms | 9.36ms | 11.09ms | 42.11ms | 46.54ms |
| comp_1to1000 | 3.28ms | 18.81ms | 9.57ms | 5.36ms | 15.02ms | 39.22ms |
| update_1to1 | 4.66ms | 23.29ms | 8.91ms | 30.56ms | 14.10ms | 6.09ms |
| update_2to1 | 4.79ms | 13.75ms | 4.51ms | 15.29ms | 7.39ms | 3.11ms |
| update_4to1 | 1.92ms | 7.52ms | 2.23ms | 7.63ms | 3.60ms | 1.57ms |
| update_1000to1 | 23μs | 68μs | 22μs | 91μs | 34μs | 15μs |
| update_1to2 | 4.78ms | 11.89ms | 4.42ms | 15.22ms | 6.98ms | 3.09ms |
| update_1to4 | 2.31ms | 6.93ms | 2.25ms | 7.66ms | 3.69ms | 1.54ms |
| update_1to1000 | 58μs | 282μs | 771μs | 111μs | 146μs | 392μs |
| cellx1000 | 6.33ms | 155.22ms | 19.48ms | 14.73ms | 27.81ms | 21.22ms |
| cellx2500 | 24.74ms | 434.72ms | 85.48ms | 62.06ms | 119.64ms | 85.86ms |
| cellx5000 | 62.42ms | 747.58ms | 167.28ms | 125.06ms | 250.39ms | 223.12ms |
| 10x5 - 2 sources - read 20.0% (simple) | 186.31ms | 1.97s | 494.01ms | 539.19ms | 329.03ms | 252.93ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 159.63ms | 1.46s | 286.36ms | 299.09ms | 221.20ms | 200.13ms |
| 1000x12 - 4 sources - dynamic (large) | 287.50ms | 1.98s | 4.03s | 3.58s | 485.05ms | 395.26ms |
| 1000x5 - 25 sources (wide dense) | 536.94ms | 3.51s | 3.32s | 4.45s | 857.13ms | 501.31ms |
| 5x500 - 3 sources (deep) | 151.00ms | 1.85s | 230.89ms | 242.88ms | 239.95ms | 213.23ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 245.43ms | 1.84s | 459.54ms | 502.81ms | 340.07ms | 270.55ms |

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
