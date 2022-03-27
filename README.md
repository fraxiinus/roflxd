# roflxd - ROFL eXtract Data

[Discuss roflxd on Discord](https://discord.com/invite/c33Rc5J)

roflxd is an umbrella term used to classify all ROFL parsers written by fraxiinus. The goal is to provide developers will easy to use ROFL parsers in the language they want to use.

(I also find writing ROFL parsers to be a great way to learn a new language. So a lot of roflxd projects will be my first project in a language.)

## Requirements

While roflxd projects might differ wildly from each other, every project must at least be able to:

* Verify the integrity of a ROFL file
* Parse the file to a data structure
* Output the data in a format like JSON (or provide a sample project that does)

## Implementations

| Project | Language  | Notes |
--- | --- | --- |
| [roflxd.go](https://github.com/fraxiinus/roflxd.go) | Golang | The README labels it as "incomplete" but the ROFL parsing works and meets all roflxd requirements. |

## Planned implementations

The following projects are currently planned, or are in progress but not published yet.

| Project | Language  | Notes |
--- | --- | --- |
| roflxd.cs | C# | A completely new, from scratch, C# parser. Created to enhance ReplayBook.

## Incomplete implementations

The following projects were created before roflxd or are missing key features.

| Project | Language  | Notes |
--- | --- | --- |
| [Rofl.Reader (ROFL Player)](https://github.com/fraxiinus/ROFL-Player/tree/master/Rofl.Reader) | C# | My first ever parser, created for [ROFL-Player](https://github.com/fraxiinus/ROFL-Player). Missing the ability to verify data and does not parse player or payload data. However it is capable of reading partial data from LoLReplay replay files (.LRF). Contains incomplete code for reading BaronReplays files (.LPR) |
| [Rofl.Reader (ReplayBook)](https://github.com/fraxiinus/ReplayBook/tree/master/src/Reader) | C# | Updated version used in [ReplayBook](https://github.com/fraxiinus/ReplayBook). Missing the ability to verify data and does not parse payload data. However it parses all player data. Unable to parse anything besides ROFL files. |

## Frequently Asked Questions

### Payload data is being parsed, but why is it unreadable?

Riot Games decided that replay files will just be a dump of the a game's packet data. Packet data is obfuscated in order to deter cheaters.

### Can you write a roflxd implementation in X language?

Maybe.
