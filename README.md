# Stokkur Analysis

[![Stokkur Analysis](assets/stokkur_logo.svg)][stokkur_link]

[![ci][ci_badge]][ci_badge_link]
[![License: MIT][license_badge]][license_badge_link]
[![style: very good analysis][badge]][badge_link]

<!-- [![pub package][pub_badge]][pub_badge_link] -->
---

This package provides lint rules for Flutter which are used at [Stokkur][stokkur_link]. 

**Note**: This package was inspired by [Very Good Analysis][vgv_link] and the Flutter [recommended][flutter_lints_link] rules.

## Usage

To use the lints, add a dependency in your `pubspec.yaml`:

```yaml
dev_dependencies:
  stokkur_analysis: ^0.0.1
```

Then, add an include in `analysis_options.yaml`:

```yaml
include: package:stokkur_analysis/analysis_options.yaml
```

This will ensure you always use the latest version of the lints. If you wish to restrict the lint version, specify a version of `analysis_options.yaml` instead:

```yaml
include: package:stokkur_analysis/analysis_options.0.0.1.yaml
```

## Suppressing Lints

There may be cases where specific lint rules are undesirable. Lint rules can be surpressed at the line, file, or project level.

### Line Level

To surpress a specific lint rule for a specific line of code, use an `ignore` comment directly above the line:

```dart
// ignore: public_member_api_docs
class A {}
```

### File Level

To surpress a specific lint rule of a specific file, use an `ignore_for_file` comment at the top of the file:

```dart
// ignore_for_file: public_member_api_docs

class A {}

class B {}
```

### Project Level

To surpress a specific lint rule for an entire project, modify `analysis_options.yaml`:

```yaml
include: package:stokkur_analysis/analysis_options.yaml
linter:
  rules:
    public_member_api_docs: false
```

## Badge

You're using `stokkur_analysis` in your project? Add the badge to your README.md 

[![style: stokkur analysis][badge]][badge_link]

```md
[![style: stokkur analysis](https://img.shields.io/badge/style-stokkur_analysis-green?logo=Flutter&logoColor=blue)](https://github.com/jorgesarabia/stokkur_analysis)
```

[badge]: https://img.shields.io/badge/style-stokkur_analysis-green?logo=Flutter&logoColor=blue
[badge_link]: https://github.com/jorgesarabia/stokkur_analysis
[license_badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license_badge_link]: https://opensource.org/licenses/MIT
<!-- [pub_badge]: https://img.shields.io/pub/v/stokkur_analysis.svg -->
<!-- [pub_badge_link]: https://pub.dartlang.org/packages/stokkur_analysis -->
[ci_badge]: https://github.com/jorgesarabia/stokkur_analysis/workflows/ci/badge.svg
[ci_badge_link]: https://github.com/jorgesarabia/stokkur_analysis/actions
[stokkur_link]: https://designsprint.stokkur.is
[vgv_link]: https://pub.dev/packages/very_good_analysis
[flutter_lints_link]: https://pub.dev/packages/flutter_lints