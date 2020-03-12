# 06_a_setup_checklist

## Invision & Figma

* Base things provided
  * Templates
  * Default page
  * Other pages
* Check comments on each page

## Change things in default reqruied files

* composer.json
  * Project Name
* packages.json
  * Project Name
* phpcs.xml.dist
  * Project Name
  * Theme Domain
  * Prefix

## Styleguide

Make color variables
Install required fonts ( Project + PC) - You can find all possible used fonts in style guide layer
Default font size for heading
Any type of hover effect
Shadow effects
Extra effects like section images,
Button + Button effects

## Fonts

* Check if the font is free, then download it, then make font face woff, woff2 from font squirrel
* If the font is paid, then search on Adobe Fonts. Make a new project, include the required fonts.
* If the fonts are paid, but not avaibale to download anywhere, then check the Google Drive folder and download from there.
* Even if not available there, then ask the company about it.
* After all of that make the font faces in Fonts.scss file of project.
* Make sure you name the font-family exactly like the name given when you open a ttf font file
* Find the default body font name used in the last theme and Find/Replace with current main body font. with all possible variations. One is given below
  * @include font(OldFont, bold, weight) &rightarrow; @include font(NewFont, bold, weight);

## Colors Variables

* There Should be a default black and white color section. For these you can use 5%, 10% etc for brigther or darker colors. Or dgrey &rightarrow; Gark Grey, lgrey &rightarrow; Light Grey etc.
  * Make the white colors
  * Make the black colors
* You can name the colors as per given names in styleguide.
* There may be some colors that need renaming like
  * Footer Frame &rightarrow; ftrbrdr
* Replace default colors
  * Link
  * Body
  * Headings

## Font Sizes

* Body, P
* All headings

## Export all related images

* Logo
* Any images in header
  * Button of header
* Any images in Footer
* Icons

## Interactive states

* Buttons

## Making Theme

### Header

* Logo
* Menu
* Other header things like buttons search etc

## Making Buttons

* Check how many button are there
* Check if there is any transparent buttons
* Make sure to use icons as svg if there are any in buttons
* Check if there are any button in colored section. Like blue button in black background section
* If there is any transparent button, then it will have 1px border. So make the .button default class a padding 1px less top bottom and give 1px solid transparent border

## Some Defaults

* Lists
  * ol
  * ul
* Headings
* Strong
* Bold
* Italic
* Paragraph
* Froms
  * Input fields
  * error field
  * checkbox
  * radio button
  * Select option
  * Send Button
* Header styling
  * Scroll Fixed colors
* Main Menu
  * Drop Down
* Feature Images/ Image Caption
* Quote
* Footer
