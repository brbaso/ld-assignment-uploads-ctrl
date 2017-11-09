=== LearnDash Assignment Uploads Control  ===
Contributors: brbaso
Tags: learndash, assignments, LMS, learning management system, courses online
Author URI: https://github.com/brbaso/
Plugin URI: https://github.com/brbaso/ld-assignment-uploads-ctrl
Requires at least: 4.0
Tested up to: 4.8.3
Requires PHP: 5.6.x
Stable tag: 1.0.0
License: GPLv2 or later

A simple LearnDash Assignment Uploads Control plugin for [LearnDash](https://www.learndash.com/) LMS .

== Description ==

This LearnDash plugin allows administrators to set limitations like max. file size, allowed file extensions and max. number of uploaded files for specific Lesson/Topic.
Once the options are set, all logged in and assigned to a LD Course Users will see additional information on their Lessons/Topics Assignment upload sections.
If a 'bad' Assignment( one which do not fit limitations from LDAUC Settings page ) upload is performed the User will see a new page with a Notice what was wrong and link back to the Lesson/Topic page to try another upload.
The 'bad' Assignment will be disregarded and will not be uploaded.

It:

* will prevent logged in Users to upload an Assignment which does not fit limitations defined by administrator.
* provides a Settings screen in wp-admin: LearnDash LMS -> LDAUC Setings
* provides [ld-markcomplete] short code to be placed in LearnDash Lesson and Topic templates
* allows admin to set Assignment upload limitations: 'max. file size', 'allowed file extensions' and 'max. number of uploaded files' for LearnDash Lessons/Topics
* allows you to adjust and additionally style the 'bad' upload Notice page and upload Assignment section information in your Topics and Lessons
* allows you to make Template override folder in your Theme and make layout and style there, keeping them update safe ...

== Installation ==

1. Unzip and then upload the 'ld-assignment-uploads-ctrl' folder to the '/wp-content/plugins/' directory

2. Activate the plugin through the 'Plugins' menu in WordPress

3. Go to LearnDash LMS -> LDAUC Setings and set your options.

4. go to your LearnDash lesson.php or topic.php template and in 'Display Lesson Assignments' section, replace line :
" echo learndash_mark_complete( $post ); "
with the new [ld-markcomplete] shortcode line :
" echo do_shortcode("[ld-markcomplete]"); "

5. If you want to additionaly style or change layout of the the 'bad' upload Notice page and upload Assignment section information in your Topics and Lessons you can do that in Plugin's Template directory or you can create 'ld-assignment-uploads-ctrl' folder in your Theme/Child Theme folder, copy content from Plugin's Template folder to the new folder in Theme/Child Theme directory and make additions/changes there.

== Frequently Asked Questions ==

= MultiSite support? =

No. it is planned for further development

== Screenshots ==
1. Shows the Settings page
2. Shows the Front End
3. Shows the Front End 'bad' upload Notice - max. file size allowed
4. Shows the Front End 'bad' upload Notice - file extension not allowed
5. Shows the Front End 'bad' upload Notice - max. number of uploads allowed

== Changelog ==
= 1.0 =
* Initial release.

== Upgrade Notice
= 1.0 =


