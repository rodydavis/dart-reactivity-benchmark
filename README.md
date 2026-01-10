# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.28s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.64s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.07s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.33s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.33s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.09s |

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
| avoidablePropagation | 125.94ms | 2.39s | 205.08ms | 256.71ms | 255.25ms | 171.41ms |
| broadPropagation | 236.78ms | 4.38s | 461.95ms | 445.13ms | 445.22ms | 404.82ms |
| deepPropagation | 81.51ms | 1.50s | 163.66ms | 169.28ms | 130.02ms | 154.43ms |
| diamond | 157.39ms | 2.42s | 290.13ms | 318.21ms | 306.13ms | 213.27ms |
| mux | 298.54ms | 1.86s | 376.17ms | 386.20ms | 391.25ms | 361.22ms |
| repeatedObservers | 27.57ms | 230.57ms | 32.30ms | 42.25ms | 88.30ms | 55.62ms |
| triangle | 64.91ms | 763.34ms | 102.51ms | 109.07ms | 97.87ms | 84.81ms |
| unstable | 46.13ms | 351.35ms | 54.95ms | 75.16ms | 101.26ms | 352.66ms |
| molBench | 487.26ms | 591.67ms | 494.30ms | 485.10ms | 490.89ms | 492.99ms |
| create_signals | 27.42ms | 80.64ms | 5.57ms | 23.43ms | 113.66ms | 58.03ms |
| comp_0to1 | 10.27ms | 22.13ms | 17.71ms | 33.72ms | 27.02ms | 51.49ms |
| comp_1to1 | 18.57ms | 28.49ms | 14.40ms | 13.96ms | 33.26ms | 53.35ms |
| comp_2to1 | 19.84ms | 20.64ms | 17.16ms | 17.39ms | 12.49ms | 36.17ms |
| comp_4to1 | 2.26ms | 14.36ms | 11.65ms | 2.04ms | 15.43ms | 16.03ms |
| comp_1000to1 | 3μs | 17μs | 5μs | 4μs | 14μs | 38μs |
| comp_1to2 | 9.71ms | 34.93ms | 18.37ms | 21.91ms | 30.70ms | 43.97ms |
| comp_1to4 | 14.23ms | 24.79ms | 24.69ms | 19.19ms | 27.13ms | 43.46ms |
| comp_1to8 | 5.86ms | 24.24ms | 6.78ms | 10.98ms | 19.82ms | 41.91ms |
| comp_1to1000 | 3.17ms | 15.15ms | 4.61ms | 4.42ms | 14.67ms | 37.42ms |
| update_1to1 | 4.45ms | 22.84ms | 8.89ms | 30.57ms | 13.89ms | 6.15ms |
| update_2to1 | 4.80ms | 11.39ms | 4.51ms | 15.18ms | 6.92ms | 3.06ms |
| update_4to1 | 1.43ms | 6.89ms | 2.29ms | 7.62ms | 3.50ms | 1.59ms |
| update_1000to1 | 9μs | 69μs | 22μs | 77μs | 35μs | 15μs |
| update_1to2 | 4.84ms | 13.81ms | 4.41ms | 15.27ms | 7.05ms | 3.07ms |
| update_1to4 | 902μs | 6.94ms | 2.27ms | 7.68ms | 3.57ms | 1.53ms |
| update_1to1000 | 32μs | 161μs | 39μs | 84μs | 143μs | 364μs |
| cellx1000 | 8.08ms | 67.68ms | 9.29ms | 9.47ms | 9.78ms | 9.73ms |
| cellx2500 | 16.54ms | 257.25ms | 25.13ms | 26.16ms | 25.84ms | 33.28ms |
| cellx5000 | 37.00ms | 560.66ms | 65.70ms | 64.43ms | 60.09ms | 111.52ms |
| 10x5 - 2 sources - read 20.0% (simple) | 189.10ms | 1.92s | 493.43ms | 540.35ms | 324.19ms | 258.46ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 158.68ms | 1.47s | 281.24ms | 300.19ms | 219.23ms | 203.11ms |
| 1000x12 - 4 sources - dynamic (large) | 282.15ms | 1.84s | 4.08s | 3.60s | 441.36ms | 376.87ms |
| 1000x5 - 25 sources (wide dense) | 527.59ms | 3.42s | 3.36s | 3.55s | 802.24ms | 494.30ms |
| 5x500 - 3 sources (deep) | 156.03ms | 1.08s | 229.70ms | 235.98ms | 225.18ms | 206.10ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.68ms | 1.65s | 466.89ms | 493.55ms | 325.51ms | 258.27ms |

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
