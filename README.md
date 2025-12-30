# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.32s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.60s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.19s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.24s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.42s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.26s |

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
| avoidablePropagation | 125.61ms | 2.34s | 204.64ms | 252.50ms | 263.92ms | 171.42ms |
| broadPropagation | 238.73ms | 4.49s | 452.35ms | 454.27ms | 446.04ms | 395.57ms |
| deepPropagation | 81.68ms | 1.51s | 165.51ms | 172.61ms | 132.93ms | 156.96ms |
| diamond | 158.71ms | 2.35s | 290.97ms | 314.31ms | 305.42ms | 211.16ms |
| mux | 294.46ms | 1.87s | 370.35ms | 383.63ms | 393.33ms | 358.03ms |
| repeatedObservers | 26.70ms | 225.25ms | 32.05ms | 42.08ms | 87.63ms | 58.73ms |
| triangle | 66.51ms | 753.21ms | 101.55ms | 114.86ms | 101.45ms | 84.66ms |
| unstable | 45.92ms | 335.60ms | 55.07ms | 74.43ms | 102.59ms | 342.83ms |
| molBench | 486.98ms | 591.05ms | 494.74ms | 482.12ms | 488.38ms | 493.19ms |
| create_signals | 28.76ms | 74.16ms | 5.70ms | 29.07ms | 120.53ms | 67.12ms |
| comp_0to1 | 18.41ms | 27.79ms | 18.29ms | 33.48ms | 19.83ms | 54.48ms |
| comp_1to1 | 19.09ms | 38.18ms | 14.74ms | 7.69ms | 40.51ms | 61.88ms |
| comp_2to1 | 20.45ms | 24.17ms | 17.69ms | 12.40ms | 22.95ms | 39.52ms |
| comp_4to1 | 4.78ms | 18.96ms | 15.58ms | 6.54ms | 4.39ms | 16.41ms |
| comp_1000to1 | 3μs | 15μs | 4μs | 6μs | 19μs | 38μs |
| comp_1to2 | 11.52ms | 37.86ms | 16.49ms | 27.34ms | 35.09ms | 43.85ms |
| comp_1to4 | 19.08ms | 30.86ms | 24.22ms | 20.65ms | 22.07ms | 44.44ms |
| comp_1to8 | 4.62ms | 21.42ms | 7.57ms | 13.24ms | 23.70ms | 41.63ms |
| comp_1to1000 | 3.33ms | 15.70ms | 5.84ms | 3.85ms | 14.21ms | 37.41ms |
| update_1to1 | 4.86ms | 27.67ms | 8.95ms | 30.66ms | 13.93ms | 6.16ms |
| update_2to1 | 4.66ms | 13.40ms | 4.51ms | 15.29ms | 7.11ms | 3.08ms |
| update_4to1 | 1.97ms | 6.92ms | 2.27ms | 7.72ms | 3.50ms | 1.58ms |
| update_1000to1 | 18μs | 68μs | 35μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.78ms | 13.82ms | 4.41ms | 15.43ms | 6.99ms | 3.09ms |
| update_1to4 | 1.03ms | 6.96ms | 2.30ms | 7.74ms | 3.66ms | 1.55ms |
| update_1to1000 | 34μs | 164μs | 940μs | 83μs | 144μs | 364μs |
| cellx1000 | 8.19ms | 95.29ms | 10.54ms | 9.88ms | 10.69ms | 10.19ms |
| cellx2500 | 21.40ms | 274.89ms | 32.14ms | 29.37ms | 34.92ms | 34.50ms |
| cellx5000 | 51.20ms | 641.90ms | 103.27ms | 89.14ms | 121.52ms | 103.23ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.53ms | 1.96s | 489.85ms | 537.73ms | 322.98ms | 241.32ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 159.33ms | 1.44s | 279.74ms | 298.33ms | 218.62ms | 197.65ms |
| 1000x12 - 4 sources - dynamic (large) | 285.36ms | 1.79s | 4.19s | 3.61s | 450.10ms | 370.96ms |
| 1000x5 - 25 sources (wide dense) | 537.40ms | 3.47s | 3.29s | 3.41s | 818.32ms | 479.21ms |
| 5x500 - 3 sources (deep) | 157.35ms | 1.10s | 232.14ms | 234.27ms | 226.24ms | 206.30ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.79ms | 1.66s | 471.51ms | 493.07ms | 328.55ms | 260.40ms |

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
