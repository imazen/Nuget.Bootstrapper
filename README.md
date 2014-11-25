# Nuget.Bootstrapper

Updated bootstrapper for NuGet.

NuGet's currently published bootstrapper has several bugs, including incorrect exit codes (which prevents correct build scripts).

This code is based on the snapshot of the [official NuGet project](https://nuget.codeplex.com/) at cccef98651a7c284f5061777f5bb2f73f8c0cc1d, before the Bootstrapper was deleted.

Many of the bugs were fixed, but the [codeplex release was never updated](https://nuget.codeplex.com/releases/view/58939) (for unknown reasons).


Bugs reported on CodePlex

* Exit code is always 0 [likely fixed]- https://nuget.codeplex.com/workitem/3498 and https://nuget.codeplex.com/workitem/3907
* Bootstrapper doesn't work behind proxy [likely fixed] - https://nuget.codeplex.com/workitem/1866
* Cryptic error message - https://nuget.codeplex.com/workitem/2398
* Corrupted cached nuget.exe will break bootstrapper - https://nuget.codeplex.com/workitem/2348
* Version number incorrect - https://nuget.codeplex.com/workitem/2355
