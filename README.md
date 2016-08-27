# XamarinFormsBorderedLabels
XAML Bordered-label-like elements

## Screenshot
![screenshot](https://raw.githubusercontent.com/xamarin-samples/XamarinFormsBorderedLabels/master/screenshots/screenshot.png)

## Pickuped code
### [Page1.xaml](XamarinFormsBorderedLabels/XamarinFormsBorderedLabels/Page1.xaml)
```xml
....
<!-- Hello1: Thin red border -->
<Frame WidthRequest="110"
       HeightRequest="80"
       HorizontalOptions="Center"
       VerticalOptions="Center"
       Padding="0"
       OutlineColor="#f00"
       >
  <Label Text="Hello1" TextColor="#ff0" FontSize="20"
         HorizontalOptions="Center"
         VerticalOptions="Center" />
</Frame>

<!-- Hello2: Thick red border, and black background -->
<Frame WidthRequest="106" HeightRequest="76" HorizontalOptions="Center" VerticalOptions="Center"
       Padding="2"
       BackgroundColor="#f00"
       >
  <Frame Padding="0"
         BackgroundColor="#000"
         VerticalOptions="Fill"
         HorizontalOptions="Fill">
    <Label Text="Hello2" TextColor="#ff0" FontSize="20"
           HorizontalOptions="Center"
           VerticalOptions="Center" />
  </Frame>
</Frame>

<!-- Hello3: Thick red border (It has Label-like appearance, but it's not a Label but a Button  -->
<Button Text="Hello3" TextColor="#ff0" FontSize="20"
        WidthRequest="110"
        HeightRequest="80"
        HorizontalOptions="Center"
        VerticalOptions="Center"
        BackgroundColor="Transparent"
        BorderColor="#f00"
        BorderWidth="2"
        />

<!-- Hello4: Normal button -->
<Button Text="Hello4" TextColor="#ff0" FontSize="20"
        WidthRequest="110"
        HeightRequest="80"
        HorizontalOptions="Center"
        VerticalOptions="Center"
        />
....
```

## Tricks
Xamarin.Forms Label element has no border attribute, so we have to use some tricks.

### Hello1
- This is a Label surrounded by Frame which has OutlineColor attribute.

### Hello2
- This is a Label surrounded by **TWO** Frames which have BackgroundColor attributes.
- Outside Frame porvides border-colored BackgroundColor attribute.
- Inside Frame porvides face-colored BackgroundColor attribute.

### Hello3
- This is **not a Label** but a Button element, but it has Label-like appearance.
- Set BackgroundColor="Transparent" to remove default button appearance.
- Then, set BorderColor and BorderWidth to make red thick border.
- **I personally like this way.**

### Hello4
- This is a normal Button. (for comparison)
