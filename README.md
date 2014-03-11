ImageProcessor
===============

Imageprocessor is a lightweight library written in C# that allows you to manipulate images on-the-fly using .NET 4.0.

It's fast, extensible, easy to use, comes bundled with some great features and is fully open source.

For full documentation please see [http://jimbobsquarepants.github.io/ImageProcessor/](http://jimbobsquarepants.github.io/ImageProcessor/)


Exponent Cropup (EC)
====================
Is an package for Umbraco which - and this might come as a surprise - crops images!
http://our.umbraco.org/projects/website-utilities/eksponent-cropup.

EC uses a separate json file to hold all metadata for each image. This file is updated when any change to any crop's are made.

Imageprocessor can cache all files processed. All remote files are "hard cached" and only refreshed when cache times out.

This little hack allows Imageprocessor to tests if json file is changed and clears cache if needed. The basic idea is this: If image path contains /cropup/ then check if json file is updated. Thats it.

Url example. 

img src="/remote.axd?http://hostname/cropup/banner/media/1014/someimagefile.jpg?preset=anypresetyoumighthave"
