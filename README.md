# Nuget.Bootstrapper

[![Build status](https://ci.appveyor.com/api/projects/status/sd0yxwm05ebj8d27?svg=true)](https://ci.appveyor.com/project/imazen/nuget-bootstrapper)

Updated bootstrapper for NuGet. You can download the [latest .exe from AppVeyor](https://ci.appveyor.com/project/imazen/nuget-bootstrapper/build/artifacts).

NuGet's currently published bootstrapper has several bugs, including incorrect exit codes (which prevents correct build scripts).

This code is based on the snapshot of the [official NuGet project](https://nuget.codeplex.com/) at cccef98651a7c284f5061777f5bb2f73f8c0cc1d, before the Bootstrapper was deleted.

Many of the bugs were fixed, but the [codeplex release was never updated](https://nuget.codeplex.com/releases/view/58939) (for unknown reasons).


Bugs reported on CodePlex. We need to write integration tests for these.

* Exit code is always 0 [likely fixed]- https://nuget.codeplex.com/workitem/3498 and https://nuget.codeplex.com/workitem/3907
* Bootstrapper doesn't work behind proxy [likely fixed] - https://nuget.codeplex.com/workitem/1866
* Cryptic error message - https://nuget.codeplex.com/workitem/2398
* Corrupted cached nuget.exe will break bootstrapper - https://nuget.codeplex.com/workitem/2348
* Version number incorrect - https://nuget.codeplex.com/workitem/2355

* nuget.exe update -self may have a bug. It always renames the running .exe to .old.exe, but what if .old.exe already exists? We may be able to delete .old.exe to reduce the frequency of this bug.
