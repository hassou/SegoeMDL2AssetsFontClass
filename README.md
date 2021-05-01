# SegoeMDL2AssetsFontClass
Unofficial Segoe MDL2 Assets Font Class C#

![image](https://user-images.githubusercontent.com/20809230/116704894-d740d800-a9c3-11eb-9416-798a9d7d0e23.png)

Easily use Segoe MDL2 Assets in your C# project (Xamarin, UWP, WPF)
## Xamarin.Forms demo
In your shared project, add Segoe MDL2 Assets font, that you can grab from Windows Fonts, and **one** of the FontClass files from the repo, to your project like this:

![image](https://user-images.githubusercontent.com/20809230/116705403-66e68680-a9c4-11eb-9b5b-c206c6319d67.png)

Make sure that the Build Action of the font file (SEGMDL2.ttf) is set to Embedded resource.
Add the namespace of your project to FontClass cs file

![image](https://user-images.githubusercontent.com/20809230/116710284-7916f380-a9c9-11eb-991a-3fdff319084c.png)


Add this line anywhere in your project (preferably in the assemblyInfo.cs file)
```C#
[assembly: ExportFont("SEGMDL2.TTF", Alias = "IconFont")]
```
You can then use the font in your XAML or C# project
```C#
Label label = new Label{
  FontFamily = "IconFont",
  Text = IconFont.Edit
}
```


If you want to use it with XAML, add your project namspace:

```XAML
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:mdl="clr-namespace:CardsGame"
             x:Class="CardsGame.DemoPage">
  <Label FontFamily="IconFont" Text="{x:Static mdl:IconFont.Edit}"/>
</ContentPage>
```
