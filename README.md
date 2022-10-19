# Velocity

[![Build Status](https://img.shields.io/jenkins/s/https/ci.velocitypowered.com/job/velocity.svg)](https://ci.velocitypowered.com/job/velocity-3.0.0/)
[![Join our Discord](https://img.shields.io/discord/289587909051416579.svg?logo=discord&label=)](https://discord.gg/papermc)

A Minecraft server proxy with unparalleled server support, scalability,
and flexibility.

Velocity is licensed under the GPLv3 license.

## Goals

* A codebase that is easy to dive into and consistently follows best practices
  for Java projects as much as reasonably possible.
* High performance: handle thousands of players on one proxy.
* A new, refreshing API built from the ground up to be flexible and powerful
  whilst avoiding design mistakes and suboptimal designs from other proxies.
* First-class support for Paper, Sponge, and Forge. (Other implementations
  may work, but we make every endeavor to support these server implementations
  specifically.)
  
## Building

Velocity is built with [Gradle](https://gradle.org). We recommend using the
wrapper script (`./gradlew`) as our CI builds using it.

It is sufficient to run `./gradlew build` to run the full build cycle.

## Running

Once you've built Velocity, you can copy and run the `-all` JAR from
`proxy/build/libs`. Velocity will generate a default configuration file
and you can configure it from there.

Alternatively, you can get the proxy JAR from the [downloads](https://papermc.io/downloads#Velocity)
page.

[//]: # (/*)

[//]: # (* PAPER'S VERSION FOR FIXING IT. MAY NEED TO REVERT LATER.)

[//]: # (*/)

[//]: # (//                  if &#40;playerKey.getKeyRevision&#40;&#41;.compareTo&#40;IdentifiedKey.Revision.LINKED_V2&#41; >= 0&#41; {)

[//]: # (//                    // Bad, very bad.)

[//]: # (//                    logger.fatal&#40;"A plugin tried to change a signed chat message. ")

[//]: # (//                        + "This is no longer possible in 1.19.1 and newer. ")

[//]: # (//                        + "Disconnecting player " + player.getUsername&#40;&#41;&#41;;)

[//]: # (//                    player.disconnect&#40;Component.text&#40;"A proxy plugin caused an illegal protocol state. ")

[//]: # (//                        + "Contact your network administrator."&#41;&#41;;)

[//]: # (//                  } else {)

[//]: # (//                    logger.warn&#40;"A plugin changed a signed chat message. The server may not accept it."&#41;;)

[//]: # (//                    return ChatBuilder.builder&#40;player.getProtocolVersion&#40;&#41;&#41;)

[//]: # (//                        .message&#40;messageNew&#41;.toServer&#40;&#41;;)

[//]: # (//                  })

[//]: # (/*)

[//]: # (* MY VERSION FOR FIXING IT.)

[//]: # (*/)