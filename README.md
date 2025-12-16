# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.26s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.61s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.24s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.10s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.59s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.00s |

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
| avoidablePropagation | 126.07ms | 2.37s | 204.64ms | 268.00ms | 237.41ms | 168.47ms |
| broadPropagation | 237.08ms | 4.38s | 456.84ms | 465.74ms | 439.79ms | 398.27ms |
| deepPropagation | 80.80ms | 1.48s | 160.09ms | 175.39ms | 131.30ms | 157.44ms |
| diamond | 157.19ms | 2.39s | 287.95ms | 321.45ms | 304.34ms | 210.72ms |
| mux | 297.17ms | 1.85s | 372.60ms | 392.44ms | 384.98ms | 369.82ms |
| repeatedObservers | 27.68ms | 231.25ms | 32.58ms | 43.23ms | 87.94ms | 58.56ms |
| triangle | 68.84ms | 750.38ms | 101.05ms | 111.65ms | 95.23ms | 86.63ms |
| unstable | 46.43ms | 343.69ms | 54.53ms | 75.41ms | 101.62ms | 344.25ms |
| molBench | 487.04ms | 591.30ms | 496.57ms | 483.42ms | 493.61ms | 492.84ms |
| create_signals | 27.52ms | 53.52ms | 5.42ms | 26.98ms | 123.36ms | 63.09ms |
| comp_0to1 | 11.29ms | 19.17ms | 17.69ms | 28.05ms | 38.15ms | 54.61ms |
| comp_1to1 | 18.66ms | 43.82ms | 13.20ms | 7.99ms | 48.99ms | 59.13ms |
| comp_2to1 | 15.20ms | 24.47ms | 17.63ms | 14.22ms | 22.99ms | 40.71ms |
| comp_4to1 | 2.91ms | 15.47ms | 25.46ms | 1.92ms | 15.69ms | 15.88ms |
| comp_1000to1 | 3μs | 26μs | 4μs | 5μs | 31μs | 38μs |
| comp_1to2 | 14.46ms | 38.29ms | 24.16ms | 17.36ms | 39.24ms | 43.87ms |
| comp_1to4 | 14.49ms | 27.11ms | 21.41ms | 14.97ms | 22.53ms | 43.37ms |
| comp_1to8 | 5.86ms | 26.76ms | 8.78ms | 6.28ms | 25.26ms | 41.36ms |
| comp_1to1000 | 3.06ms | 15.47ms | 6.67ms | 4.23ms | 14.65ms | 37.14ms |
| update_1to1 | 7.32ms | 28.02ms | 8.94ms | 30.57ms | 13.95ms | 6.14ms |
| update_2to1 | 4.74ms | 13.53ms | 4.55ms | 15.21ms | 7.15ms | 3.08ms |
| update_4to1 | 1.90ms | 7.45ms | 2.22ms | 7.62ms | 3.54ms | 1.61ms |
| update_1000to1 | 9μs | 73μs | 22μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.74ms | 13.84ms | 4.45ms | 15.27ms | 7.02ms | 3.08ms |
| update_1to4 | 2.05ms | 6.94ms | 2.25ms | 7.69ms | 3.61ms | 1.57ms |
| update_1to1000 | 40μs | 171μs | 421μs | 67μs | 144μs | 373μs |
| cellx1000 | 6.38ms | 84.90ms | 9.63ms | 12.05ms | 12.19ms | 9.52ms |
| cellx2500 | 15.68ms | 276.95ms | 26.17ms | 27.98ms | 38.58ms | 29.39ms |
| cellx5000 | 36.01ms | 568.64ms | 69.40ms | 71.16ms | 138.64ms | 98.28ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.09ms | 1.90s | 491.32ms | 536.12ms | 325.40ms | 236.78ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.42ms | 1.46s | 278.92ms | 300.84ms | 222.41ms | 197.43ms |
| 1000x12 - 4 sources - dynamic (large) | 275.06ms | 1.84s | 4.17s | 3.46s | 453.80ms | 369.39ms |
| 1000x5 - 25 sources (wide dense) | 525.31ms | 3.42s | 3.52s | 3.42s | 826.85ms | 495.73ms |
| 5x500 - 3 sources (deep) | 154.32ms | 1.10s | 227.80ms | 242.95ms | 231.67ms | 207.61ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 241.32ms | 1.63s | 469.18ms | 491.54ms | 331.37ms | 263.13ms |

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
