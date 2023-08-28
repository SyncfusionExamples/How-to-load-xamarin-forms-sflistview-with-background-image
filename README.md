# How to load Xamarin.Forms SfListView with background image?

This example demonstrates how to load an background image for listview in Xamarin.Forms.

## Xaml

 ```
<ContentPage xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms" >
    <ContentPage.Content>
        <Grid>
          <Image Source="{Binding BackgroundImage}" Aspect="AspectFill"/>
         <syncfusion:SfListView x:Name="listView" ItemsSource="{Binding contactsinfo}">
               <syncfusion:SfListView.GroupHeaderTemplate>
                      <DataTemplate>
                           <ViewCell>
                                    <Label Text="{Binding Key}" TextColor="White"/>
                           </ViewCell>
                     </DataTemplate>
                </syncfusion:SfListView.GroupHeaderTemplate>
                <syncfusion:SfListView.ItemTemplate>
                    <DataTemplate>
                        <ViewCell>
                            <ViewCell.View>
                               <Grid>   
                                     <Label Text="{Binding ContactName}"/>
                                     <Label Text="{Binding ContactNumber}">
                              </Grid>
                            </ViewCell.View>
                        </ViewCell>
                    </DataTemplate>
                </syncfusion:SfListView.ItemTemplate>                
            </syncfusion:SfListView>
        </Grid>
    </ContentPage.Content>
</ContentPage>
```
 
## Requirements to run the demo

* [Visual Studio 2017](https://visualstudio.microsoft.com/downloads/) or [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/)
* Xamarin add-ons for Visual Studio (available via the Visual Studio installer).

## Troubleshooting

### Path too long exception

If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.
