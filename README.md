This is an example iOS app to demonstrate what a mocl application looks like. It is a simple contact list satisfying the CRUD basics (create, read, update, delete).

Note: mocl is required to build this application. It cannot run on its own. But, you can still see what the code looks like without it.

The application works as follows:
* Zach Beane's vecto (actually the Wukix fork) renders the contact list itself, as well as the detail view of each contact.
* The UI navigation and edit form layout is defined using Xcode's Interface Builder.
* Lisp is used to manage the contact data (sorting the list, reader/printer for storage persistence, etc.).

Step by step to run the example:

Part I: run mocl to deal with the app.lisp
- Install the dependence libs
  - cd into the mocl/systems/   
  ```cd ~/mocl/systems```
  - get all require libs
  ``` 
  $ cd mocl/systems
  $ git clone https://github.com/xach/vectometry.git
  $ ln -s vectometry/vectometry.asd vectometry.asd
  $ git clone https://github.com/xach/geometry.git
  $ ln -s geometry/geometry.asd geometry.asd
  $ git clone https://github.com/Wukix/vecto.git
  $ ln -s vecto/vecto.asd vecto.asd
  $ git clone https://github.com/xach/zpb-ttf.git
  $ ln -s zpb-ttf/zpb-ttf.asd zpb-ttf.asd
  $ git clone https://github.com/xach/zpng.git
  $ ln -s zpng/zpng.asd zpng.asd
  $ git clone https://github.com/xach/salza2.git
  $ ln -s salza2/salza2.asd salza2.asd
  $ git clone https://github.com/fjolliton/cl-vectors.git
  $ ln -s cl-vectors/cl-vectors.asd cl-vectors.asd
  $ ln -s cl-vectors/cl-paths.asd cl-paths.asd
  $ ln -s cl-vectors/cl-aa.asd cl-aa.asd
  ```
- use mocl to deal with the app.lisp    
 ```
 $ mocl -ios LispContacts app.lisp 
 ```
 
Part II: run Xcode to deal with the project
- add the directory mocl to project
- build it!

Video (from [mocl ECLM 2013 presentation](http://i.wukix.com/mocl_eclm2013.pdf)):
* Navigation: http://i.wukix.com/contacts_navigation.m4v
* Scrolling: http://i.wukix.com/contacts_scrolling.m4v
* Rotation: http://i.wukix.com/contacts_rotation.m4v
 
There is also an Android version which uses the exact same app.lisp file: https://github.com/Wukix/mocl-example-lisp-contacts-android
