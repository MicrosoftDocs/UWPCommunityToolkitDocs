---
title: Transform Extensions
author: michael-hawker
description: UWP Transform extensions methods
keywords: windows 10, uwp, windows community toolkit, uwp community toolkit, uwp toolkit, Extensions, matrix, transform, rotate, skew, scale, RotateTransform, Value, ScaleTransform, SkewTransform, TranslateTransform
dev_langs:
  - csharp
---

# Transform Extensions

The Transform Extensions ([RotateTransformExtensions](/dotnet/api/microsoft.toolkit.uwp.ui.extensions.rotatetransformextensions), [ScaleTransformExtensions](/dotnet/api/microsoft.toolkit.uwp.ui.extensions.scaletransformextensions), [SkewTransformExtensions](/dotnet/api/microsoft.toolkit.uwp.ui.extensions.skewtransformextensions), and [TranslateTransformExtensions](/dotnet/api/microsoft.toolkit.uwp.ui.extensions.translatetransformextensions)) provide the ability to retrieve the Matrix of the transform.  This is similar to the `Value` property on the [System.Windows.Media.Transform](https://msdn.microsoft.com/library/system.windows.media.transform(v=vs.110).aspx) class.

## Methods

| Methods | Return Type | Description |
| -- | -- | -- |
| GetMatrix | Matrix | Returns the matrix representation of the transform. |

## Requirements (Windows 10 Device Family)

| [Device family](https://go.microsoft.com/fwlink/p/?LinkID=526370) | Universal, 10.0.16299.0 or higher |
| --- | --- |
| Namespace | Microsoft.Toolkit.Uwp.UI |
| NuGet package | [Microsoft.Toolkit.Uwp.UI](https://www.nuget.org/packages/Microsoft.Toolkit.Uwp.UI/) |

## API Source Code

- [RotateTransformExtensions source code](https://github.com/windows-toolkit/WindowsCommunityToolkit/blob/rel/7.0.0/Microsoft.Toolkit/Extensions/Media/RotateTransformExtensions.cs)
- [ScaleTransformExtensions source code](https://github.com/windows-toolkit/WindowsCommunityToolkit/blob/rel/7.0.0/Microsoft.Toolkit/Extensions/Media/ScaleTransformExtensions.cs)
- [SkewTransformExtensions source code](https://github.com/windows-toolkit/WindowsCommunityToolkit/blob/rel/7.0.0/Microsoft.Toolkit/Extensions/Media/SkewTransformExtensions.cs)
- [TranslateTransformExtensions source code](https://github.com/windows-toolkit/WindowsCommunityToolkit/blob/rel/7.0.0/Microsoft.Toolkit/Extensions/Media/TranslateTransformExtensions.cs)

## Related Topics

- [Windows.UI.Xaml.Media.RotateTransform](/uwp/api/Windows.UI.Xaml.Media.RotateTransform)
- [Windows.UI.Xaml.Media.ScaleTransform](/uwp/api/Windows.UI.Xaml.Media.ScaleTransform)
- [Windows.UI.Xaml.Media.SkewTransform](/uwp/api/Windows.UI.Xaml.Media.SkewTransform)
- [Windows.UI.Xaml.Media.TranslateTransform](/uwp/api/Windows.UI.Xaml.Media.TranslateTransform)
- [System.Windows.Media.Transform](https://msdn.microsoft.com/library/system.windows.media.transform(v=vs.110).aspx)
