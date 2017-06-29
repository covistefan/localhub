# localhub
Contributors: www.covi.de
Contact: s.haendler@covi.de
Version: 1.0
Release: 2017-06-29
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=5762TWVRT6RQ4
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

# Description
Localhub is a tiny web based version control, that creates a zip file on call with version log

# Requirements
Requires „libzip“ which is bundled with PHP.

# Installation
1. Install folder „localhub“ on root level of your webspace
2. Create a (hidden) file called „.localhub“ on root level of your webspace 
3. Edit the „.localhub“ file and write down all files to put into zip - ONE per col. Examples:
   a. „./index.php“ => zips the index.php as it is on root level
   b. „./js/file.js“ => zips the „file.js“ into folder „js“
   c. „./index.org=>./index.php“ => zips the „index.org“ from your web account as „index.php“ on root level
   d. „./file.js=>./js/file.js“ => zips the „file.js“ from your web account as „file.js“ into folder „js“
4. Edit the „config.php“ in folder „localhub“:
   a. define('LOCALHUB', 'localhub'); // the directory, your localhub is located
   b. define('VERSIONS', 'versions.log'); // the filename to log versions
   c. define('BASEVERSION', '1.0'); // the base version your zip file will be named. required. NO dot at the end
   d. define('SLUG', 'slug'); // the slug before version  your zip file will be named. required. UNIX-filename-style
   e. define('LOCALDATE', 'd.m.Y, H:i'); // the date format, the last file will be shown
5. put the localhub script call to anywhere you want on your page „<?php require('./localhub/localhub.php‘); ?>“

# Changelog
## Version 1.0
* first release
