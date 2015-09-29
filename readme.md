## Usage

The NuGet package installs a custom MSBuild target into the project that will use `nuget pack` to pack the project output to a NuGet package.  The custom target file also contains a conditional push task to publish the package to [nuget.org](https://www.nuget.org/) or a custom repository.  To publish the package after build, invoke MSBuild with the following properties:

`NuGetPush=true`

`NuGetPushApiToken=[API Key]`

`NuGetPushSource=[URL to repository]`

`NugetPushOptions=[Additional options to pass to nuget.exe]`



**Example**

Publish to [nuget.org](https://www.nuget.org/):

`msbuild /p:NuGetPush=true /p:NuGetPushApiToken=MyApiToken`

Publish to private repository:

`msbuild /p:NuGetPush=true /p:NuGetPushApiToken=MyApiToken /p:NuGetPushSource:\\My\private\repository`

## Install

Install from [https://www.nuget.org/packages/Robusto](https://www.nuget.org/packages/Robusto)
