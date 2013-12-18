# monolit

## monolit

*   is a **simple** photoblog theme based on [WordPress][1] and [YAPB][2]. It's designed to be minimalistic and to focus on what's important - the photo.
*   **depends** on the [Yet Another Photoblog][2] plugin.
*   has a **fixed width** of 900 pixels. It will scale down larger images.
*   has **inline comments** and **no popups**
*   is based on the default WordPress theme, but has also borrowed stuff from the [grain][3] theme and the [monochrome][4] blog with permission from the authors.
*   **free** to be used or modified by whoever chooses to do so

## monolit is not

*   a photo gallery.
*   feature-rich - you will not find EXIF-data (yet), syndication, or thousands of options. It will not make you coffee.

# Installation and configuration notes

## Installation

1.  Download and install [WordPress][1]
2.  Download and install [YAPB][2]
3.  Download / checkout monolit and put it in your **wp-content/themes/** folder

## Configuration

1.  In the YAPB configuration menu, disable automatic embedding
2.  In the Presentations menu, enable monolit as your theme
3.  In the Options / Reading menu change the 'Show at most' to the maximum
    number of thumbnails you want to show in a single archive page. By default I
    recommend this number to be a multiple of 6, eg. 6, 12, 18, 24, etc. This is
    the default number of thumbs per line and can be changed through the
    MONOLIT\_SET\_THUMBS\_PER\_LINE value in the **config/config.php** file. If you
    change this value, remember that the 'Show at most' value should probably
    also be changed.

## If you wan to enable archives

*   Create an 'archives' page through Manage/Pages. Remember the title and be sure to select the 'Arcives' template under 'Page Template'.
*   in the **config/config.php** file 
    *   change the value of MONOLIT\_SET\_ARCHIVE\_WP\_TITLE to the title of the page you just created
    *   change the value of MONOLIT\_SET\_SHOW_ARCHIVES to 1

## If you want to enable an about page

*   Create an 'about' page through Manage/Pages. Remember the title.
*   in the **config/config.php** file: 
    *   change the value of MONOLIT\_SET\_ABOUT\_WP\_TITLE to the title of the page you just created
    *   change the value of MONOLIT\_SET\_SHOW_ABOUT to 1
    *   to show the timestamp on the about page set MONOLIT\_SET\_SHOW\_ABOUT\_TIMESTAMP to 1

## Changing the copyright notice and other settings

*   Copyright: Change the MONOLIT\_SET\_COPYRIGHT to whatever you want the copyright notice to say.
*   Change other configuration values in the file if needed. They are pretty much self-explanatory.

## About photo sizes

The theme automatically resizes images to a max width of 900 pixels and a max
height that is customizable through the MONOLIT\_SET\_MAX\_HEIGHT value
(default is 600 pixels). If you want wider images the layout will break unless
you change the stylesheet (look for the 'inside' class). Also you can configure
the thumbnail sizes through the MONOLIT\_SET\_THUMB\_WIDTH and
MONOLIT\_SET\_THUMB\_HEIGHT values. If you change these values - especially
the width, you might also want to change the MONOLIT\_SET\_THUMBS\_PER_LINE and
'Show at most' values as previously explained.

## About language and messages

Language and messages can be configured through the **lang/lang.php** file. It
might take some skill to figure out which message goes where :-)

## Todo / some future version

*   a smarter way to control the configuration, ie. via the admin page
*   use imagemagick to resize and optionally sharpen downsized photos

## Requests from users

*   optional support for EXIF-data (currently being developed but it will take a while)
*   syndication support (not likely to happen in near future)

 [1]: http://www.wordpress.org/
 [2]: http://johannes.jarolim.com/yapb/
 [3]: http://mac.defx.de/grain-theme
 [4]: http://www.226-design.com/monochrome/
