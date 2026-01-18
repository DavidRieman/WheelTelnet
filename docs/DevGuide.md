## Development and Testing
You will find the solution in the `src`. This will have both the `WheelTelnet` library and the `Demo` application which can be used to test the library. When running any other application using the WheelTelnet library (including the Demo app) on Windows, Windows Security will ask if you want to allow public and private networks access to this app. Given that this is the whole point of the library, you will want to give at least Private networks access. (You may also want to consider giving Public networks access, if you are working on a portable device like a laptop. Especially if you feel it likely that you may want to collaboratively test your application on a public wi-fi some day. It is not obvious how to fix the Windows per-app setting later without doing some research, and Windows will just block the traffic silently and it won't be clear why the app decided not to work in that future situation.)

## NuGet
WheelTelnet will be housed on NuGet. You could also pull the source to be adjacent to the project, and use a relative project reference, if you want direct low level source code insight.

## License
Microsoft Public License (MS-PL). [Read Here](../src/LICENSE.txt).
