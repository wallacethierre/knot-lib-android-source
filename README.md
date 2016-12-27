## Using Android library directly
1. In module app file include instruction
>
```
   dependencies {
       ...
       compile 'com.github.cesarbr:knot-lib-android-sourc:KNOT-v01.00'
       ...
   }


```
>


                                    ##OR


## Generated .aar file of knot_lib

1. In root directory project run command: **./gradlew clean aR** to generated this file.
   file is generated in a folder: root_project/androidlibrary/build/outputs/aar/

## Using Android library

1. Add file created with command above in libs folder.

   *Important: if not seen libs folder, change AndroidStudio perspective to Project.
      
2. Change allprojects attribute in project gradle to:
>
```
    allprojects {
        repositories {
              jcenter()
              flatDir {
                 dirs 'libs'
              }
          }
    }
```
>

3. In Module: app add the following command:
>
```
  compile(name:'knot-android-library-release', ext:'aar')
```
>
