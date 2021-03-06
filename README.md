# LearnDash Assignment Uploads Control

A simple WP plugin for [LearnDash](https://www.learndash.com/) Learning Management System.

**notice:**
Since Version 2.5.0, LearnDash introduced assignment upload control parameters at Lesson and Topic level. This plugin will be adapted for those changes soon enough, but until then it is recomennded for use on LearnDash versions < 2.5.0


### Description

This LearnDash plugin allows administrators to set limitations like **max. file size**, **allowed file extensions** and **max. number of uploads** for LearnDash Lessons and Topics assignment uploads.

The plugin adds 'LDAUC Settings' submenu under Learndash LMS admin link. By clicking on the link **'LearnDash Assignment Uploads Control Settings'** page appears where upload options can be set.

**LearnDash Assignment Uploads Control Settings page:**

![LearnDash Assignment Uploads Control Settings](http://brbaso.com/images/ld-assignment-uploads-ctrl/screenshot-1.png)

Once the options are set, all users, which are logged in and assigned to a LD Course will see additional information about upload limitations on their Lessons/Topics Assignment upload sections.

**Additional information about upload limitations:**

![Additional information about upload limitations](http://brbaso.com/images/ld-assignment-uploads-ctrl/screenshot-2.png)

If a 'bad' Assignment upload is performed, that is one which do not fit limitations set in the **'LearnDash Assignment Uploads Control Settings'** page, the User will see a new page with a Notice about what was wrong and with a  link back to the Lesson/Topic page to try another upload. In this case the 'bad' Assignment will be disregarded and will not be uploaded.

**File too big Notice:**

![File too big Notice](http://brbaso.com/images/ld-assignment-uploads-ctrl/screenshot-3.png)

**File extension not allowed Notice:**

![File extension not allowed Notice](http://brbaso.com/images/ld-assignment-uploads-ctrl/screenshot-4.png)

**Max number of uploads reached Notice:**

![Max number of uploads reached Notice](http://brbaso.com/images/ld-assignment-uploads-ctrl/screenshot-5.png)

Also, **[ld-markcomplete]** short code is generated which should be used in LearnDash Lesson and Topic templates to render additional info in 'Display Lesson Assignments' section.

The plugin is translation ready.

Layout, styling of plugin's front end or adding additional java script to the front end if needed, can be managed within files placed in plugin's **'templates'** folder. This files could be overridden by adding **'ld-assignment-uploads-ctrl'** folder to your Theme or Child Theme and copying them to it.

### Installation

1. Unzip and then upload the **'ld-assignment-uploads-ctrl'** folder to the **'/wp-content/plugins/'** directory

2. Activate the plugin through the 'Plugins' menu in WordPress

3. Go to **LearnDash LMS -> LDAUC Setings** and set your options.

4. go to your LearnDash lesson.php or topic.php template and in 'Display Mark Complete Button' section, **replace line** :
```
echo learndash_mark_complete( $post );
```
**with** the new [ld-markcomplete] shortcode line :
``` 
echo do_shortcode("[ld-markcomplete]");
```

5. If you want to additionaly style or change layout of the the 'bad' upload Notice page or upload Assignment section information in your Topics and Lessons you can do that in **Plugin's templates directory**. 

    Alternatively you can create **'ld-assignment-uploads-ctrl' folder** in your Theme or Child Theme. 
    
    After you created the folder copy content from Plugin's Template folder to the newly created folder in your Theme or Child Theme. 
    
    Edit layouts, css or js there, the original Plugin's files are overridden now with your own layouts and styles...

## TO DO

Make changes/additions so that plugin work with the newest LearnDash Version >= 2.5.0