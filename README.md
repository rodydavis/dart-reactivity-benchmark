# Dart Reactivity Benchmark [![Pub Version](https://img.shields.io/pub/v/reactivity_benchmark)](https://pub.dev/packages/reactivity_benchmark)

Benchmark comparing different standalone Dart reactivity/signals frameworks.

> [!NOTE]
> This benchmark is primarily for **entertainment purposes** and should not be considered a rigorous scientific comparison. The test results may be influenced by various factors such as testing environment, hardware, and specific implementation details. Please use the results as a casual reference only and conduct your own testing in your actual use cases.

## Ranking

<!-- ranking start -->
| Rank | Framework | Success Rate | Tests | Time |
|------|-----------|--------------|-------|------|
| 🥇 | [alien_signals](https://github.com/medz/alien-signals-dart) | 100.0% | 35/35 | 3.31s |
| 🥈 | [state_beacon](https://github.com/jinyus/dart_beacon) | 100.0% | 35/35 | 4.63s |
| 🥉 | [solidart](https://github.com/nank1ro/solidart) | 100.0% | 35/35 | 5.11s |
| 4 | [signals_core](https://github.com/rodydavis/signals.dart) | 100.0% | 35/35 | 10.80s |
| 5 | [preact_signals](https://pub.dev/packages/preact_signals) | 100.0% | 35/35 | 11.30s |
| 6 | [mobx](https://github.com/mobxjs/mobx.dart) | 100.0% | 35/35 | 26.96s |

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
| avoidablePropagation | 126.57ms | 2.34s | 203.47ms | 254.93ms | 249.66ms | 170.74ms |
| broadPropagation | 246.24ms | 4.36s | 448.94ms | 461.06ms | 444.35ms | 398.33ms |
| deepPropagation | 81.38ms | 1.50s | 160.35ms | 172.16ms | 132.21ms | 156.99ms |
| diamond | 157.96ms | 2.37s | 291.88ms | 319.14ms | 307.06ms | 209.42ms |
| mux | 303.13ms | 1.86s | 368.15ms | 381.08ms | 380.39ms | 363.01ms |
| repeatedObservers | 27.05ms | 236.07ms | 32.79ms | 41.96ms | 90.69ms | 58.73ms |
| triangle | 64.70ms | 745.87ms | 99.51ms | 111.39ms | 96.84ms | 85.34ms |
| unstable | 47.92ms | 344.70ms | 55.63ms | 75.25ms | 105.20ms | 342.45ms |
| molBench | 487.28ms | 591.25ms | 494.60ms | 482.16ms | 487.60ms | 493.89ms |
| create_signals | 27.64ms | 51.34ms | 4.91ms | 26.64ms | 122.07ms | 65.13ms |
| comp_0to1 | 14.54ms | 19.22ms | 17.90ms | 19.69ms | 22.06ms | 62.52ms |
| comp_1to1 | 16.22ms | 28.89ms | 13.91ms | 8.05ms | 38.28ms | 61.53ms |
| comp_2to1 | 24.08ms | 17.52ms | 19.74ms | 16.19ms | 13.34ms | 44.02ms |
| comp_4to1 | 7.48ms | 18.69ms | 13.79ms | 4.94ms | 4.36ms | 17.37ms |
| comp_1000to1 | 4μs | 22μs | 6μs | 5μs | 17μs | 41μs |
| comp_1to2 | 12.52ms | 41.01ms | 27.58ms | 23.07ms | 28.10ms | 50.41ms |
| comp_1to4 | 17.97ms | 24.95ms | 30.05ms | 16.67ms | 24.43ms | 48.62ms |
| comp_1to8 | 5.42ms | 21.48ms | 7.71ms | 11.79ms | 23.85ms | 45.34ms |
| comp_1to1000 | 3.33ms | 15.51ms | 8.76ms | 7.76ms | 14.60ms | 40.46ms |
| update_1to1 | 4.82ms | 26.55ms | 8.93ms | 30.59ms | 13.96ms | 6.10ms |
| update_2to1 | 4.82ms | 12.90ms | 4.56ms | 15.20ms | 7.11ms | 3.05ms |
| update_4to1 | 1.53ms | 6.56ms | 2.30ms | 7.84ms | 3.52ms | 1.54ms |
| update_1000to1 | 21μs | 57μs | 22μs | 77μs | 34μs | 15μs |
| update_1to2 | 4.84ms | 12.64ms | 4.47ms | 15.40ms | 6.98ms | 3.06ms |
| update_1to4 | 927μs | 6.43ms | 2.29ms | 7.71ms | 3.61ms | 1.53ms |
| update_1to1000 | 33μs | 160μs | 65μs | 87μs | 145μs | 401μs |
| cellx1000 | 5.96ms | 70.81ms | 9.43ms | 9.46ms | 9.50ms | 11.12ms |
| cellx2500 | 21.91ms | 258.03ms | 25.11ms | 25.65ms | 33.12ms | 38.99ms |
| cellx5000 | 48.43ms | 587.46ms | 75.55ms | 61.46ms | 67.28ms | 87.69ms |
| 10x5 - 2 sources - read 20.0% (simple) | 183.63ms | 1.94s | 494.39ms | 542.06ms | 324.43ms | 241.19ms |
| 10x10 - 6 sources - dynamic - read 20.0% (dynamic) | 156.70ms | 1.45s | 268.09ms | 298.90ms | 221.00ms | 197.04ms |
| 1000x12 - 4 sources - dynamic (large) | 276.82ms | 1.82s | 4.13s | 3.33s | 455.47ms | 368.88ms |
| 1000x5 - 25 sources (wide dense) | 532.54ms | 3.40s | 3.30s | 3.31s | 818.44ms | 495.55ms |
| 5x500 - 3 sources (deep) | 156.34ms | 1.09s | 223.43ms | 238.07ms | 229.73ms | 205.56ms |
| 100x15 - 6 sources - dynamic (very dynamic) | 243.55ms | 1.69s | 453.03ms | 478.88ms | 328.46ms | 258.45ms |

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
