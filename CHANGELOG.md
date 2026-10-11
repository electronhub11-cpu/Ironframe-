# Changelog

## v0.1.0 — prototype baseline

- Added modular blockout construction UI, simplified differential-track driving, gun aiming, pooled kinetic projectiles, basic armor/damage, one AI target and three prototype modes.
- Added direct IPv4 host/join multiplayer using a simple UDP protocol (up to four human tanks including host); requires physical LAN/hotspot testing.
- Fixed an empty startup scene/Build Settings gap by committing the bootstrap scene and registering it for builds.
- Added an Android manifest for LAN networking and landscape orientation.
- Updated CI baseline to Unity 6.3 LTS, URP 17.3.0 and Android target API 36.
- Added GameCI signed APK/AAB builds, SHA-256 output and automatically versioned GitHub Releases.
- Deferred advanced crew interiors, seat possession, realistic multi-shell ballistics, online Relay matchmaking and real-device profiler evidence.

## Validation status

The repository/source ZIP has only received static checks in this environment. Unity import/compile, APK/AAB build/signing, physical installation, LAN multiplayer and Snapdragon profiling remain unverified.
