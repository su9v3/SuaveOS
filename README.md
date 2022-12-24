# **SuaveOS**

This is an operating system created specifically to run live on a USB or similar medium. The idea was to create a system that could automatically set up persistent memory, as well as be low in resource consumption so that it could be run anywhere, and at any time. 

## **Important Basic Information**

1. In the `~/SuaveOS` directory of the operating system, the file `Changes.md` holds information about the customizations and changes made to Debian that makes SuaveOS what it is.

2. `sudo auto-persistence` executes a shell script that automates the process to set up persistent memory with some imput from the user. 

3. `suave` is the default username.

4. Debian `live-build` was the tool used to configure and create the custom build for SuaveOS.

5. This repo contains the config files used to make `live-build` build SuaveOS. A pre-built .iso file of SuaveOS can be found in the **Releases** of this repo.

6. The default username and password of this operating system is "suave" and "live" respectively.

The files in this repo correspond to those of a Debian `live-build` project. This repo is designed such that you can clone it, init a `live-build` project in another directory, replace the files in the `live-build` project directory with the ones in the repo, and then build SuaveOS with `lb-build`.

This project was started on January 22, 2022
