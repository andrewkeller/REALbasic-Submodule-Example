This is a relatively blank REALbasic project.

The purpose of this project is to show a possible implementation of a shared common library.  The REALbasic Common KFS BSD library is used as an example here.

To clone this project, perform the following actions:

  git clone git://github.com/andrewkeller/REALbasic-Submodule-Example.git
  cd REALbasic-Submodule-Example
  git submodule init
  git submodule update

After that, you can poke around the project all you want.  The most important thing to notice is:

  If you modify some code in the common library, the change is physically stored only in the submodule, whereas if you modify some code in the parent project, the change is stored in the parent repository only.

The following is how you would pull in new changes to the library in this scenario:

1) Open the RB Project.
2) Delete the library.
3) Run `git fetch` in the library.
4) Run `git checkout origin/master` in the library.
     - This is assuming you do not have any changes in the library you want to keep, and that you only want to update to the current commit of origin/master.
     - If you have changes, you can blow them away before you run the checkout with `git reset --hard HEAD` and `git clean -fd`.
5) Open up the project in the library, and copy and paste the library items from the library's IDE to your project's IDE.
6) Commit the changes.  You should have changes in the .submodules file, and the project.rbvcp file.
