This is a relatively blank REALbasic project.

The purpose of this project is to show a possible implementation of a shared common library.  The REALbasic Common KFS BSD library is used as an example here.

To clone this project, perform the following actions:

  git clone git://github.com/andrewkeller/REALbasic-Submodule-Example.git
  cd REALbasic-Submodule-Example
  git submodule init
  git submodule update

After that, you can poke around the project all you want.  The most important thing to notice is:

  If you modify some code in the common library, the change is physically stored only in the submodule, whereas if you modify some code in the parent project, the change is stored in the parent repository only.
