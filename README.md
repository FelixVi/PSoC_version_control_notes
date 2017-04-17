# PSoC_version_control_notes
Notes on what files should be under version control for PSoC projects


Support & Community
Revision Control for PSoC® Creator™ Projects - KBA86358
Last Updated: March 09, 2016
Version: 
*B
Question: 

Which PSoC® Creator™ project files can you place into your source control system? 
Answer: 

​PSoC Creator projects have a well-defined directory structure that makes it easy for you to add "source" files to the source control systems. Place the files in the following directories under revision control. (Note: Italicized text is based on the workspace, project, or user name.)

Project Directory (project_name.cydsn)

    main.c
    cyapicallbacks.h
    project_name.cydwr
    project_name.cyprj
    TopDesign\project_name.cycsh 

Optional Files

These files control the user experience (look and feel, open files in the workspace, and so on) but do not impact the application:

    project_name.cyprj.username
    ..\workspace_name.cywsp
    ..\workspace_name.cywsp.username 

Generated_Source

These files are generated based on the components used in your design and their parameter settings. As a result, you can typically replicate these files using the normal build process. Adding them to your revision control system is optional.

However, there are two exceptions to this rule. If you have made the following changes in your design, add those files to revision control:

    You have added your own code in the merge regions of the generated source files. 
    You have modified the default ARM® linker files (cm3gcc.ld or cm3RealView.scat).

External Source Files

If your project includes source files located outside the directories specified here, add them to your revision control system.

Keil Re-Entrancy File

If your project includes project_name.cyre file, add it to your revision control system. 

Third-Party IDE Files

The following files are created when you export designs to the Keil™ µVision® IDE. You can always replicate these files by re-executing the export function, or you can add them to your revision control system for convenience.

    project_name.uvopt
    project_name.uvproj
    project_name.uvmpw
    project_name_PSoCxlib.uvopt ('x' is 3, 4, or 5 for the PSoC architecture)
    project_name_PSoCxlib.uvproj ('x' is 3, 4, or 5 for the PSoC architecture)
