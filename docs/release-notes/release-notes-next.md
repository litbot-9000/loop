# Loop Client Release Notes

#### New Features

#### Breaking Changes

#### Bug Fixes

* Fix a connection ownership bug where an embedded loop daemon closed the
  shared lnd connection on shutdown. When running as a subserver of
  lightning-terminal, a graceful stop or a runtime error in the loop daemon
  tore down the lnd connection owned by the parent process, breaking lnd
  access for LiT and all other integrated subservers. The daemon now tracks
  whether it created the connection itself and only closes owned connections.

#### Maintenance
- Update the LoopRPC requirement to the revision used by this release.

#### Contributors (Alphabetical Order)
