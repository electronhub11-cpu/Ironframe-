# Ironframe Build / Environment Report

Date: 2026-10-11

## Environment
- Unity Editor: not installed / not available on PATH.
- Android SDK/NDK, Gradle, ADB, dotnet, Mono: unavailable on PATH.
- Java and keytool: available. A dedicated Android release keystore was generated and packaged separately.
- GitHub connector: not connected, so no remote repository or release could be created from this session.

## Static validation performed
- Source ZIP integrity verified.
- Unity package manifest JSON and Android manifest XML parse.
- GitHub Actions workflow YAML parses. It defines GameCI APK and AAB builds, archive integrity checks, SHA-256 output, artifact uploads, and automatic versioned GitHub Releases on main/manual/tag runs.
- Startup scene and EditorBuildSettings paths agree; bootstrap script GUID and asset metadata are present.
- All 16 C# files passed a lightweight delimiter scan with no duplicate class names. This is not a C# compiler result.
- Signing keystore was inspected with `keytool`; this does not certify that Unity will use it successfully.

## Not verified
- Unity import/compile or the URP asset setup during a clean cloud build.
- APK/AAB build, signature verification, installation, launch, touch controls, or LAN/hotspot networking.
- FPS, memory, cold start, frame pacing, profiler captures, or performance on Snapdragon 685 / Adreno 610.

## Hard blocker for the requested APK
The current container does not include Unity or the Android build toolchain, and outbound toolchain downloads fail DNS. Therefore no APK or AAB was produced, and there is no APK SHA-256 to report. The source contains the cloud CI pipeline, but it must be published to a GitHub repository and run with authorized Unity-license and Android-signing secrets before a real binary can be produced.

## Delivered archive checksums

These are checksums for the ZIP files only, **not an APK**.

- Source + CI ZIP: `Ironframe-APK-CI-Source.zip`, 61940 bytes, SHA-256 `a452a2d2f3af4e58206250b2575c10e69a5d81ab9ad3c771a6b203ceb3d7c090`
- Private signing kit ZIP: `Ironframe-Signing-Kit.zip`, 6072 bytes, SHA-256 `f16f9bb75146fcdf36c47a050286ebc0623bbf274742b086b060751cdec26cec`
