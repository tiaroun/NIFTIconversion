# NIFTIconversion.sh

This script iterates through all run folders within a session folder, creates a new folder ("NIFTI") 
for dcm2niix output, then runs the dcm2niix program if there are no nifti files in this subfolder.

NOTE: You will need dcm2niix (https://github.com/rordenlab/dcm2niix/releases) installed on the device you are running this script from, and dcm2niix MUST 
be executable and added to your PATH. Once you install dcm2niix (it will come to you as a shell file), move the
file into a folder called dcm2niix_folder. In Terminal, go to this folder and enter the following line of code

<chmod u+x dcm2niix>


Navigate to your bash profile (this will be a text file that is located under your user folder on your device) and add the following lines to the very end of this file (replace tb3344 with your own user folder name)

PATH="/Users/tb3344/Desktop/dcm2niix_folder:${PATH}"

export PATH


Run this script within the MRI session folder (e.g. R21_EEG-fMRI_001_v2) in Terminal by calling

<bash ~/folder-where-you-have-this-script-downloaded/NIFTIconversion.sh>
