=== LearnDash Assignment Uploads Control  ===
Contributors: brbaso
Tags: learndash, assignments
Author URI: https://github.com/brbaso/
Plugin URI: https://github.com/brbaso/
Requires at least: 4.0
Tested up to: 4.8.3
Stable tag: 1.0
License: GPLv2 or later

A simple LearnDash Assignment Uploads Control plugin for [LearnDash](https://www.learndash.com/) LMS.

== Description ==

This LearnDash plugin allows administrators to set limitations like max. file size, allowed file extensions and max. number of uploaded files for specific Lesson/Topic.
Once the options are set, all logged in and assigned to a LD Course Users will see additional information on their Lessons/Topics Assignment upload sections.
If a 'bad' Assignment( one which do not fit limitations from LDAUC Settings page ) upload is performed the User will see a new page with a Notice what was wrong and link back to the Lesson/Topic page to try another upload.
The 'bad' Assignment will be disregarded and will not be uploaded.

It:

* will prevent logged in Users to upload an Assignment which does not fit limitations defined by administrator.
* provides a Settings screen in wp-admin: LearnDash LMS -> LDAUC Setings
* allows an admin to set Assignment upload limitations: max. file size, allowed file extensions and max. number of uploaded files for Lessons/Topics
* provides a Private checkbox in the upper right corner of every page, post, and custom post type selected in Settings

For more BuddyPress plugins, please visit [PhiloPress](http://www.philopress.com/)

== Installation ==

1. Unzip and then upload the 'ld-assignment-uploads-ctrl' folder to the '/wp-content/plugins/' directory

2. Activate the plugin through the 'Plugins' menu in WordPress

3. Go to LearnDash LMS -> LDAUC Setings and set your options.

== Frequently Asked Questions ==

= MultiSite support? =

No. it is planned for further development

== Screenshots ==
1. Shows the Settings page
2. Shows the Front End
3. Shows the Front End bad upload notice - max. file size
4. Shows the Front End bad upload notice - bad file extension
5. Shows the Front End bad upload notice - max. number of uploads allowed

== Changelog ==
= 1.0 =
* Initial release.

== Upgrade Notice
= 1.0 =


