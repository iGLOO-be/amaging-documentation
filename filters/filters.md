---
description: >-
  Adding these parameters to your image URLs can enhance, resize, images or
  compress i.e.
---

# Filters

| **Name** | Desc |
| :--- | :--- |
| **blur** | **`radius`** and **`sigma`** are numbers Blur the image with a Gaussian operator |
| **background** | **`color`** in hexadecimal notation Set the background color of your image |
| **border** | **`width`** and **`height`** are numbers in pixel Surround the image with a border of color |
| **crop** | **`width`** **`height`** **`x`** and **`y`** are numbers **`x`** and **`y`** are optionalPreferred size and location of the cropped image. The width and height give the size of the image that remains after cropping, and x and y are offsets that give the location of the top left corner of the cropped image with respect to the original image.If the x and y offsets are present, a single image is generated, consisting of the pixels from the cropping region. The offsets specify the location of the upper left corner of the cropping region measured downward and rightward with respect to the upper left corner of the image. **Pay attention to the 'x' delimiter between width and height.**  |
| **equalize** | Perform histogram equalization to the image |
| **extent** | **`width`** **`height`** **`x`** and **`y`** are numbers **`x`** and **`y`** are optionalComposite image on background color canvas imageThis option composites the image on a new background color \(background\) canvas image of size x.The existing image content is composited at the position specified by geometry x and y offset**Pay attention to the `x` delimiter between width and height.** |
| **flip** | Create a "mirror image".Reflect the scanlines in the vertical direction. |
| **flop** | Create a "mirror image".Reflect the scanlines in the horizontal direction. |
| **gravity** | **`type`** : northwest, north, northeast, west, center, east, southwest, south, southeast Direction primitive gravitates to when annotating the image. |
| **implode** | **`factor`** is a number Implode image pixels about the center. |
| **negative** | Replace every pixel with its complementary color. The red, green, and blue intensities of an image are negated. White becomes black, yellow becomes blue, etc… |
| **quality**  | **`value`** is 0 \(lowest image quality and highest compression\) to 100 \(best quality but least effective compression\). For the JPEG image formats, the default quality is 75. |
| **widthxheight** | Resize an image with width and height you provide.**Pay attention to the `x` delimiter between width and height.** |
| **sepia** | Give a sepia effect to your image |



