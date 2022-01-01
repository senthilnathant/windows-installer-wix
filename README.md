# windows-installer-wix

This repository contains source code for Windows Installer built with WiX ToolSet.

a. 	Pre-requisites:
--------------------

1. Visual Studio 2019 or 2022 - C# .Net Framework 4.7.2 or above

2. 	Wix Toolset 3.11
	https://wixtoolset.org/releases/

3. 	Visual Studio 2019 Wix Toolset Extenstion
	https://marketplace.visualstudio.com/items?itemName=WixToolset.WixToolsetVisualStudio2019Extension
	
4. 	If you use Visual Studio 2022, then you need Visual Studio 2022 Wix Toolset Extenstion
	https://marketplace.visualstudio.com/items?itemName=WixToolset.WixToolsetVisualStudio2022Extension
	

b.	Code compilation:
----------------------
	
1.	Build the application - HelloWorld.exe

	This is a C# Winforms application project - just a demo app that displays a Hello World! text when runs.
	Open the HelloWorld.sln found in HelloWorld_WixInstaller_Demo\HelloWorld folder,
	clean build it, the output file HelloWorld.exe will be copied to HelloWorld_WixInstaller_Demo\HelloWorld_WixInstaller\source
	
2.	Build the MSI Installer - HelloWorld_WixInstaller.msi

	Open the HelloWorld_WixInstaller.sln found in HelloWorld_WixInstaller_Demo\HelloWorld_WixInstaller folder,
	clean build it, the output file HelloWorld_WixInstaller.msi and be found in \bin\Release or \bin\Debug based on your build selection.
	
	The repository has an output file HelloWorld_WixInstaller.msi at the folder HelloWorld_WixInstaller_Demo\HelloWorld_WixInstaller\output
	This is signed by my individual code signing certificate, just to prove its origin.

	This is the MSI Installer file project, a Wix Toolset project. The output of this prohect build is the HelloWorld_WixInstaller.msi file.
	When it is run, it opens the MSI installer dialog and you proceed with the installation. 
	This is a 32 bit installer package that installs the HelloWorld.exe program to 
	"Program Files (x86)\HelloWorld WixInstaller Demo" on 64 bit machine and 
	"Program Files\HelloWorld WixInstaller Demo" on 32 bit machine and adds the Hello World WixInstaller Demo 
	entry to Programs and Features section (Add or remove programs) of Control Panel for later uninstallation.
	

