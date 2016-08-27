# XamarinFormsBorderedLabels
XAML Bordered-label-like elements

## Screenshot
![screenshot](https://raw.githubusercontent.com/xamarin-samples/XamarinFormsBorderedLabels/master/screenshots/screenshot.png)

## Pickuped code
### [Page1.xaml](XamarinFormsBorderedLabels/XamarinFormsBorderedLabels/Page1.xaml)
```xml
....
....
<!-- Thin red border -->
<Frame Padding="0"
       VerticalOptions="Center"
       HorizontalOptions="Center"
       OutlineColor="#f00"
       WidthRequest="110"
       HeightRequest="80"
       >
  <Label Text="Hello1" TextColor="#ff0" FontSize="20" HorizontalOptions="Center" VerticalOptions="Center" />
</Frame>

<!-- Thick red border, and black background -->
<Frame Padding="2"
       BackgroundColor="#f00"
       VerticalOptions="Center"
       HorizontalOptions="Center"
       WidthRequest="106"
       HeightRequest="76">
  <Frame Padding="0"
         BackgroundColor="#000"
         VerticalOptions="Fill"
         HorizontalOptions="Fill">
    <Label Text="Hello2" TextColor="#ff0" FontSize="20" HorizontalOptions="Center" VerticalOptions="Center" />
  </Frame>
</Frame>

<!-- Thick red border (It has Label-like appearance, but it's not a Label but a Button  -->
<Button Text="Hello3"
        FontSize="20"
        TextColor="#ff0"
        WidthRequest="110"
        HeightRequest="80"
        BackgroundColor="Transparent"
        BorderColor="#f00"
        BorderWidth="2"
        HorizontalOptions="Center" />

<!-- Normal button -->
<Button Text="Hello4"
        TextColor="#ff0"
        FontSize="20"
        WidthRequest="110"
        HeightRequest="80"
        HorizontalOptions="Center"
        VerticalOptions="Center" />
....
```

## Tricks
Xamarin.Forms Label element has no border attribute, so we have to use some tricks.

### Hello1
- This is a Label arounded by Frame which has OutlineColor attribute.

### Hello2
- This is a Label arounded by **TWO** Frames which have BackgroundColor attributes.
- Outside Frame porvides border-colored BackgroundColor attribute.
- Inside Frame porvides face-colored BackgroundColor attribute.

### Hello3
- This is **not a Label** but a Button element, but it has Label-like appearance.
- Set BackgroundColor="Transparent" to remove default button appearance.
- Then, set BorderColor and BorderWidth to make red thick border.

### Hello4
- This is a normal Button. (for comparison)
