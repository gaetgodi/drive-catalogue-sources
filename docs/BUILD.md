# Third-party build and library replacement information

Status: retained supplier build evidence, with remaining completeness checks. No builds or application tests were performed. See [Slim r5 review](SLIM-R5-REVIEW.md) and [source inventory](SOURCE-AVAILABILITY.md). Distribution clearance remains pending.

## Retained evidence

- **JQt 2.6.4:** source commit `3827c94935ef0dd3d8680032649db9fca767685a`; official successful build run `25791603866`, Windows job `75758339458`. Windows MSVC2022 and Qt 6.10.3 `win64_msvc2022_64`; retained command: `script/makewin.cmd x64 6.10.3`. The source archive includes its build scripts. Preserve its LGPL-2.1 text, Qt header exception and incorporated QXlsx notices; the header exception is not a general waiver of LGPL duties.
- **Qt 6.10.3:** complete official upstream source archive and matching SDK WebEngine SPDX evidence are retained. The exact SDK WebEngine DLL matches the shipped DLL. Obtain/identify the applicable configure/CMake feature settings, build-control scripts, tool versions and any vendor changes required for the actual distributed Qt build; the short companion build summary alone does not establish all of these.
- **FFmpeg 7.1.3:** complete upstream source and DLL-reported configuration are retained. Full flags are in companion `release-evidence/runtime-provenance/runtime-versions.json` and r5 `RUNTIME_COMPONENTS.json`. Recorded options include `--toolchain=msvc --enable-shared --disable-static --enable-zlib`, with Windows zlib-1.3.1 paths. Record the complete build-control recipe, dependency provenance and patches/no-patches evidence; flags alone are not all corresponding source.
- **MPIR:** stock 3.0.0 sources are reference only. The original DLL's build.vc16/Core2 recipe, source revision and patches remain unresolved. No rebuild recipe for that DLL is claimed.
- **J engine:** commercial-marked supplied binary; no assertion that a generic GPL J source checkout establishes its license or build correspondence.

These records are build evidence, not a promise of bit-for-bit reproducibility. Required source/build supplements must be identified and supplied before declaring delivery complete.

## Replacement procedure for the shared-library route

1. Keep a backup of the accepted portable folder and close all running J/Drive Catalogue processes.
2. Build an x64, interface-compatible replacement using the relevant source and build controls. Preserve the library's required exported interfaces and compatible dependent libraries; a different major Qt/FFmpeg ABI is not automatically compatible.
3. In a separate recipient-controlled copy, replace the relevant libraries under `runtime/j/bin`: JQt `jqt.dll`, the applicable `Qt6*.dll` files, or FFmpeg `avcodec-61.dll`, `avformat-61.dll`, `avutil-59.dll`, `swresample-5.dll`, `swscale-8.dll`. Keep related plugins/resources consistent with the replacement build.
4. Launch through the ordinary launcher in that copy. Archive hashes identify the accepted distribution; existing review records say launch does not require the original LGPL DLL hashes. Keep normal architecture/interface prerequisite checks. No signing key or distributor unlock is documented.
5. Consult r5's `RUNTIME_COMPATIBILITY.md` for application interfaces and dependencies. Owner support/acceptance of modified binaries is not promised.

This describes recipient replacement, not an instruction to alter the owner's accepted application. Confirm the suitable shared-library mechanism under the applicable license; a blanket demand for application object files is not justified solely by dynamic linking. MPIR replacement additionally requires compatible exports and resolution of J's LGPL debugging-permission scope. Owner terms cannot override that supplier restriction.
