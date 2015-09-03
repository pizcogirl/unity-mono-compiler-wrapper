# Unity Mono Compiler Wrapper

Updates Unity to use newer Mono compiler. 

Because Unity uses a very old Mono compiler this fixes various problems, like:
* Not compiling perfectly valid C# code.
* Generating invalid IL (http://forum.unity3d.com/threads/compiling-errors.319958/ - as far as we know this is related to nested classes).
* Not being to use C# 6 - yay!

## Setting up

### Instructions
- Install [latest mono](http://www.mono-project.com/download/).
- Either:
 - Install [UnityVS](http://unityvs.com/) & get Unity SDK files from `C:\Program Files (x86)\Reference Assemblies\Microsoft\Framework\.NETFramework\v3.5\Profile\Unity Full v3.5`.
 - Download Unity SDK files from here: [`unityfull.zip`](https://github.com/tinylabproductions/unity-mono-compiler-wrapper/releases/)
- Put Unity SDK files somewhere - the default location is `%UNITY_INSTALL_DIR%\unityfull`.
- Download [`compiler-upgrade.zip`](https://github.com/tinylabproductions/unity-mono-compiler-wrapper/releases/).
- Extract `compiler-upgrade.zip` to `%UNITY_INSTALL_DIR%` overwriting any files.

### Environment variables

You can specify these environment variables to change the behaviour of the wrapper:

* `UNITY_NEW_MONO_SDK` - path to Unity SDK which is used when building (default: `%UNITY_INSTALL_DIR%\unityfull`).
* `UNITY_NEW_MONO` - path to new version of Mono (default: `%ProgramFiles%\Mono\lib\mono\4.5\mcs.exe`).

## Troubleshooting

We have only checked this on Windows & Android. Pull requests are welcome.

Other than that - if you have problems check the log file at `%TEMP%\UnityMonoUpdatedCompilerOutput.txt`

## Original Author

Evaldas Čiakas <evaldas@tinylabproductions.com>
