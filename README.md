# CSS Color

Color can easily bring your pages to life. Here, we will look at:

- How to specify colors, as there are three common ways in which you can indicate your choice of colors.
- Color terminology, as there are some terms that are very helpful to understand when it comes to picking colors.
- Contrast, and ensuring that your text is readable.
- Background colors for behind either your entire page or parts of a page.

## Foreground Color.

The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

**a. RGB VALUES.**

- These express colors in terms of how much red, green and blue are used to make it up. For example: **rgb(100, 100, 90)**.

**b. HEX CODES.**

- These are six-digit codes that represent the amount of red, green and blue in a color. proceded by a pound or hash # sign. For example: **#ee3e80**.

**c. COLOR NAMES.**

- There are **147** predefined color names that are recognized by browsers. For example: **DarkCyan**.

```
/* color name */
h1{
    color: DarkCyan;
}

/* hex code */
h2{
    color: #ee3e80;
}

/* rgb value */
p{
    color: rgb(100, 100, 90);
}

```

Anything between the **/\*** symbols and the **\*/** symbols will not be interpreted by the browser. They are used to add comments to your CSS files. The use of comments can help you to understand a CSS file (and organize it, by splitting a long document into sections).

## Background Color.

CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.

You can specify your choice of background color in the same three ways tou can specify foreground colors: **RGB values, hex codes and color names** (as seen above).

If you do not specify a background color, then the background is transparent.

By default, most browser windows have a white background, but browser users can set a background color for their windows, so if you want to be sure that the background is white you can use the background-color property on the **&lt;body&gt;** element.

```
body{
    background-color: rgb(200,200,200);
}

h1{
    background-color: DarkCyan;
}

h2{
    background-color: #ee3e80;
}

p{
    background-color: white;
}
```

## Understanding the concept of color.

Every color on a computer screen is created by mixing amounts of red, green and blue. To find the color you want, you can use a color picker.

Computer monitors are made up of thousands of tiny squares called pixels(if you look very closely at your monitor you should be able to see them).

![colorpicker](https://user-images.githubusercontent.com/68738624/132853903-83e4d40e-4289-4bdf-a31d-16b91ef02721.jpg)

When the screen is not turned on, it's black because it's not emitting any light. When it's turned on, each pixel can be different color, creating a picture.

The color of every pixel on the screen is expressed in terms of a mix of red, green and blue - just like a television screen.

### a. RGB Values.

Values for red, green and blue are expressed as numbers between 0 and 255.

![mediumAquaMarine](https://user-images.githubusercontent.com/68738624/132855201-2e6bfedf-9bda-4d90-9b6e-56f0684772d0.jpg)

**rgb(102, 205, 170)**

This color is made up of the following values:

- 102 red, 205 green and 170 blue.

### b. HEX Codes.

Hex values represent values for red, green and blue in hexadecimal code.

![mediumAquaMarine](https://user-images.githubusercontent.com/68738624/132855201-2e6bfedf-9bda-4d90-9b6e-56f0684772d0.jpg)

**#66cdaa**

The value of the _red_ **(102)** is expressed as **66** in hexadecimal code. The **205** of the _green_ is expressed as **cd** and the **170** of the _blue_ equated to **aa**.

### c. Color Names.

Colors are represented by predefined names. However, they are limited in number.

![mediumAquaMarine](https://user-images.githubusercontent.com/68738624/132855201-2e6bfedf-9bda-4d90-9b6e-56f0684772d0.jpg)

**MediumAquaMarine**

There are 147 color names supported by browsers (this color is MediumAquaMarine). Most consider this to be a limited color palette, and it is hard to remember the name for each of the colors so (Apart from white and black) they are not commonly used.

### Hue.

Hue is near to the colloquial idea of color.

![hue](https://user-images.githubusercontent.com/68738624/132856265-9ed2700f-f42e-46d1-a340-93ae842b57a8.jpg)

### Saturation.

Saturation refers to the amount of gray in a color. At maximum saturation, there would be no gray in the color. At minimum saturation, the color would be mostly gray.

![saturation](https://user-images.githubusercontent.com/68738624/132856898-6113fb1e-e638-4a5e-989e-9385acda3a79.jpg)

### Brightness.

Brightness (or "value") refers to how much black is in a color. At maximum brightness, there would be no black in the color. At minimum brightness, the color would be very dark.

![brightness](https://user-images.githubusercontent.com/68738624/132879697-bf811def-7045-49ba-8481-148ba20a6f0e.jpg)

## Contrast.

When picking foreground and background colors, it is important to ensure that there is enought contrast for the text to be legible.

### a. Low Contrast.

![lowContrast](https://user-images.githubusercontent.com/68738624/132858974-396e14b9-d0f3-45de-81c6-317776c1c5c8.jpg)

- Text is harder to read when there is low contrast between background and background colors.

- A lack of contrast is particularly a problem for those with visual impairments and color blindness.

### b. High Contrast.

![highContrast](https://user-images.githubusercontent.com/68738624/132859431-0fc61b38-a4e4-4870-9ad6-db1d5cf4f965.jpg)

- Text is easier to read when there is higher contrast between background and foreground colors.

- If you want people to read a lot of text on your page, however, then too much contrast can make it harder to read, too.

### c. Medium Contrast.

![mediumContrast](https://user-images.githubusercontent.com/68738624/132859668-4f07c3c8-0c20-4e31-8ba9-a892ba5f98b9.jpg)

- For long spans of text, reducing the contrast a little bit improves readability.

- You can reduce contrast by using dark gray text on a white background or an off-white text on a dark background.

## CSS3: Opacity.

CSS3 introduces the opacity property which allows you to specify the opacity of an element and any of its child elements. The value is a number between **0.0** and **1.0** (so a value of **0.5** is **50%** opacity and **0.15** is **15%** opacity).

The CSS3 rgba property allows you to specify a color, just like you would with a RGB value, but adds a fourth value to indicate opacity. This value is known as an **alpha value** and is a number between **0.0** and **1.0** (so a value of **0.5** is **50%** opacity and **0.15** is **15%** opacity). The _rgba_ value will only affect the element on which it is applied (not child elements).

Because some browsers will not recognize RGBA colors, you can offer a fallback so that they display a solid color. It there are two rules that apply to the same element, the latter of the two will take priority. To create the fallback, you can specify a color as a hex code, color name or RGB value, followed by the rule that specifies an RGBA value. If the browser understands RGBA colors it will use that rule. It it doesn't, it will use the RGB value.

```
p.one{
    background-color: rgb(0, 0, 0);
    opacity: 0.5;
}

p.two{
    background-color: rgb(0, 0, 0);
    background-color: rgba(0, 0, 0, 0.5);
}
```

## CSS3: HSL Colors.

CSS3 introduces an entirely new and intuitive way to specify colors using hue, saturation, and lightness values.

**a. HUE**.

Hue is the colloquial idea of color. In HSL colors, hue is often represented as a color circle where the angle represents the color, althought it may also be shown as a slider with values from 0 to 360.

![hue(2)](https://user-images.githubusercontent.com/68738624/132862490-02deb19b-55b2-4960-89dd-eaff58cf950f.jpg)

**b. SATURATION**.

Saturation is the amount of gray in a color. Saturation is represented as a percentage. **100%** is a full saturation and **0%** is a shade of gray.

![saturation](https://user-images.githubusercontent.com/68738624/132856898-6113fb1e-e638-4a5e-989e-9385acda3a79.jpg)

**c. LIGHTNESS**.

Lightness is the amount of white(lightness) or black(darkness) in acolor. Lightness is represented as a percentage. **0%** lightness is black, **100%** lightness is black, and **50%** lightness is normal. Lightness is sometimes referred to as **_luminosity_**.

![lightness](https://user-images.githubusercontent.com/68738624/132880392-0dadd151-0cb6-4122-a3aa-4bb2c2d706ac.jpg)

> Please note that the lightness is a different concept to brightness. Graphic design software(such as Photoshop and GIMP) have color pickers that use hue, saturation, and brightness - but brightness only adds black, whereas lightness offers both white and black.

### CSS3: HSL & HSLA.

The **hsl color property** has been introduced in CSS3 as an alternative way to specify colors. The value of the property starts with the letters **hsl**, followed by individual values inside parenthesis for:

a. HUE

- This is expressed as an angle (between 0 and 360 degrees).

b. SATURATION

- This is expressed as a percentage.

c. LIGHTNESS

- This is expressed as a percentage with **0%** being white, **50%** being normal and **100%** being black.

The **hsla color property** allows you to specify color properties using hue, saturation, and lightness as above, and adds a fourth value which represents transparency (just like the rgba property).

The **a** stands for: **ALPHA**

- ALPHA is expressed as a number between **0** and **1.0**. For example, **0.5** represents **50%** transparency, and **0.75** represents **75%** transparency.

This provides a fallback because if there are two rules that apply to the same element in CSS, the latter of the two always takes priority. This means that if the browser understands **HSL** and **HSLA colors**, it will use that rule; and if it does not, it will use the first rule.

Because older browsers do not recognize **HSL** and **HSLA values**, it is a good idea to add an extra rule which specifies the color using a hex code, RGB value or color name. This should appear before the rule that uses the **_HSL or HSLA value_**.

```
body{
    background-color: #C8C8C8;
    background-color: hsl(0, 0%, 78%);
}

p{
    background-color: #ffffff;
    background-color: hsla(0, 0%, 78%, 0.5);
}
```
