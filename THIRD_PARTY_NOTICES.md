# Third-party notices

## Retained source notices

Some source portions are Copyright (c) 2026 Bhavit Naowapradit and are used under the MIT License. Their full copyright and permission notice is preserved in [licenses/retained-source-MIT.txt](licenses/retained-source-MIT.txt). This includes retained or adapted Windows integration, screen capture, hotkey, OCR language management and language installation UI code; the notice also applies to other retained portions.

ZM GameChat Translator is maintained and distributed from its own repository. Separate maintenance does not remove the copyright and permission notices applicable to incorporated source code.

## .NET dependencies

- .NET runtime and WPF — Microsoft / .NET Foundation, MIT; runtime distribution includes its applicable notices.
- CommunityToolkit.Mvvm — .NET Foundation and contributors, MIT.
- Microsoft.Extensions.DependencyInjection and System.IO.Hashing — .NET Foundation and contributors, MIT.
- Windows SDK / C#/WinRT references — Microsoft, applicable package licenses.
- RapidOcrNet 4.2.0 — BobLd / RapidOCR contributors, Apache-2.0. See `licenses/RapidOcrNet-NOTICE.txt` and `licenses/Apache-2.0.txt`.
- ONNX Runtime 1.29.0 — Microsoft contributors, MIT, with its bundled third-party notices.
- SkiaSharp 3.119.1 and native assets — Microsoft / Mono contributors, MIT, with the native asset package's third-party notices.
- Clipper2 2.0.0 — Angus Johnson, Boost Software License 1.0.
- Test-only: xUnit.net (Apache-2.0), Microsoft.NET.Test.Sdk (MIT), xunit.runner.visualstudio (Apache-2.0). A copy of Apache-2.0 is provided in `licenses/Apache-2.0.txt`.

The publish output includes the resolved runtime and package license/notice files in `licenses/<package>-<version>/`. The Windows SDK targeting package supplies a license URL and package metadata; these are included in its notice directory. When ZIP packaging is resumed, `release-manifest.json` also lists the dependencies redistributed by that build. Test tooling is not shipped; the Apache-2.0 license copy is included for OCR dependencies and models.

Resolved versions and license metadata are also available in the NuGet package cache and `obj/project.assets.json` after restore.

## Bundled OCR models and character dictionaries

PP-OCRv6 small detection/recognition and Korean PP-OCRv5 mobile recognition are provided by PaddleOCR, converted to ONNX and distributed by RapidAI / RapidOCR under Apache-2.0. See `licenses/OCR-MODELS-NOTICE.txt`. Character dictionaries are extracted from the matching models' metadata with LF newline normalization. Source URLs and checksums are in `models/ocr/models.json` in the published app (`assets/ocr/models.json` in the source tree).

`scripts/publish.ps1` copies the models and resolved dependency notices alongside the executable. These files are required parts of the local publish output; the user does not install Windows OCR language packs for the default engine.
