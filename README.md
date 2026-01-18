WheelTelnet
===========
A minimal C# Telnet library.

## Overview
WheelTelnet is a highly-reusable Telnet implementation.
It was initially built for [WheelMUD](https://github.com/DavidRieman/WheelMUD), then rebuilt as a separate library to strengthen separation of concerns and provide value to new usage cases.

## Goals
* Provide an easy-to-use abstraction over Socket, dealing with a lot of the fiddly stumbling blocks automatically.
* Provide tracking of Telnet connections.
* Provide notifications of state changes (like new connections and disconnections) through events.
* Provide useful functionality whether you are building a Telnet client, server, or true bi-directional experience. (Currently, server mode is the most featured and best tested mode.)

## Possible Goals
* We may decide to house some common Telnet options negotiations logic here, as Telnet options state machines can also be a bit fiddly and valuable to abstract. While we would not want every option under the sun explicitly defined here, we could build it to be extensible without requiring the user to know the ins and outs of these state machines.

## Non-Goals
* Does not apply implementation-specific ideas about how input data gets handled. (Data remains bytes, not culled to strings.)
* Does not discriminate between character-at-a-time mode or line mode, or other protocol specifics. (Tries to work with any clients or servers instead of ruling out options at this level.)
* Does not apply other application-specific rules for you. (Things like deciding to automatically disconnect long-inactive connections are per-application choices.)

## Development and Testing
You will find the solution in the `src`. This will have both the `WheelTelnet` library and the `Demo` application which can be used to test the library. When running any other application using the WheelTelnet library (including the Demo app) on Windows, Windows Security will ask if you want to allow public and private networks access to this app. Given that this is the whole point of the library, you will want to give at least Private networks access. (You may also want to consider giving Public networks access, if you are working on a portable device like a laptop. Especially if you feel it likely that you may want to collaboratively test your application on a public wi-fi some day. It is not obvious how to fix the Windows per-app setting later without doing some research, and Windows will just block the traffic silently and it won't be clear why the app decided not to work in that future situation.)

## NuGet
WheelTelnet will be housed on NuGet. You could also pull the source to be adjacent to the project, and use a relative project reference, if you want direct low level source code insight.

## License
Microsoft Public License (MS-PL). [Read Here](src/LICENSE.txt).
