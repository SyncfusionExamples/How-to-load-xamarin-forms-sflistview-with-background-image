# How to load Xamarin.Forms SfListView with background image?

This example demonstrates how to load an background image for listview in Xamarin.Forms.

## Sample

```xaml
        <Grid>
            <Image Source="{Binding BackgroundImage}" Aspect="AspectFill"/>
            <syncfusion:SfListView x:Name="listView" SelectionMode="None" Margin="5"
                                   ItemSize="70"
                                   ItemsSource="{Binding contactsinfo}">
                <syncfusion:SfListView.GroupHeaderTemplate>
                    <DataTemplate>
                        <ViewCell>
                            <Label Text="{Binding Key}" TextColor="White" FontAttributes="Bold" FontSize="24"/>
                        </ViewCell>
                    </DataTemplate>
                </syncfusion:SfListView.GroupHeaderTemplate>
                
                <syncfusion:SfListView.ItemTemplate>
                    <DataTemplate>
                        <ViewCell>
                            <ViewCell.View>
                                <Grid x:Name="grid" RowSpacing="0">

                                    <Grid.RowDefinitions>
                                        <RowDefinition Height="*" />
                                        <RowDefinition Height="1" />
                                    </Grid.RowDefinitions>
                                    <Grid RowSpacing="0">
                                        <Grid.ColumnDefinitions>
                                            <ColumnDefinition Width="Auto" />
                                        </Grid.ColumnDefinitions>

                                        <Grid Grid.Column="1"
                          RowSpacing="1"
                          Padding="10,0,0,0"
                          VerticalOptions="Center">
                                            <Grid.RowDefinitions>
                                                <RowDefinition Height="*" />
                                                <RowDefinition Height="*" />
                                            </Grid.RowDefinitions>

                                            <Label  Text="{Binding ContactName}" TextColor="White" FontSize="18"/>
                                            <Label Grid.Row="1" Grid.Column="0" TextColor="White" FontSize="18"
                                                  Text="{Binding ContactNumber}">

                                            </Label>
                                        </Grid>
                                    </Grid>
                                </Grid>
                            </ViewCell.View>
                        </ViewCell>
                    </DataTemplate>
                </syncfusion:SfListView.ItemTemplate>
                
            </syncfusion:SfListView>
        </Grid>
```

See [How to load Xamarin.Forms SfListView with background image?](https://www.syncfusion.com/kb/9479/how-to-load-listview-with-background-image) for more details.

```
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns:local="clr-namespace:SfListViewSample"
             xmlns:syncfusion="clr-namespace:Syncfusion.ListView.XForms;assembly=Syncfusion.SfListView.XForms"
             x:Class="SfListViewSample.MainPage">
    <ContentPage.BindingContext>
        <local:ContactsViewModel x:Name="viewModel"/>
    </ContentPage.BindingContext>

    <ContentPage.Content>
            <Grid>
            <Image Source="{Binding BackgroundImage}" Aspect="AspectFill"/>
            <syncfusion:SfListView x:Name="listView" SelectionMode="None" Margin="5"
                                   ItemSize="70"
                                   ItemsSource="{Binding contactsinfo}">
                
                <syncfusion:SfListView.ItemTemplate>
                    <DataTemplate>
                      -----
                      -----
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
