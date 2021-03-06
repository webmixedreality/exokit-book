# Dev Tasks

## How do I test local changes to the Exokit audio subsystem?

* clone [https://github.com/webmixedreality/exokit](https://github.com/webmixedreality/exokit)
  * `cd exokit && yarn && cd ..`
* clone [https://github.com/modulesio/LabSound](https://github.com/modulesio/LabSound)

The rest of the guide is partitioned into OS-specific sections.

### Windows

* Open the Visual C++ 2015 MSBuild Command Prompt. \(This was installed along with [windows-build-tools](https://www.npmjs.com/package/windows-build-tools).\)

![](.gitbook/assets/image.png)

* Navigate to `LabSound\labsound` and run `build-windows.cmd` 
* Copy `LabSound\labsound\build\x64\Release\LabSound.lib` to `exokit\node_modules\native-audio-deps\lib\windows\LabSound.lib`
* `cd exokit`and then `npm i`
* Repeat this process to test local changes to LabSound.

