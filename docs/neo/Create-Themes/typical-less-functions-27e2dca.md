<!-- copy27e2dca36abf4e0b95bec39c73ad8f29 -->

# Typical LESS Functions

The following is a list of typical LESS functions for colors.



****


<table>
<tr>
<th valign="top">

LESS Function

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

saturate\(@color, 10%\);

</td>
<td valign="top">

Returns a color 10% points more saturated

</td>
</tr>
<tr>
<td valign="top">

desaturate\(@color, 10%\);

</td>
<td valign="top">

Returns a color 10% points less saturated

</td>
</tr>
<tr>
<td valign="top">

lighten\(@color, 10%\);

</td>
<td valign="top">

Returns a color 10% points lighter

</td>
</tr>
<tr>
<td valign="top">

darken\(@color, 10%\);

</td>
<td valign="top">

Returns a color 10% points darker

</td>
</tr>
<tr>
<td valign="top">

fade\(@color, 50%\);

</td>
<td valign="top">

Returns @color with 50% transparency

</td>
</tr>
<tr>
<td valign="top">

spin\(@color, 10\);

</td>
<td valign="top">

Returns a color with a 10 degree larger in hue

</td>
</tr>
<tr>
<td valign="top">

mix\(@color1, @color2, \[@weight: 50%\]\);

</td>
<td valign="top">

Returns a mix of @color1 and @color2

</td>
</tr>
<tr>
<td valign="top">

greyscale\(@color\);

</td>
<td valign="top">

Returns a grey, 100% desaturated color

</td>
</tr>
<tr>
<td valign="top">

contrast\(@color1, \[@darkcolor: black\], \[@lightcolor: white\], \[@threshold: 43%\]\);

</td>
<td valign="top">

Returns @darkcolor if @color1 is \> 43% luma \(perceptual brightness\), otherwise returns @lightcolor

</td>
</tr>
</table>

