# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.31s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.65s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.16s |
| 4 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.39s |
| 5 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 11.44s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 27.45s |

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
| avoidablePropagation | 128.14ms | 2.39s | 213.73ms | 257.48ms | 237.56ms | 170.71ms |
| broadPropagation | 241.08ms | 4.54s | 447.74ms | 457.42ms | 440.83ms | 399.62ms |
| deepPropagation | 81.53ms | 1.50s | 164.35ms | 172.91ms | 127.30ms | 161.10ms |
| diamond | 159.83ms | 2.42s | 292.69ms | 318.93ms | 299.44ms | 214.02ms |
| mux | 306.15ms | 1.86s | 373.73ms | 389.03ms | 380.97ms | 368.09ms |
| repeatedObservers | 27.80ms | 237.07ms | 32.56ms | 41.84ms | 87.17ms | 58.89ms |
| triangle | 64.46ms | 755.01ms | 101.37ms | 110.66ms | 95.52ms | 86.77ms |
| unstable | 47.55ms | 348.47ms | 55.15ms | 74.03ms | 101.35ms | 342.28ms |
| molBench | 487.68ms | 592.45ms | 494.85ms | 484.48ms | 490.01ms | 493.00ms |
| create_signals | 32.80ms | 84.92ms | 5.59ms | 26.44ms | 117.47ms | 58.90ms |
| comp_0to1 | 12.37ms | 30.59ms | 18.10ms | 27.25ms | 42.28ms | 50.80ms |
| comp_1to1 | 22.00ms | 35.77ms | 13.26ms | 8.03ms | 38.15ms | 52.58ms |
| comp_2to1 | 18.89ms | 37.75ms | 18.36ms | 12.66ms | 25.78ms | 35.64ms |
| comp_4to1 | 2.60ms | 20.01ms | 18.95ms | 7.76ms | 10.18ms | 15.80ms |
| comp_1000to1 | 3μs | 19μs | 8μs | 5μs | 31μs | 38μs |
| comp_1to2 | 11.19ms | 38.80ms | 18.34ms | 28.06ms | 34.75ms | 43.65ms |
| comp_1to4 | 13.77ms | 20.94ms | 27.19ms | 17.66ms | 21.73ms | 43.96ms |
| comp_1to8 | 7.34ms | 24.32ms | 5.86ms | 13.23ms | 23.12ms | 41.44ms |
| comp_1to1000 | 3.76ms | 17.99ms | 3.83ms | 5.72ms | 14.57ms | 37.27ms |
| update_1to1 | 3.73ms | 26.49ms | 8.84ms | 30.72ms | 13.94ms | 6.16ms |
| update_2to1 | 4.79ms | 12.24ms | 4.51ms | 15.28ms | 7.14ms | 3.05ms |
| update_4to1 | 1.01ms | 7.34ms | 2.28ms | 7.60ms | 3.47ms | 1.57ms |
| update_1000to1 | 15μs | 70μs | 22μs | 76μs | 35μs | 15μs |
| update_1to2 | 4.71ms | 13.45ms | 4.42ms | 15.24ms | 6.90ms | 3.06ms |
| update_1to4 | 1.02ms | 6.97ms | 2.28ms | 7.65ms | 3.54ms | 1.54ms |
| update_1to1000 | 41μs | 173μs | 68μs | 66μs | 144μs | 365μs |
| cellx1000 | 5.71ms | 76.27ms | 10.39ms | 9.89ms | 10.55ms | 10.80ms |
| cellx2500 | 17.85ms | 275.30ms | 32.34ms | 30.07ms | 34.78ms | 34.36ms |
| cellx5000 | 37.93ms | 608.98ms | 96.31ms | 84.80ms | 105.99ms | 95.20ms |
| 10x5 - 2 sources - read 20.0% (simple) | 185.78ms | 1.96s | 496.04ms | 540.62ms | 330.87ms | 256.04ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.60ms | 1.48s | 296.47ms | 296.19ms | 221.03ms | 212.89ms |
| 1000x12 - 4 sources - dynamic (large) | 273.12ms | 1.80s | 4.15s | 3.66s | 453.18ms | 374.68ms |
| 1000x5 - 25 sources (wide dense) | 538.63ms | 3.41s | 3.27s | 3.56s | 820.91ms | 499.54ms |
| 5x500 - 3 sources (deep) | 157.64ms | 1.13s | 236.39ms | 239.87ms | 226.63ms | 211.94ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 250.84ms | 1.69s | 464.37ms | 494.24ms | 330.50ms | 265.03ms |

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
