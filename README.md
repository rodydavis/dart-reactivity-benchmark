# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.29s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.62s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.05s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.35s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.39s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.83s |

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
| avoidablePropagation | 125.24ms | 2.35s | 197.93ms | 286.83ms | 246.59ms | 166.94ms |
| broadPropagation | 239.68ms | 4.32s | 452.44ms | 461.13ms | 444.33ms | 399.86ms |
| deepPropagation | 82.17ms | 1.48s | 169.69ms | 170.69ms | 131.88ms | 155.38ms |
| diamond | 157.15ms | 2.36s | 290.60ms | 312.70ms | 305.17ms | 219.16ms |
| mux | 296.10ms | 1.83s | 374.95ms | 378.80ms | 384.88ms | 365.12ms |
| repeatedObservers | 27.00ms | 225.59ms | 31.71ms | 41.94ms | 87.50ms | 58.46ms |
| triangle | 65.88ms | 737.53ms | 102.28ms | 111.56ms | 114.19ms | 91.79ms |
| unstable | 45.98ms | 337.35ms | 54.92ms | 74.02ms | 107.27ms | 342.92ms |
| molBench | 487.78ms | 589.16ms | 495.94ms | 484.71ms | 491.67ms | 493.94ms |
| create_signals | 31.98ms | 69.73ms | 4.92ms | 27.17ms | 67.69ms | 59.50ms |
| comp_0to1 | 22.91ms | 31.93ms | 18.08ms | 28.06ms | 18.23ms | 53.08ms |
| comp_1to1 | 12.78ms | 39.64ms | 12.74ms | 14.21ms | 28.87ms | 55.48ms |
| comp_2to1 | 23.41ms | 23.68ms | 17.08ms | 15.00ms | 13.42ms | 37.60ms |
| comp_4to1 | 3.28ms | 26.42ms | 11.23ms | 2.13ms | 4.42ms | 17.51ms |
| comp_1000to1 | 4μs | 19μs | 4μs | 6μs | 19μs | 40μs |
| comp_1to2 | 13.28ms | 34.70ms | 30.67ms | 22.79ms | 34.51ms | 46.05ms |
| comp_1to4 | 16.08ms | 17.98ms | 20.70ms | 15.44ms | 21.57ms | 45.33ms |
| comp_1to8 | 7.04ms | 21.43ms | 7.59ms | 10.72ms | 23.04ms | 45.48ms |
| comp_1to1000 | 4.76ms | 15.21ms | 4.60ms | 4.96ms | 14.08ms | 39.59ms |
| update_1to1 | 4.66ms | 27.45ms | 8.87ms | 31.71ms | 14.05ms | 7.01ms |
| update_2to1 | 5.04ms | 13.79ms | 4.50ms | 15.68ms | 7.19ms | 3.08ms |
| update_4to1 | 2.01ms | 7.36ms | 2.22ms | 7.87ms | 3.58ms | 1.55ms |
| update_1000to1 | 9μs | 68μs | 23μs | 94μs | 36μs | 15μs |
| update_1to2 | 3.38ms | 13.65ms | 4.41ms | 15.74ms | 6.99ms | 3.06ms |
| update_1to4 | 1.38ms | 6.82ms | 2.26ms | 7.89ms | 3.65ms | 1.50ms |
| update_1to1000 | 44μs | 170μs | 155μs | 86μs | 144μs | 385μs |
| cellx1000 | 5.42ms | 74.96ms | 9.95ms | 9.73ms | 9.28ms | 9.39ms |
| cellx2500 | 15.59ms | 265.65ms | 26.16ms | 27.69ms | 32.43ms | 28.41ms |
| cellx5000 | 36.54ms | 582.95ms | 81.12ms | 71.90ms | 79.08ms | 94.37ms |
| 10x5 - 2 sources - read 20.0% (simple) | 186.95ms | 1.90s | 492.84ms | 535.88ms | 327.12ms | 259.44ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 157.59ms | 1.45s | 282.14ms | 298.92ms | 220.14ms | 198.04ms |
| 1000x12 - 4 sources - dynamic (large) | 277.09ms | 1.84s | 4.13s | 3.68s | 443.88ms | 359.98ms |
| 1000x5 - 25 sources (wide dense) | 532.65ms | 3.40s | 3.30s | 3.51s | 813.46ms | 495.32ms |
| 5x500 - 3 sources (deep) | 154.44ms | 1.09s | 231.48ms | 236.47ms | 222.63ms | 207.19ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 242.86ms | 1.65s | 472.53ms | 483.19ms | 326.38ms | 256.33ms |

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
