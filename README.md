# CLIPSJNI

This is a fork of https://github.com/gomezgoiri/CLIPSJNI

## A quick overview

### What is this?

This project contains:

* The CLIPSJNI **java library**, useful to create java applications that use CLIPS
* The CLIPSJNI **native library**, which is required to be installed on your system to make the **CLIPSJNI java library** work.

> I renamed the **native library** from CLIPSJNI to CLIPSJNI2 to avoid naming conflicts with the original CLIPSJNI, as someone may want to keep both versions for compatibility with other applications.

### Project directories

* `library-src`: the sources (written in C) of the CLIPSJNI **native library**
* `compiled-library`: some compiled versions of the CLIPSJNI **native library**
* `src`: the sources of the CLIPSJNI **java library**
* `examples`: some examples (you don't say?)

## Configuration

### Install CLIPSJNI native library

Copy CLIPSJNI2 from `compiled-library` (according to your platform), and paste it in a directory of your OS reachable by PATH. 

> CLIPSJNI2 has different names and extensions across different platforms, such as CLIPSJNI2.dll for Windows and libCLIPSJNI2.os for linux

If you can't find your platform in `compiled-library`, you have to compile the CLIPSJNI native library manually (see next section)

#### Compile CLIPSJNI native library (if needed)

If you need to generate the library from scratch, in the `library-src` directory you will find a `README` file which explains how to do it.

> To compile CLIPSJNI2 you must have a jdk installed in your system, with all the environment variables configured correctly.

If you compile CLIPSJNI for a platform which is not present in `compiled-library`, please send me a pull request to include it here, or just let me know [opening an issue](https://github.com/Chosko/CLIPSJNI/issues/new)

### Compile CLIPSJNI java library

To install CLIPSJNI in your Maven local repository, simply run:

    mvn install

This will also generate an OSGi compliant jar in the `target` subfolder that you can use wherever you want.

### Original README

You can find the original README [here](README.old.md)
