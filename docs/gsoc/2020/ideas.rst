.. _ideas:

Ideas List
=====================


This year we plan to apply to Google Summer of Code. Currently we are looking for project ideas. If you are a student, you are welcome to explore existing project ideas towards the GSoC application phase. There are ways to reach out to mentors, and many projects have lists of newcomer friendly issues you can start from. Students are also welcome to propose their own project ideas.

Propose Project
---------------
If you have a project idea, edit the "Project Ideas" section below by filling the required details and sending a pull request (this page is editable at  https://github.com/synfig/synfig-docs-dev/blob/master/docs/gsoc/2020/ideas.rst), even if you could not mentor (we will find a mentor).

**Required information for project proposal**

::

    A descriptive title
    ~~~~~~~~~~~~~~~~~~~
    **- Description**

    A brief description about the project

    **- Expected Results**

    What benefit this deliver?

    **- Difficulty** Easy | Medium | High

    **- Skills required*** Knowledge Prerequisite

    **- Mentor(s)** Put your name if you are willing to mentor + other mentors.

*Please mention the following as comment on your proposal pr*

:Your name: :)
:Your profile: github | linkedin | etc 
:Your role: I am a making this proposal as a <student | mentor | community member | contributor | etc>

Projects Ideas
--------------

Improvements for Lottie exporter plugin
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**- Description**

This project will improve plugin which helps to export animation for web through Lottie export format (http://airbnb.io/lottie/). See this page for details - https://forums.synfig.org/t/google-summer-of-code-2020/10545/4?u=anishg

**- Expected Results**

This will allow users to export animations which use advanced features of Synfig, such as advanced outline layer, convert methods etc.

**- Difficulty** Medium

**- Skills required** C++, Python

**- Mentor(s)** Anish Gulati (https://github.com/AnishGG)


Skeleton Tool
~~~~~~~~~~~~~

**- Description**

Currently the skeleton is created by adding a Skeleton Layer (via "Layer"->"New Layer"->"Other"->"Skeleton") and adding bones one-by-one through context menu. This is tedious and non-intuitive. It would be better to construct Skeleton in the same way as we can construct splines (using Spline Tool). So the proposal is to add Skeleton Tool, which allows user to "draw" bones and set their parent-child relationships.

**- Expected Results**

Simpler and faster Skeleton construction. Creating bones will be intuitively visible for new users (exposed as tool in Toolbox).

**- Difficulty** Medium

**- Skills required** C++, GTKmm

**- Mentor(s)** Konstantin Dmitriev (https://github.com/morevnaproject)


Simplify building process by utilizing Conan C++ package manager
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

**- Description**

Integrate Conan C/C++ package manager (https://conan.io/) to provide all required dependencies for building Synfig on any platform. See this page for details - https://github.com/synfig/synfig/issues/666

**- Expected Results**

Developers can easily set up build environment on any platform and any toolchain.

**- Difficulty** Easy

**- Skills required** CMake, Autotools, MSYS2

**- Mentor(s)** Konstantin Dmitriev (https://github.com/morevnaproject)


CMake build system
~~~~~~~~~~~~~~~~~~~~

**- Description**

Current implementation of CMake build scripts is not full. Synfig builded by CMake still can be run by using some hacks.
The task is to complete CMake build system scripts and fix some parts of Synfig code (mainly image and library search algorithms)

**- Expected Results**

Synfig can be built using CMake. Installers can be built using CMake (CPack).

**- Difficulty** Medium

**- Skills required** CMake, C++

**- Mentor(s)** Artem Konoplin (https://github.com/ice0)


Text Layer rewrite
~~~~~~~~~~~~~~~~~~~~

**- Description**

Current implementation of Text Layer uses old rendering engine, which makes it really slow. The task is to rewrite the Text Tool for new rendering engine, with consideration of solving its current issues - https://github.com/synfig/synfig/labels/Text

**- Expected Results**

A usable Text Tool in Synfig.

**- Difficulty** High

**- Skills required** C++, Freetype

**- Mentor(s)** Artem Konoplin (https://github.com/ice0)


Replacement of deprecated Gtk classes
~~~~~~~~~~~~~~~~~~~
**- Description**

- get rid of deprecated Gtk::StockId (since before 2013)
- convert deprecated Gtk::Action to Gio::Action (since 2016)
- convert/get rid of deprecated Gtk::UIManager to Gtk::Builder (since 2013)
- (possibly) convert deprecated Gtk::Main 2 to Gtk::Application (since 2012)

**- Expected Results**

Let Synfig Studio code avoid unmantained code, as they can led to stability and security issues.
Besides, it will ease porting of Synfig Studio to upcoming Gtk 4, that deletes all currently deprecated classes and methods.

**- Difficulty** Easy

**- Skills required*** C++, Gtkmm

**- Mentor(s)** Rodolfo Ribeiro Gomes (https://github.com/rodolforg)

Contacts
--------

https://www.synfig.org/contact/
