# Template_SFML_x64_Project

This project was originally built using Visual C++20 in Visual Studio 2022 and uses the Visual C++17 64-bit version of SFML 2.6.1. Please ensure you have a 64-bit compatible system before attempting to compile and run this application.
In order to compile the code locally and run it using Visual Studio, you should follow the instructions below, ensuring that software versions match where possible to avoid any unwanted errors.

 - [Download](https://visualstudio.microsoft.com/vs/) and Install Visual Studio 2022.
 - Clone or Download and Extract this repository to an appropriate directory on your local machine. You should end up with a folder called ``Template_SFML_x64_Project``.
   - Note: If you Download this project rather than Cloning it, you may find that after extracting the files from the ``.zip`` folder, there is a second folder called ``Template_SFML_x64_Project`` within the first one. It is this inner folder you want -- move the inner folder to your desired directory and delete the (now empty) outer folder.
 - [Download SFML](https://www.sfml-dev.org/download/sfml/2.6.1/). You will need the Visual C++17 (2022) 64-bit version of SFML 2.6.1.
 - Extract the SFML files from the ``.zip`` folder you just downloaded.
 - Inside the ``SFML-2.6.1-windows-vc17-64-bit`` folder you will find a folder named ``SFML-2.6.1``. Move this ``SFML-2.6.1`` folder to the same directory as the ``Template_SFML_x64_Project`` folder you obtained earlier, but NOT inside the ``Template_SFML_x64_Project`` folder itself.
 - Rename ``SFML-2.6.1`` to ``SFML_x64.``

Your final folder hierarchy should look like

 - CHOSEN_DIRECTORY
   - ``Template_SFML_x64_Project``
     - PROJECT_FILES
   - ``SFML_x64``
     - FILES FROM ``SFML-2.6.1``

If so then that's it, you're good to go! 

The build options you will need to use are ``x64`` and ``Debug`` in order for the code to compile correctly. Also ensure that your C++ Language Standard (found under ``Project > Project Properties > Configuration Properties > General > General Properties`` in Visual Studio) is set to ``ISO C++20 Standard (/std:c++20)``.
The linker and compiler, along with the above build options and standards, should be set up appropriately by default due to the .vcxproj file included in this repository, however if Visual Studio fails to read this file for any reason, you may have to alter these settings manually. 
If you need to change the linker and compiler settings manually, I recommend following the ``Setting up SFML`` chapter of John Horton's book [Beginning C++ Game Programming](https://subscription.packtpub.com/search?query=beginning%20c%2020%20game%20programming).

Note that the .dll files included in this repository also need to be copied into the folder where the executable is generated in order for the executable to run. This is usually x64 > Debug.
