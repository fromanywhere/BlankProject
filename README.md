BlankProject
============

Сore files which I use for starting a new project.

Significant feature of my projects is small size and short lifetime of site (usually < 1 year).
So i build compact project skeleton which help me begin to work effectially.

Project structure:

	/ (contain html files)
	|
	|---img (containt project images)
	|---js (contain scripts and libraries)
	|---css (contain style.css)
		|
		|---less (contain style.less and reset.less)
			|
			|---blocks (contain less-modules for independent development)
			

Currently I use LESS for building and merging CSS.
Any LESS app compile my style.less and reset.less in single file. Usually style.less include blocks, which are logically independant.

I use jQuery 1.9.* as base framework, and Modernizr as shim and feature detecting library.