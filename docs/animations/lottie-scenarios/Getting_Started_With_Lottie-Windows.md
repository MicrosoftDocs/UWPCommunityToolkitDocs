# Getting Started with Lottie-Windows

You probably have a JSON file that was exported from [Adobe AfterEffects](https://www.adobe.com/products/aftereffects.html) using the [BodyMovin](https://aescripts.com/bodymovin/) plugin. If not, you can find many from the [fantastic community](https://lottiefiles.com/) of Lottie designers and creators. Let’s bring these animations to your Windows app using Lottie-Windows.

In these steps below, we use `LottieLogo1.json` as an example:

1. _(Optional but Recommended)_ Install the [LottieViewer app](https://www.microsoft.com/p/lottie-viewer/9p7x9k692tmw) from the Store and validate that the JSON file works as expected. If there are any known issues due to unsupported AfterEffects features, the warning icon may light up and provide more context.  

2. Install the [`Microsoft.UI.Xaml` nuget package](https://www.nuget.org/packages/Microsoft.UI.Xaml/) which contains the [`AnimatedVisualPlayer`](https://docs.microsoft.com/en-us/uwp/api/microsoft.ui.xaml.controls.animatedvisualplayer) element. In your VisualStudio project:
    * Go to the Nuget Package Manager by navigating Project > Manage Nuget Packages.
    * Check the _Include prerelease_ box and search for “Microsoft.UI.Xaml” in nuget.org.
    * Install the latest prerelease version of the nuget package available.

    Modify your `Page.xaml` to include the `Microsoft.UI.Xaml.Controls` namespace:

```xaml
xmlns:controls="using:Microsoft.UI.Xaml.Controls"
```

3. Install the latest [`Microsoft.Toolkit.Uwp.UI.Lottie` nuget package](https://www.nuget.org/packages/Microsoft.Toolkit.Uwp.UI.Lottie/) by following steps similar to those listed above. Modify your `Page.xaml` to include the namespace:

```xaml
xmlns:lottie="using:Microsoft.Toolkit.Uwp.UI.Lottie"
```

4. Add the JSON file to your project: create a new  `/AnimatedVisuals` folder and include `LottieLogo1.json` in the Project Solution by right clicking > Add > Existing Item. Set its [Build Action](https://docs.microsoft.com/visualstudio/ide/build-actions) to **Content** in the Properties window.

![Build Action image](../resources/images/Animations/Lottie/LottieDocs_BuildAction.png)

5. Instantiate the `AnimatedVisualPlayer` element and configure its `Source` as follows:

```xaml
    <Border Style="{StaticResource LottiePlayer}">
        <!--AnimatedVisualPlayer with AutoPlay-->
        <winui:AnimatedVisualPlayer x:Name="LottiePlayer">
            <!--LottieVisualSource with JSON UriSource-->
            <lottie:LottieVisualSource x:Name="LottieJsonSource" UriSource="ms-appx:///AnimatedVisuals/LottieLogo1.json"/>
        </winui:AnimatedVisualPlayer>
    </Border>
```

Since the `AutoPlay` property is set to `True` by default, the result will be a looping animation:

![Json Gif](../resources/images/Animations/Lottie/LottieDocs_Autoplay.gif)

## Resources

* [Source code](https://github.com/windows-toolkit/Lottie-Windows/blob/master/samples/LottieSamples/Scenarios/JsonPage.xaml) for getting started with a JSON file
* The resulting page in the [Lottie Samples application](aka.ms/lottiesamples)
* [LottieVisualSource](https://docs.microsoft.com/dotnet/api/microsoft.toolkit.uwp.ui.lottie.lottievisualsource) API reference
* [Lottie Viewer application](https://www.microsoft.com/p/lottie-viewer/9p7x9k692tmw) for previewing JSON files
* [Help + feedback](https://github.com/windows-toolkit/Lottie-Windows/issues)