# libpd4unity-starter
Starter Unity project with example bouncing ball and accompanying PureData syntehsis

This repository uses (libpd4unity)[https://github.com/patricksebastien/libpd4unity] which relies on the wonderful (libpd)[https://github.com/libpd] itself.  All dependencies are included in the project for ease of use.  This also means that any updates to libpd or libpd4unity will not be kept uptodate here.

This unity project has been tested on Unity 5.4.1f1, with patches made with (Pd Vanilla 0.47-1)[http://msp.ucsd.edu/software.html] on OS X El Capitan 10.11.5 (15F34).  The sample project is also tested for an Android build, on an LG Lexus 5X running Android 7.0.

## Instructions
The project contains one scene called "AScene". Said scene contains the following game objects:

1. Main Camera: Nothing special 
2. Directional Light: Nothing special
3. LibPd: an ampty game object with an "AudioListner" attached, that points to the Pd patch called "bouncingBallSound.pd"
  * Pd patches must be placed in Assets/StreamingAssets/PdAssets
4. A Plane: has a Mesh Collider
5. A Sphere: has several things attached:
  * A Sphere Collider: Note the Physic Material called "Bouncy" that keeps the ball bouncing
  * A Rigid Body: Gives us the sphere's velocity
  * A script called "BounceToPd.cs": sends messages to P dfor the sonification

