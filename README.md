Mobile Studio Package
======================

This project is a Unity package for integrating the Mobile Studio tool suite
into game development workflows. This version of the package has the following
features for integrating with the Streamline profiler.

* C# language bindings for emitting event annotations.
* C# language bindings for emitting software counters.

License
=======

Most files in this library are licensed under the BSD-3 Clause License,
provided in [LICENSE.md](LICENSE.md).

The Unity native plugin interface header, `IUnityInterface.h`, is licensed
under the Unity Companion License, provided in
[LICENSE_UNITY.md](LICENSE_UNITY.md).

Technical details
=================

Requirements
------------

This version of the package is compatible with the Unity Editor version 2020.3
LTS and later.

Building
--------

This package is built using the Unity bee compiler.

1) Set the environment variable `ANDROID_NDK_ROOT`
   to a local Android NDK install. Android NDK can usually be found in:
   `\Editor\Data\PlaybackEngines\AndroidPlayer\NDK`
2) Locate the bee compiler in your Unity install. It is usually found in:
   `\Editor\Data\il2cpp\build\BeeSettings\offline\bee.exe`
3) To trigger a build, run `bee.exe` in the `Native~` directory.

Compatibility
-------------

This package uses application-generated Streamline annotations to add more
context to captured data. It allocates annotation handles in the ID range 16384-32767; other users of Streamline in the same process should avoid using
this range to avoid collisions.

Installing and using
--------------------

For instructions on how to install and use this package, see the
[full documentation page](Documentation/Mobile-Studio.md).



