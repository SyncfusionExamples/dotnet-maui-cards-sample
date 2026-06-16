# Getting started with .NET MAUI Card
This section details the process of integrating the [.NET MAUI Cards](https://www.syncfusion.com/maui-controls/maui-cards) control and focuses solely on the fundamental features required for initiating your exploration of Syncfusion<sup>&reg;</sup> Card.

## Register Syncfusion handler

Make sure to add the namespace.

{% highlight MauiProgram.cs %}
using Syncfusion.Maui.Core.Hosting;
{% endhighlight %} 

Register the Syncfusion core handler in your `CreateMauiApp` method of `MauiProgram.cs` file to use Syncfusion controls.

{% highlight MauiProgram.cs %}
builder.ConfigureSyncfusionCore();
{% endhighlight %} 

## Import the Card namespace

Add the following namespace in your XAML or C#.

{% tabs %}
{% highlight xaml tabtitle="xaml" %}
xmlns:cards="clr-namespace:Syncfusion.Maui.Cards;assembly=Syncfusion.Maui.Cards"
{% endhighlight %}
{% highlight c# tabtitle="C#" %}
using Syncfusion.Maui.Cards;
{% endhighlight %}
{% endtabs %}

## Add the Card component

Create an instance for the Card control, and add it as content.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}
<cards:SfCardView>
    <Label Text="CardView" 
           Background="PeachPuff" 
           HorizontalTextAlignment="Center" 
           VerticalTextAlignment="Center"/>
</cards:SfCardView>
{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}
    SfCardView cardView = new SfCardView();
    cardView.Content = new Label()
    {
        Text = "CardView",
        HorizontalTextAlignment = TextAlignment.Center,
        VerticalTextAlignment = TextAlignment.Center,
        BackgroundColor = Colors.PeachPuff
    };
    this.Content = cardView;
{% endhighlight %}
{% endtabs %}

The following screenshot illustrates the result of the above code.

![MAUI SfCardView image](images/maui-card-initial.png)

### Define the card layout

Initialize a card layout with a card view using the provided code sample below.

{% tabs %}
{% highlight xaml tabtitle="MainPage.xaml" %}

<cards:SfCardLayout HeightRequest="500" BackgroundColor="#F0F0F0">

    <cards:SfCardView CornerRadius="10">
        <Label  Text="Peach" BackgroundColor="PeachPuff"/>
    </cards:SfCardView>

    <cards:SfCardView CornerRadius="10">
        <Label  Text="MediumPurple" BackgroundColor="MediumPurple"/>
    </cards:SfCardView>

    <cards:SfCardView CornerRadius="10" >
        <Label  Text="LightPink" BackgroundColor="LightPink"/>
    </cards:SfCardView>

</cards:SfCardLayout>

{% endhighlight %}
{% highlight c# tabtitle="MainPage.xaml.cs" %}
    SfCardLayout cardLayout = new SfCardLayout();

    //Add children for card layout 
    cardLayout.Children.Add(new SfCardView() { Content = new Label() { Text = "Peach", BackgroundColor = Colors.PeachPuff }, CornerRadius = 15 });

    cardLayout.Children.Add(new SfCardView() { Content = new Label() { Text = "MediumPurple", BackgroundColor = Colors.MediumPurple },CornerRadius = 15 });

    cardLayout.Children.Add(new SfCardView() { Content = new Label() { Text = "LightPink", BackgroundColor = Colors.LightPink },CornerRadius = 15 });

    this.Content = cardLayout;
{% endhighlight %}
{% endtabs %}	

The following screenshot illustrates the result of the above code.

![MAUI SfCardView image](maui-card-cardlayout.gif)


N> You can refer to our [.NET MAUI Cards](https://www.syncfusion.com/maui-controls/maui-cards) feature tour page for its groundbreaking feature representations. You can also explore our [.NET MAUI Cards Example](https://github.com/syncfusion/maui-demos/tree/master/MAUI/Cards) that shows you how to render and configure the Cards in .NET MAUI.