Welcome to the source code for _The Busy Coder's Guide to Android
Development_!

All of the source code in this archive is licensed under the
Apache 2.0 license except as noted.

The names of the top-level directories roughly correspond to a
shortened form of the chapter titles. Since chapter numbers
change with every release, and since some samples are used by
multiple chapters, I am loathe to put chapter numbers in the
actual directory names.

## Using in Android Studio

Most of the projects should have a `build.gradle` file suitable for
importing the project into Android Studio. Note, though, that you
may need to adjust the `compileSdkVersion` in `build.gradle` if it
requests an SDK that you have not downloaded and do not wish to
download.

You will also need your own independent copy of [Gradle](http://gradle.org)
1.12 installed and to know where you installed it. The first time you
import a project, you may be asked where your "Gradle home" is &mdash;
supply the directory into which you installed Gradle.

## Using in Eclipse

These projects can be imported using the normal Eclipse import process. That
being said, importing *all* the projects is probably a **really bad idea**, simply
because there are so many of them. Import select projects, if and when you need
them.

Note, though, that you will have to fix some things up, particularly if you
are getting errors:

- The build target of the project may be an Android SDK that you do not have
installed. You will need to set the project build target to something that
you have, by means of Project Properties.

- A few of these projects use [ActionBarSherlock](http://actionbarsherlock.com) or
other Android library projects. You will need to attach a suitable copy of those
projects to your app. For example, 
there is a copy of a compatible ActionBarSherlock in `external/`, and the 
project files are set up to reference that copy. If you import it first, your
imports of other sample apps should go more smoothly. Alternatively, you 
can download and set up ActionBarSherlock yourself in your Eclipse workspace,
then go into Project Properties and point the
book's project to use your copy of the ActionBarSherlock library project.

- Many of the book samples, and ActionBarSherlock, require your Java compiler
compliance level to be set to 1.6, so code can use the `@Override` annotation
on interface method implementations. You can find this in Project Properties,
in the Java Compiler area.

- Restarting Eclipse, for whatever reason, can clear up some undefined problems
indicated by red exclamation marks over the project name in the Project Explorer.

