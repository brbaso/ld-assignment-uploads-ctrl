## LearnDash Assignment Uploads Control

A simple WP plugin for [LearnDash](https://www.learndash.com/) Learning Management System.

###Description
This LearnDash plugin allows administrators to set limitations like **max. file size**, **allowed file extensions** and **max. number of uploads** for LearnDash Lessons and Topics assignment uploads.

The plugin adds 'LDAUC Settings' submenu under Learndash LMS admin link. By clicking on the link **'LearnDash Assignment Uploads Control Settings'** page appears where upload options can be set.

Once the options are set, all users, which are logged in and assigned to a LD Course will see additional information on their Lessons/Topics Assignment upload sections.

If a 'bad' Assignment upload is performed, that is one which do not fit limitations set in the **'LearnDash Assignment Uploads Control Settings'** page, the User will see a new page with a Notice about what was wrong and with a  link back to the Lesson/Topic page to try another upload. In this case the 'bad' Assignment will be disregarded and will not be uploaded.

Also, **[ld-markcomplete]** short code is generated which should be used in LearnDash Lesson and Topic templates to render additional info in 'Display Lesson Assignments' section.

The plugin is translation ready.

Layout, styling of plugin's front end or adding additional java script to the front end if needed, can be managed within files placed in plugin's **'templates'** folder. This files could be overridden by adding **'ld-assignment-uploads-ctrl'** folder to your Theme or Child Theme and copying them to it.

###Installation

1. Unzip and then upload the **'ld-assignment-uploads-ctrl'** folder to the **'/wp-content/plugins/'** directory

2. Activate the plugin through the 'Plugins' menu in WordPress

3. Go to **LearnDash LMS -> LDAUC Setings** and set your options.

4. go to your LearnDash lesson.php or topic.php template and in 'Display Lesson Assignments' section, **replace line** :
```
echo learndash_mark_complete( $post );
```
**with** the new [ld-markcomplete] shortcode line :
``` 
echo do_shortcode("[ld-markcomplete]");
```

5. If you want to additionaly style or change layout of the the 'bad' upload Notice page or upload Assignment section information in your Topics and Lessons you can do that in **Plugin's templates directory** Alternatively you can create **'ld-assignment-uploads-ctrl' folder** in your Theme or Child Theme. After you created the folder copy content from Plugin's Template folder to the newly created folder in your Theme or Child Theme. Edit layouts, css or js there, the original Plugin's files are overridden now with your own layouts and styles...


