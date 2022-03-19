# Image Lab - A Cross Stitch Application.

### The source code of this project is private as this is an academic project. If you need access to the code, kindly contact the author.

### About
Image Lab lets you manipulate images by applying various color transformation effects, filters and color density reduction effects to images. You can now create cross-stitch pattern, pixelate your images and create mosaic art of the images.

## List of features
- A Graphical User Interface to work with images.
- Load images from disk.
- Blur the images.
- Sharpen the images.
- Apply greyscale effect to images.
- Apply sepia effect to images.
- Reduce color density of images by dithering.
- Apply Mosaic effect images 
- Adjust density for mosaic by providing number of seeds the image should have.
- Apply Pixelation effect to images.
- Adjust density of pixelation by providing number of seeds/squares the image should have.
- Write the converted/manipulated images to disk.
- Create batch file to execute all the commands at once.
- Load batch file from disk to execute all the commands in the file at once.

## Cross Stitch Features
- Generate a cross stitch version of image.
- Cross Stitch Image will have only floss colors. (Total 489 floss colors).
- Create Cross Stitch Image from custom palette of floss colors.
- Replace a color in the cross stitch pattern by your own color.
- Remove a particular color from the cross stitch image.
- See pattern of cross stitch overlayed on the top of cross stitch image.
- Save cross stitch image to disk 
- Save cross stitch pattern to the disk.

## Getting Started

p5-CrossStitchApplication jar file is used for running this project.

## Usage

There are two ways to use this application
<br>1) Use Interactive Graphical User Interface.
<br>2) Use a batch file to execute all the commands at once.

### Interactive Method.

```
java -jar p5-CrossStitchApplication -interactive
```
This will launch a graphical user interface (GUI)
<br>GUI will have a menu to perform various operations.

Menu : 
<li>File - Provides menu items to deal with file read/save related operations. (Shortcut - ALT + F)
<li>Effects - Provides menu items to apply various effects on the images. (Shortcut - ALT + E)

File Menu Items : 
<li>Load Image - Loads the image from the disk. (Shortcut - CTRL + I)
<li>Save Image - Saves the image to the disk. (Shortcut - CTRL + S)
<li>Create Batch File - Allows to enter commands for batch execution. (Shortcut - CTRL + F)
<li>Execute Batch File - Loads the batch file from disk to run a batch execution (Shortcut - CTRL + E)
<li>Save Cross Stitch Pattern - Saves the cross stitch pattern to the disk. (Shortcut - CTRL + P)
<li>Exit - Closes the Application ((Shortcut - CTRL + Q)


Effects Menu Items : 
<li>Blur Effect - Blurs the image. (Shortcut - SHIFT + B)
<li>Sharpen Effect - Sharpens the image. (Shortcut - SHIFT + S)
<li>Sepia Effect - Applies sepia effect. (Shortcut - SHIFT + I)
<li>GreyScale Effect - Converts the image to greyscale. (Shortcut - SHIFT + G)
<li>Dither Effect - Color Density Reduction dither effect is applied. (Shortcut - SHIFT + D)
<li>Pixelate Effect - Pixelates the image. (Shortcut - SHIFT + P)
<li>Mosaic Effect - Creates the mosaic version of image. (Shortcut - SHIFT + M)
<li>Cross Stitch Pattern - Creates the cross stitch version of image. (Shortcut - SHIFT + C)

## How to use the program
1. Load Image 
<br>Click File -> Load Image
2. Apply blur effect
<br>Click Effects -> Blur Effect
3. Apply Sepia effect
<br>Click Effects -> Sepia Effect
4. Apply GreyScale effect
<br>Click Effects -> GreyScale Effect
5. Apply Dither effect
<br>Click Effects -> Dither Effect
<br>Enter the intensity of dither as desired.
<br>Click OK.
6. Apply Pixelate effect
<br>Click Effects -> Pixelate Effect
<br>Enter the number of square.
<br>Click OK. 
7. Apply Mosaic effect
<br>Click Effects -> Mosaic Effect
<br>Enter the number of seeds.
<br>Click OK. 
8. Aply Cross Stitch effect
<br>Click Effects -> Cross Stitch Pattern
<br>Enter the number of square in pattern.
<br> Select number of colors from which pattern is to be generated. Leave blank and Continue if all colors are needed.
<br>Click OK. 

#### How to replace color 
<li> Once the cross stitch pattern is generated, click on any square to replace the color.
<li> Click Replace Color.
<li> Select the color to be replaced from the combo box.
<li> Click OK.

#### How to remove color
<li> Once the cross stitch pattern is generated, click on any square to replace the color.
<li> Click Remove Color.

#### See Cross Stitch Pattern and Legend.
<li> Once the cross stitch pattern is generated, click on any square to replace the color.
<li> Click Show Pattern Overlay.
<li> Cross Stitch Pattern will be overlayed on top of cross stitch image and legend will be show at the bottom.

#### Create Batch File.
<li> Click File.
<li> Click Create Batch File.
<li> Enter commands.
<li> Click Execute.

### Batch File Method.

```
java -jar p5-CrossStitchApplication batch-commands.txt
```
where p5-CrossStitchApplication is the runnable jar file containing the driver for the project
and batch-commands contains all the commands that can be use to apply effects on 
the images.

##### List of Commands and their Usage ( Create batch file using these commands )

```
1) load <filepath> 
- filepath is the path of image to be loaded.

2) blur
- Applies blur effect on the image. It takes no parameter.

3) sharpen
- Applies sharpen effect on the image. It takes no parameter.

4) greyscale
- Applies greyscale effect on the image. It takes no parameter.

5) sepia
- Applies sepia effect on the image. It takes no parameter.

6) dither <number of colors>
- Applies dither effect on the image. 
- Take numeric parameter indicating the number of colors the image has to be reduced in.

7) mosaic <number of seeds> 
- Applies mosaic effect on the image.
- Take numeric parameter indicating the total number of seeds that can exist in the resultant image.

8) pixelate <number of squares>
- Applies pixelate effect on the image. 
- Take a numeric parameter indicating the total number of squares across a image.

9) pattern <number of squares>
- Applies pixelate effect on the image based on number of squares provided in parameter.
- Generates cross stitch pattern of pixelated image.
- Take a numeric parameter indicating the total number of squares across a image.

10) Save <filepath>
- Saves the image. Takes string as parameter to indicate the path and name to save the image.

11) quit
- quits the program execution.

12) q
- Alternative to quit command. It also terminates the execution.
```

## Example Usage

Run 1 : 

```
java -jar p5-crossStitchApplication input.txt
```
Applies all the commands specifies in the input.txt file and generates the images and pattern. 

The above example shows usage where : 
- Image is loaded
- Effect is applied
- Image is saved.
- to apply next effect we repeat the cycle.


Run 2 : 

```
java -jar p5-crossStitchApplication input.txt
```
The above example shows usage where multiple effects are applied before saving the image. It follow something like : 
- load beach.jpg
- blur
- greyscale
- save beach-new.jpg

Here the image will first be blurred and then greyscaled. The output will be greyscaled image that is blur. 

Run 3 : 

```
java -jar p5-crossStitchApplication -interactive 
```

Here a interactive graphical user interface will be displayed.

### Commands example :

```
load beach.jpg
dither 8
save beach-dither.jpg
load beach.jpg
blur
save beach-blur.jpg
load beach.jpg
greyscale
save beach-greyscale.jpg
load beach.jpg
sepia
save beach-sepia.jpg
load beach.jpg
sharpen
save beach-sharpen.jpg
load beach.jpg
mosaic 570
save beach-mosaic.jpg
load beach.jpg
pixelate 30
save beach-pixelate.jpg
load beach.jpg
pattern 30
save beach-pattern.txt
quit            
```

### Support command line syntax
<li> -interactive 
<li> -script [batch_file_path]

## Change Log
- Added View to interact with controller and model.
- Added Graphical User Interface using swing.
- GUI will display the results.
- Cross stitch image will be displayed having floss colors only.
- A single color can be removed from the cross stitch pattern.
- A single color can be replaced with another color.
- User can select custom palette of cross stitch floss colors to generated colors from.
- Pattern can be overlayed on top of cross stitch image.

## Design/Model Changes
- Added JList to allow user to create custom palette to be used for cross stitch image.
- Added JComboBox to allow user to select a single color which can be replaced from cross stitch pattern.
- Added various method in IView interface to help all the operation supported by application.
- Added RemoveColor and ReplaceColor commands in controller for reusability. 
- Added DmcImage class which represents cross stitch image and pattern. This makes it easy to perform operations like 
removeColor and replaceColor as DmcImage acts as AbstractDataType.
- Controller will have constructor to support batch and view execution modes.

## Assumptions
- Each channel can have maximum of 8 bits i.e maximum of 256 colors in each channel.
- The number of colors that the image has to be reduced to for dithering is for each channel. For example - if the 
  image has to be reduced to 2 colors ... it will be 2 colors each for R,G,B.
- Pixelation can generate perfect squares ( ex. 10x10 ) or squares whose width x height differs by 
only 1 (10x11, 11x10,etc) provided that the number of offset pixels are less than number super-pixels.
- Parameter for pixelation indicates the total number of super pixels across the width.
- Applying effect changes the image. If any new effect is applied, it will be applied on the changed effect. If new effect is to be applied on
  original effect, then original image has to be loaded again. For example. If blur is applied on image and then greyscale is applied, the resultant
  image will be a image that is greyscale in color and blurred.
- Each command will be on a new line in batch file.
- Setting console encoding to UTF-8 in run configurations.

## Limitations
- The intensity of blur,sharpen, greyscale, sepia cannot be adjusted.
- Application supports UTF-8 character encoding. If the operating system does not have default encoding as UTF-8 , then use JAVA_TOOL_OPTION=-Dfile.encoding=UTF8 as envrionment variable.

## Resources Reference / Citation
- The images used for example run and in this project are clicked from my phone camera and are original. I authorize its use in this project. 
- The unicode used are from website : https://en.wikipedia.org/wiki/List_of_Unicode_characters

## Author
- Meet Patel
