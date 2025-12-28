# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.19s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.63s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.18s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.27s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.61s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.22s |

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
| avoidablePropagation | 126.34ms | 2.36s | 204.02ms | 261.84ms | 249.49ms | 171.94ms |
| broadPropagation | 237.01ms | 4.38s | 453.96ms | 461.17ms | 455.39ms | 417.83ms |
| deepPropagation | 81.40ms | 1.48s | 163.05ms | 173.99ms | 131.54ms | 154.90ms |
| diamond | 156.31ms | 2.38s | 287.64ms | 325.75ms | 302.48ms | 220.84ms |
| mux | 298.98ms | 1.83s | 373.83ms | 385.61ms | 376.87ms | 358.04ms |
| repeatedObservers | 26.94ms | 229.41ms | 32.57ms | 41.85ms | 87.50ms | 58.83ms |
| triangle | 65.63ms | 748.80ms | 104.14ms | 112.20ms | 94.39ms | 87.78ms |
| unstable | 45.60ms | 346.31ms | 54.76ms | 79.46ms | 101.75ms | 344.15ms |
| molBench | 416.96ms | 588.86ms | 495.45ms | 491.14ms | 491.65ms | 492.41ms |
| create_signals | 28.55ms | 76.03ms | 11.06ms | 32.40ms | 122.35ms | 60.90ms |
| comp_0to1 | 12.01ms | 25.41ms | 17.45ms | 23.79ms | 47.41ms | 55.95ms |
| comp_1to1 | 19.94ms | 28.28ms | 6.91ms | 7.87ms | 25.63ms | 53.59ms |
| comp_2to1 | 17.13ms | 8.80ms | 12.11ms | 16.20ms | 19.48ms | 35.14ms |
| comp_4to1 | 1.93ms | 28.43ms | 11.44ms | 1.78ms | 16.90ms | 16.26ms |
| comp_1000to1 | 4μs | 20μs | 6μs | 5μs | 16μs | 37μs |
| comp_1to2 | 12.97ms | 42.72ms | 19.16ms | 16.91ms | 37.09ms | 43.44ms |
| comp_1to4 | 15.13ms | 24.01ms | 26.64ms | 12.28ms | 29.02ms | 43.11ms |
| comp_1to8 | 7.80ms | 22.19ms | 6.80ms | 6.16ms | 33.08ms | 41.65ms |
| comp_1to1000 | 5.59ms | 15.07ms | 4.54ms | 4.86ms | 15.45ms | 37.36ms |
| update_1to1 | 5.00ms | 23.23ms | 8.85ms | 30.61ms | 14.04ms | 6.10ms |
| update_2to1 | 4.52ms | 13.10ms | 4.49ms | 16.15ms | 6.98ms | 3.05ms |
| update_4to1 | 1.33ms | 7.35ms | 2.24ms | 7.63ms | 3.60ms | 1.53ms |
| update_1000to1 | 9μs | 71μs | 22μs | 76μs | 34μs | 15μs |
| update_1to2 | 4.73ms | 10.52ms | 4.42ms | 15.27ms | 7.60ms | 3.05ms |
| update_1to4 | 2.36ms | 6.85ms | 2.27ms | 7.66ms | 3.65ms | 1.50ms |
| update_1to1000 | 41μs | 162μs | 155μs | 63μs | 145μs | 365μs |
| cellx1000 | 5.54ms | 84.34ms | 9.83ms | 9.72ms | 10.67ms | 9.27ms |
| cellx2500 | 15.24ms | 284.34ms | 30.34ms | 30.73ms | 35.22ms | 29.39ms |
| cellx5000 | 32.89ms | 603.70ms | 97.16ms | 84.46ms | 108.19ms | 95.71ms |
| 10x5 - 2 sources - read 20.0% (simple) | 184.42ms | 1.95s | 489.44ms | 533.14ms | 321.34ms | 251.48ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.30ms | 1.45s | 285.00ms | 297.08ms | 218.85ms | 202.02ms |
| 1000x12 - 4 sources - dynamic (large) | 265.68ms | 1.87s | 4.28s | 3.64s | 444.95ms | 357.04ms |
| 1000x5 - 25 sources (wide dense) | 535.87ms | 3.52s | 3.40s | 3.42s | 815.98ms | 498.18ms |
| 5x500 - 3 sources (deep) | 156.90ms | 1.10s | 232.24ms | 233.33ms | 228.78ms | 212.37ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 241.96ms | 1.68s | 471.16ms | 487.57ms | 327.02ms | 262.41ms |

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
