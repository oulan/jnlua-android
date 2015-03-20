At [PlayScape](http://www.playscape.com) we needed lua scripting up and running on android over jni.
jnlua project seemed great, but it didn't support android out of the box.
We took the jnlua code as code base and ported it to android.

This is the result, I hope you'll find it useful.


---


jnlua 0.9.6 is used as an android library.
I've included a sample demo app as well.

I also plan to port jnlua 1.x (lua 5.2.x) so watch for updates.


---


## Project structure ##

**jnlua-android-0.9.6a this is an android library** jnlua-android-testapp this is a simple example app that runs a script using the library


## Notes ##

This release is based on jnlua-0.9.6 and lua 5.1.5 sources

1. Lua sources were modified so that output will go to android log instead
> of stdout.
2. jnlua.c was modified so that it won't use global weak references due to
> the behaviour of dalvik in android < 4.x where it immediately releases weak
> referneces.
3. Support for using java from lua was removed.


## Requirements ##

# You can import the projects from Eclipse by going to File>Import and choosing Existing Projects (NOT Existing Android Projects)
# Tested on android >= 2.2
# You need to have ndk, get it from android developers site (google it) I've included an ndk builder configuration in the Eclipse projects which will compile jnlua native libs for armv7,armv6 and intel x86.

Cheers, Max Raskin.