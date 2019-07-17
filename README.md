# WordPress Child Themes
ขั้นตอนสร้าง WordPress Child Themes

### 1. Create a child theme folder
สร้างโพเดอร์ wp-content/themes/`twentyseventeen-child`

### 2. Create a stylesheet: style.css
```
/*
 Theme Name:   AAgold
 Theme URI:    https://github.com/anuchit33/twentyseventeen-child/
 Description:  Twenty seventeen Child Theme
 Author:       Anuchit Yaiin
 Author URI:   https://anuchit.com
 Template:     twentyseventeen
 Version:      1.0.0
 License:      GNU General Public License v2 or later
 License URI:  http://www.gnu.org/licenses/gpl-2.0.html
 Tags:         light, dark, two-columns, right-sidebar, responsive-layout, accessibility-ready
 Text Domain:  twentyseventeenchild
*/

```

### 3. Enqueue stylesheet (สร้างไฟล์ functions.php)
```
<?php
add_action( 'wp_enqueue_scripts', 'my_theme_enqueue_styles' );
function my_theme_enqueue_styles() {
    wp_enqueue_style( 'parent-style', get_template_directory_uri() . '/style.css' );
 
}
```
