# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.30s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.62s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.43s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.41s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.77s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.43s |

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
| avoidablePropagation | 125.00ms | 2.44s | 211.65ms | 257.78ms | 282.14ms | 172.31ms |
| broadPropagation | 237.34ms | 4.44s | 451.06ms | 459.72ms | 441.03ms | 399.71ms |
| deepPropagation | 81.20ms | 1.53s | 166.27ms | 171.24ms | 132.85ms | 157.32ms |
| diamond | 159.30ms | 2.41s | 296.89ms | 321.04ms | 327.44ms | 213.69ms |
| mux | 294.14ms | 1.85s | 378.61ms | 378.23ms | 396.86ms | 357.39ms |
| repeatedObservers | 27.06ms | 236.36ms | 32.24ms | 42.55ms | 90.53ms | 59.12ms |
| triangle | 64.78ms | 792.81ms | 105.25ms | 110.78ms | 100.16ms | 86.28ms |
| unstable | 45.67ms | 346.33ms | 56.30ms | 75.29ms | 104.61ms | 343.04ms |
| molBench | 485.97ms | 593.01ms | 495.19ms | 486.50ms | 491.04ms | 493.22ms |
| create_signals | 30.89ms | 50.92ms | 18.93ms | 30.42ms | 126.37ms | 60.58ms |
| comp_0to1 | 12.28ms | 19.17ms | 15.40ms | 21.25ms | 37.25ms | 52.01ms |
| comp_1to1 | 20.90ms | 37.65ms | 6.83ms | 7.89ms | 42.69ms | 53.73ms |
| comp_2to1 | 16.99ms | 9.05ms | 10.44ms | 16.15ms | 13.36ms | 35.85ms |
| comp_4to1 | 2.18ms | 28.26ms | 13.71ms | 4.93ms | 4.42ms | 16.38ms |
| comp_1000to1 | 5μs | 19μs | 6μs | 4μs | 18μs | 40μs |
| comp_1to2 | 11.88ms | 31.16ms | 30.09ms | 23.26ms | 29.11ms | 44.05ms |
| comp_1to4 | 18.24ms | 30.11ms | 21.73ms | 16.72ms | 26.33ms | 44.30ms |
| comp_1to8 | 10.35ms | 26.21ms | 9.29ms | 12.06ms | 26.79ms | 41.94ms |
| comp_1to1000 | 3.11ms | 15.57ms | 6.51ms | 7.31ms | 14.59ms | 37.69ms |
| update_1to1 | 3.88ms | 24.13ms | 9.03ms | 31.11ms | 13.96ms | 6.10ms |
| update_2to1 | 4.78ms | 13.78ms | 4.61ms | 15.36ms | 7.17ms | 3.08ms |
| update_4to1 | 955μs | 6.63ms | 2.28ms | 7.71ms | 3.53ms | 1.59ms |
| update_1000to1 | 9μs | 65μs | 22μs | 78μs | 35μs | 15μs |
| update_1to2 | 4.85ms | 13.54ms | 4.43ms | 15.50ms | 6.98ms | 3.10ms |
| update_1to4 | 1.54ms | 6.91ms | 2.29ms | 7.75ms | 3.60ms | 1.55ms |
| update_1to1000 | 43μs | 160μs | 2.53ms | 70μs | 159μs | 363μs |
| cellx1000 | 6.13ms | 74.41ms | 9.59ms | 10.18ms | 11.72ms | 10.34ms |
| cellx2500 | 16.00ms | 245.98ms | 29.39ms | 32.48ms | 49.27ms | 36.51ms |
| cellx5000 | 39.25ms | 566.44ms | 81.68ms | 94.32ms | 158.18ms | 120.85ms |
| 10x5 - 2 sources - read 20.0% (simple) | 182.68ms | 1.93s | 491.77ms | 539.16ms | 324.62ms | 239.38ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.59ms | 1.49s | 279.69ms | 303.97ms | 221.07ms | 196.89ms |
| 1000x12 - 4 sources - dynamic (large) | 289.27ms | 1.87s | 4.31s | 3.73s | 470.78ms | 370.82ms |
| 1000x5 - 25 sources (wide dense) | 540.78ms | 3.53s | 3.52s | 3.45s | 896.42ms | 493.16ms |
| 5x500 - 3 sources (deep) | 156.76ms | 1.11s | 231.19ms | 241.60ms | 232.66ms | 205.96ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 252.01ms | 1.67s | 462.56ms | 491.62ms | 342.57ms | 260.44ms |

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
