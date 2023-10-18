# Xamarin Tabbed View (SfTabView) 

The Tabbed View control is available in Xamarin.Forms, Xamarin.Android, Xamarin.iOS and Xamarin.UWP. It helps you to create the customizable features that are used to explore and switch among the different views. 

For know more details about TabView: https://www.syncfusion.com/xamarin-ui-controls/xamarin-tabbed-view

TabView user guide documentation: https://help.syncfusion.com/xamarin/tabbed-view/getting-started

## Creating the project
Create a new BlankApp (Xamarin.Forms.Portable) application in Xamarin Studio or Visual Studio for Xamarin.Forms.

## Adding SfTabView in Xamarin.Forms
Add the required assembly references to the PCL and renderer projects as discussed in the Assembly deployment section.

Import the control namespace as shown in the following code.

**[XAML]**
```
xmlns:tabView="clr-namespace:Syncfusion.XForms.TabView;assembly=Syncfusion.SfTabView.XForms"
```
**[C#]**
```
using Syncfusion.XForms.TabView;
```
Set the control to content in ContentPage.

**[XAML]**
```
 <ContentPage.Content> 
        <tabView:SfTabView/> 
 </ContentPage.Content> 
```
**[C#]**
```
public MainPage()   
{   
    InitializeComponent();       
    tabView = new SfTabView();   
    this.Content = tabView;  
}  
```
# Font icons in the header
You can refer this link for getting the font icons. Add the font file to your application by using the following steps for each platform:

## Adding font file for iOS

*   Add the font family inside Resource folder iOS project.
*   Add the font file with the following build action: BundleResource.
*   Update the Info.plist file (fonts that are provided by application, UIAppFonts, or key).
## Adding font file for Android

Add the font file to the Assets folder in the application project, and set the following build action: AndroidAsset.

## Adding font file for UWP
Add the font family inside the application project of UWP
## Setting font file for font icons

**[XAML]**
```
    <ContentPage.Resources>
        <ResourceDictionary>
            <OnPlatform x:TypeArguments="x:String" 
                        x:Key="fonts"
                        iOS="OpenTypeFont" 
                        Android="Fonts/OpenTypeFont.ttf" />
            <OnPlatform x:TypeArguments="x:String" 
                        x:Key="fonts" 
                        iOS="Fonts/fa-regular-400" 
                        Android="Fonts/fa-regular-400.ttf" />
        </ResourceDictionary>
    </ContentPage.Resources>
    <ContentPage.Content>
        <Grid BackgroundColor="White" Padding="0,20,0,0">
            <Grid.RowDefinitions>
                <RowDefinition Height="30" />
                <RowDefinition Height="*" />
            </Grid.RowDefinitions>
            <Label Text="Welcome to the Xamarin forms" Grid.Row="0" />
            <tabview:SfTabView Margin="0,0,0,2" 
                               x:Name="SimTab" 
                               VisibleHeaderCount="4" 
                               TabHeaderPosition="Bottom" 
                               DisplayMode="ImageWithText"
                               EnableSwiping="true" 
                               Grid.Row="1" >
                <tabview:SfTabView.Items>
                    <tabview:SfTabItem Title="Chat"   
                                       TitleFontSize="14"
                                       IconFont="A"
                                       FontIconFontFamily="{StaticResource fonts}"
                                       SelectionColor="#FF00AFF0"
                                       FontIconFontColor="#FF00AFF0"
                                       TitleFontColor="#FF00AFF0">
                        <tabview:SfTabItem.Content>
                            <Label Text="Hai" />
                        </tabview:SfTabItem.Content>
                    </tabview:SfTabItem>
                    <tabview:SfTabItem Title="Chat2"   
                                       TitleFontSize="14"
                                       IconFont="&#xf000;"
                                       FontIconFontFamily="{StaticResource fonts}"
                                       SelectionColor="#FF00AFF0"
                                       FontIconFontColor="#FF00AFF0"
                                       TitleFontColor="#FF00AFF0">
                        <tabview:SfTabItem.Content>
                            <Label Text="Hai" />
                        </tabview:SfTabItem.Content>
                    </tabview:SfTabItem>
                    <tabview:SfTabItem Title="like"   
                                       TitleFontSize="14"
                                       IconFont="&#0041;"
                                       FontIconFontFamily="{StaticResource fonts}"
                                       SelectionColor="#FF00AFF0"
                                       FontIconFontColor="#FF00AFF0"
                                       TitleFontColor="#FF00AFF0">
                        <tabview:SfTabItem.Content>
                            <Label Text="Hello"/>
                        </tabview:SfTabItem.Content>
                    </tabview:SfTabItem>
                    <tabview:SfTabItem Title="dislike"   
                                       TitleFontSize="14"
                                       IconFont="&#0041;"
                                       FontIconFontFamily="Fonts/OpenTypeFont.ttf"
                                       SelectionColor="#FF00AFF0"
                                       FontIconFontColor="#FF00AFF0"
                                       TitleFontColor="#FF00AFF0">
                        <tabview:SfTabItem.Content>
                            <Label Text="How are"/>
                        </tabview:SfTabItem.Content>
                    </tabview:SfTabItem>
                    <tabview:SfTabItem Title="status"
                                       TitleFontSize="14"
                                       IconFont="C"
                                       FontIconFontFamily="{StaticResource fonts}"
                                       SelectionColor="#FF00AFF0"
                                       FontIconFontColor="#FF00AFF0"
                                       TitleFontColor="#FF00AFF0">
                        <tabview:SfTabItem.Content>
                            <Label Text="You"/>
                        </tabview:SfTabItem.Content>
                    </tabview:SfTabItem>
                </tabview:SfTabView.Items>
            </tabview:SfTabView>
        </Grid>
    </ContentPage.Content>
</ContentPage>
```

## How to run this application?

To run this application, you need to first clone the tabview-font-sample repository and then open it in Visual Studio 2022. Now, simply build and run your project to view the output.

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion has no liability for any damage or consequence that may arise by using or viewing the samples. The samples are for demonstrative purposes, and if you choose to use or access the samples, you agree to not hold Syncfusion liable, in any form, for any damage that is related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion’s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion’s samples.
