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
* Provide some commonly needed Telnet helper definitions (such as `TelnetCommandByte` constants).

## Possible Goals
* We may decide to house some common Telnet options negotiations logic here, as Telnet options state machines can also be a bit fiddly and valuable to abstract. While we would not want every option under the sun explicitly defined here, we could build it to be extensible without requiring the user to know the ins and outs of these state machines.

## Non-Goals
* Does not apply implementation-specific ideas about how input data gets handled. (Data remains bytes, not culled to strings.)
* Does not discriminate between character-at-a-time mode or line mode, or other protocol specifics. (Tries to work with any clients or servers instead of ruling out options at this level.)
* Does not apply other application-specific rules for you. (Things like deciding to automatically disconnect long-inactive connections are per-application choices.)

## Development Guide
To keep this README short and shared with NuGet, see the [Development Guide](https://github.com/DavidRieman/WheelTelnet/docs/DevGuide.md) for further details to getting started.
