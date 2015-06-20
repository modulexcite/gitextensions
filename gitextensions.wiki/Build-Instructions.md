## How to build and test in VS2010 and VS2012
Download and install WiX Toolset from <http://wixtoolset.org/>

Synchronize and update all submodules using GitExtensions.

If you have never set up NuGet, open Visual Studio, and go to Tools > Options. Select "NuGet Package Manager". Be sure "Allow NuGet to download missing packages" and "Automatically check for missing packages during build" are checked.

Open GitExtensions.VS2010.sln, GitExtensions.VS2012.sln, or GitExtensions.VS2013.sln.

Push F5 to build and run GitExtensions project.

Note that this may not work with Express versions of Visual Studio. See [issue #1785](https://github.com/gitextensions/gitextensions/issues/1785#issuecomment-15876302) for more info.

### Building the installer
 * VS2012: Run <GitExtensions>\Setup\BuildInstallers.VS2012.cmd

 * VS2013: Run <GitExtensions>\Setup\BuildInstallers.VS2013.cmd

 * Mono: Run <GitExtensions>\Setup\BuildInstallers.Mono.cmd

### Running tests
You should use VS Professional or better for running tests. Ctrl+R, A to run all tests in solution.

## How to build and test in Mono
Mono 2.10 or better required, because it use by default C# 4.0 compiler.

Note that it will not build out of the box with Mono on Linux. There is a laundry list of other things that you also need to install/do. Someone really needs to document the **complete and detailed** set of steps for this, because the information currently provided here is not nearly sufficient.

If you use old Mono:
> Use xbuild. By default, MonoDevelop (and most mono devs) will use mcs but this is being overtaken by xbuild which is the Mono version of msbuild. It is the future of mono compilation. The mcs compiler may not build or link the assemblies properly and xbuild does a good job of this. If you are having linking or build errors that aren't related to the code itself, try building the solution with xbuild.

## Images and linux compatibility
Not all image formats are supported on mono. Png images with a color depth of 48bpp will cause compiler errors. If you run into this problem you should convert all png images to 8bpp.

This can be done using the following Linux commands:
<pre>
sudo apt-get intall imagemagic
mogrify -depth 8 $(find -iname '*.png')
mogrify -depth 8 $(find -iname '*.PNG')
</pre>

### Running tests
Tests use NUnit under Mono.