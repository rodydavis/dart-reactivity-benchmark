# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.30s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.77s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.19s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.31s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 12.02s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.58s |

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
| avoidablePropagation | 126.60ms | 2.39s | 209.36ms | 256.97ms | 238.21ms | 176.27ms |
| broadPropagation | 234.60ms | 4.45s | 455.88ms | 458.08ms | 449.55ms | 415.82ms |
| deepPropagation | 81.17ms | 1.52s | 162.04ms | 174.97ms | 129.89ms | 157.30ms |
| diamond | 158.08ms | 2.40s | 296.04ms | 322.64ms | 302.48ms | 236.37ms |
| mux | 293.21ms | 1.84s | 373.46ms | 376.69ms | 386.50ms | 358.90ms |
| repeatedObservers | 27.31ms | 231.21ms | 32.95ms | 43.26ms | 87.13ms | 59.08ms |
| triangle | 64.82ms | 757.24ms | 102.85ms | 111.83ms | 94.43ms | 86.87ms |
| unstable | 46.04ms | 345.98ms | 57.41ms | 76.40ms | 100.75ms | 342.50ms |
| molBench | 487.06ms | 591.24ms | 495.37ms | 484.15ms | 490.96ms | 493.83ms |
| create_signals | 25.75ms | 56.17ms | 10.71ms | 25.00ms | 75.33ms | 58.57ms |
| comp_0to1 | 19.02ms | 15.91ms | 34.41ms | 30.06ms | 41.16ms | 52.46ms |
| comp_1to1 | 18.61ms | 39.35ms | 11.41ms | 7.75ms | 41.98ms | 54.13ms |
| comp_2to1 | 23.03ms | 24.70ms | 9.32ms | 19.60ms | 13.45ms | 36.52ms |
| comp_4to1 | 2.96ms | 26.78ms | 8.71ms | 2.00ms | 4.36ms | 17.08ms |
| comp_1000to1 | 4μs | 15μs | 6μs | 7μs | 19μs | 40μs |
| comp_1to2 | 9.98ms | 40.78ms | 33.63ms | 23.58ms | 34.27ms | 44.49ms |
| comp_1to4 | 14.91ms | 19.98ms | 28.08ms | 23.30ms | 21.47ms | 44.99ms |
| comp_1to8 | 6.01ms | 25.41ms | 7.13ms | 8.92ms | 23.86ms | 42.42ms |
| comp_1to1000 | 3.20ms | 15.86ms | 4.96ms | 4.36ms | 14.32ms | 37.97ms |
| update_1to1 | 4.26ms | 25.52ms | 8.92ms | 30.57ms | 13.93ms | 6.09ms |
| update_2to1 | 4.73ms | 13.63ms | 4.54ms | 15.18ms | 7.14ms | 3.04ms |
| update_4to1 | 1.04ms | 6.84ms | 2.23ms | 7.61ms | 3.48ms | 1.57ms |
| update_1000to1 | 9μs | 67μs | 22μs | 75μs | 35μs | 15μs |
| update_1to2 | 4.71ms | 12.64ms | 4.47ms | 15.25ms | 7.10ms | 3.06ms |
| update_1to4 | 1.03ms | 6.75ms | 2.29ms | 7.65ms | 3.58ms | 1.58ms |
| update_1to1000 | 42μs | 160μs | 155μs | 66μs | 145μs | 382μs |
| cellx1000 | 7.92ms | 90.98ms | 10.98ms | 11.13ms | 11.19ms | 11.57ms |
| cellx2500 | 21.29ms | 287.12ms | 34.23ms | 36.81ms | 40.06ms | 44.92ms |
| cellx5000 | 47.94ms | 660.93ms | 97.16ms | 109.36ms | 145.14ms | 145.03ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.25ms | 1.96s | 492.89ms | 541.83ms | 320.75ms | 262.53ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.50ms | 1.46s | 286.87ms | 299.39ms | 220.46ms | 202.31ms |
| 1000x12 - 4 sources - dynamic (large) | 281.45ms | 1.90s | 4.49s | 3.61s | 474.38ms | 386.40ms |
| 1000x5 - 25 sources (wide dense) | 538.94ms | 3.53s | 3.55s | 3.44s | 833.71ms | 500.37ms |
| 5x500 - 3 sources (deep) | 156.74ms | 1.14s | 233.54ms | 238.72ms | 228.78ms | 212.73ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.57ms | 1.70s | 471.13ms | 500.92ms | 334.63ms | 267.97ms |

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
