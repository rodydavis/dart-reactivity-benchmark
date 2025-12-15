# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.24s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.58s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.04s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.31s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.40s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.24s |

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
| avoidablePropagation | 125.70ms | 2.37s | 204.56ms | 250.69ms | 244.98ms | 165.25ms |
| broadPropagation | 235.74ms | 4.49s | 473.12ms | 463.76ms | 443.17ms | 389.68ms |
| deepPropagation | 82.25ms | 1.50s | 164.97ms | 169.62ms | 128.50ms | 161.97ms |
| diamond | 156.13ms | 2.41s | 300.29ms | 311.22ms | 297.87ms | 211.38ms |
| mux | 297.74ms | 1.85s | 372.34ms | 382.49ms | 378.44ms | 365.29ms |
| repeatedObservers | 26.93ms | 235.49ms | 32.20ms | 41.14ms | 87.19ms | 58.31ms |
| triangle | 65.33ms | 751.68ms | 103.43ms | 110.53ms | 95.95ms | 91.00ms |
| unstable | 46.79ms | 344.47ms | 54.87ms | 75.63ms | 101.70ms | 343.80ms |
| molBench | 487.74ms | 590.48ms | 493.90ms | 482.60ms | 486.70ms | 493.19ms |
| create_signals | 33.20ms | 52.31ms | 5.45ms | 30.75ms | 115.16ms | 64.68ms |
| comp_0to1 | 11.33ms | 15.65ms | 17.34ms | 23.93ms | 22.10ms | 50.76ms |
| comp_1to1 | 14.98ms | 45.55ms | 14.20ms | 7.53ms | 48.14ms | 59.68ms |
| comp_2to1 | 13.10ms | 25.75ms | 19.32ms | 12.18ms | 12.99ms | 38.13ms |
| comp_4to1 | 4.86ms | 16.10ms | 11.11ms | 2.03ms | 4.35ms | 16.09ms |
| comp_1000to1 | 3μs | 15μs | 7μs | 4μs | 17μs | 38μs |
| comp_1to2 | 11.82ms | 37.25ms | 14.02ms | 17.99ms | 27.89ms | 46.53ms |
| comp_1to4 | 14.25ms | 23.33ms | 16.32ms | 21.66ms | 24.00ms | 48.92ms |
| comp_1to8 | 5.13ms | 23.54ms | 5.17ms | 8.86ms | 23.09ms | 42.69ms |
| comp_1to1000 | 3.04ms | 15.60ms | 3.60ms | 4.13ms | 14.56ms | 37.02ms |
| update_1to1 | 5.70ms | 24.02ms | 8.93ms | 30.63ms | 13.98ms | 6.11ms |
| update_2to1 | 4.79ms | 10.80ms | 4.48ms | 15.17ms | 7.09ms | 3.06ms |
| update_4to1 | 943μs | 7.04ms | 2.22ms | 7.64ms | 3.52ms | 1.59ms |
| update_1000to1 | 9μs | 69μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.78ms | 13.85ms | 4.41ms | 15.30ms | 6.95ms | 3.06ms |
| update_1to4 | 959μs | 6.95ms | 2.24ms | 7.67ms | 3.60ms | 1.53ms |
| update_1to1000 | 41μs | 161μs | 36μs | 64μs | 161μs | 375μs |
| cellx1000 | 5.39ms | 71.28ms | 9.37ms | 9.47ms | 9.04ms | 9.17ms |
| cellx2500 | 15.96ms | 249.03ms | 25.29ms | 25.70ms | 26.18ms | 26.81ms |
| cellx5000 | 33.93ms | 543.73ms | 65.80ms | 64.36ms | 67.55ms | 85.61ms |
| 10x5 - 2 sources - read 20.0% (simple) | 186.51ms | 1.97s | 496.52ms | 536.09ms | 328.87ms | 246.52ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.26ms | 1.48s | 286.03ms | 301.24ms | 217.21ms | 199.37ms |
| 1000x12 - 4 sources - dynamic (large) | 276.03ms | 1.81s | 4.12s | 3.74s | 436.17ms | 358.10ms |
| 1000x5 - 25 sources (wide dense) | 516.90ms | 3.48s | 3.37s | 3.41s | 810.30ms | 491.55ms |
| 5x500 - 3 sources (deep) | 151.68ms | 1.11s | 232.10ms | 238.88ms | 226.69ms | 206.51ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 244.85ms | 1.66s | 465.49ms | 484.71ms | 327.85ms | 258.29ms |

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
