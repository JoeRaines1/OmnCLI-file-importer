This is a script that was intended to run as a cron job and would automatically upload any files from the user's local machine into an instance of Nvidia's Omniverse Nucleus, Omniverse's file system.

Installation Guide
1.	Download Omniverse from: https://www.nvidia.com/en-us/omniverse/download/ or on a Linux system wget https://install.launcher.omniverse.nvidia.com/installers/omniverse-launcher-linux.AppImage 
2.	Once the Omniverse Launcher is installed, navigate to the exchange tab and search for ‘connect sample omniverse connector’ and install it.
3.	If the file importer is being run on Ubuntu 20.4 or earlier a newer version of glibc will have to be installed so Omnicli can run. To install a new version without interfering with the operating system follow the steps in the following link. https://install.launcher.omniverse.nvidia.com/installers/omniverse-launcher-linux.AppImage . After installing the new glibc version ./build.sh must be rerun to recompile Omnicli. Once the build.sh file has been rerun Omnicli should be working properly.
4.	Before the file importer can be run 5 environmental variables must be created.
    •	PDB_FILES: the path to folder containing the .pdb files that are going to be uploaded to Omniverse

    •	PATH_TO_OMNI_CLI: the path to the location of the omnicli file

    •	PATH_TO_OMNIVERSE_PDB: the path to the folder in Omniverse where the .pdb files are going to be stored

    •	OMNIVERSE_USERNAME: a valid username that can be used to login to the Omniverse server

    •	OMNIVERSE_PASSWORD: the password for logging in to the Omniverse server

5.	After creating the environment variables omni_cli_importer.py can be run.
