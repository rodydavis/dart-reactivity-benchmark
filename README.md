# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.31s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.72s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.14s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.28s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.49s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.11s |

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
| avoidablePropagation | 126.71ms | 2.35s | 202.64ms | 251.25ms | 238.01ms | 171.38ms |
| broadPropagation | 234.54ms | 4.45s | 451.47ms | 459.62ms | 446.45ms | 404.86ms |
| deepPropagation | 81.36ms | 1.49s | 164.51ms | 174.33ms | 131.16ms | 160.54ms |
| diamond | 157.82ms | 2.39s | 288.89ms | 313.73ms | 310.83ms | 224.87ms |
| mux | 301.91ms | 1.85s | 368.90ms | 384.03ms | 374.46ms | 369.68ms |
| repeatedObservers | 26.68ms | 229.41ms | 31.90ms | 40.87ms | 88.82ms | 58.51ms |
| triangle | 65.23ms | 745.99ms | 106.49ms | 109.82ms | 94.83ms | 92.72ms |
| unstable | 46.45ms | 345.26ms | 55.31ms | 73.58ms | 101.19ms | 344.32ms |
| molBench | 486.69ms | 590.11ms | 495.83ms | 484.13ms | 490.79ms | 493.73ms |
| create_signals | 28.97ms | 73.34ms | 5.59ms | 23.53ms | 75.83ms | 59.96ms |
| comp_0to1 | 10.62ms | 25.15ms | 18.73ms | 30.08ms | 41.16ms | 51.07ms |
| comp_1to1 | 17.38ms | 27.89ms | 13.26ms | 10.51ms | 42.73ms | 53.55ms |
| comp_2to1 | 20.48ms | 11.88ms | 21.07ms | 18.21ms | 25.69ms | 40.63ms |
| comp_4to1 | 3.52ms | 33.00ms | 11.64ms | 1.85ms | 4.41ms | 16.11ms |
| comp_1000to1 | 5μs | 15μs | 9μs | 5μs | 18μs | 38μs |
| comp_1to2 | 14.45ms | 37.37ms | 18.85ms | 22.88ms | 31.02ms | 44.34ms |
| comp_1to4 | 18.55ms | 23.56ms | 30.81ms | 16.43ms | 25.67ms | 43.39ms |
| comp_1to8 | 5.43ms | 25.53ms | 6.55ms | 11.98ms | 25.50ms | 41.60ms |
| comp_1to1000 | 3.17ms | 15.39ms | 5.34ms | 3.87ms | 13.99ms | 37.38ms |
| update_1to1 | 4.67ms | 26.41ms | 8.98ms | 30.71ms | 13.94ms | 6.11ms |
| update_2to1 | 5.01ms | 13.02ms | 4.50ms | 15.24ms | 7.12ms | 3.09ms |
| update_4to1 | 1.83ms | 6.58ms | 2.26ms | 7.67ms | 3.56ms | 1.58ms |
| update_1000to1 | 9μs | 68μs | 22μs | 75μs | 34μs | 15μs |
| update_1to2 | 4.78ms | 13.51ms | 4.42ms | 15.27ms | 6.98ms | 3.10ms |
| update_1to4 | 3.13ms | 6.70ms | 2.26ms | 7.63ms | 3.60ms | 1.55ms |
| update_1to1000 | 40μs | 162μs | 924μs | 65μs | 157μs | 362μs |
| cellx1000 | 5.84ms | 82.12ms | 9.86ms | 9.94ms | 11.05ms | 12.46ms |
| cellx2500 | 17.57ms | 278.56ms | 34.32ms | 30.12ms | 33.65ms | 33.88ms |
| cellx5000 | 43.37ms | 588.60ms | 82.48ms | 91.43ms | 129.95ms | 108.06ms |
| 10x5 - 2 sources - read 20.0% (simple) | 181.08ms | 1.93s | 494.55ms | 535.39ms | 323.39ms | 249.09ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.40ms | 1.47s | 285.49ms | 299.35ms | 220.15ms | 215.39ms |
| 1000x12 - 4 sources - dynamic (large) | 290.13ms | 1.85s | 4.27s | 3.72s | 454.64ms | 379.37ms |
| 1000x5 - 25 sources (wide dense) | 540.00ms | 3.41s | 3.29s | 3.37s | 815.09ms | 520.45ms |
| 5x500 - 3 sources (deep) | 155.91ms | 1.10s | 230.05ms | 237.78ms | 228.03ms | 211.02ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 247.05ms | 1.63s | 467.77ms | 482.07ms | 327.29ms | 263.28ms |

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
