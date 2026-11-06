# Slim r5 source distribution review

Review date: 2026-11-06. **Distribution licensing clearance remains pending.**
The owner reports Windows 11 VM acceptance of RC5 Slim r5. Functional acceptance is satisfied; it is not licensing clearance. No application was run, rebuilt, retested or modified in this review. The accepted executable ZIP and companion ZIP were read only. No archive was uploaded and no GitHub Release was created.

## Evidence and correspondence

| Artifact | Bytes | SHA-256 |
| --- | ---: | --- |
| DriveCatalogue-RC5-offline-Windows-x64-slim-r5.zip | 145411295 | ad9a6fe98022f4bdd8eb8848a064876cd37bfbeea486b9e7f7d8ab90e587ed6e |
| DriveCatalogue-RC5-offline-Windows-x64-slim-r2-companion-sources.zip | 1351105579 | d99786903c9c23a005f7ea1aa2a8b75679387dc0e4eae53d1bf7580ef9f4b75e |

Both whole-file hashes were recalculated and match the retained checksum files. All 174 runtime files in r5 were hashed and match r5's MANIFEST.json; all 174 runtime hash records also match release-evidence/r1-MANIFEST.json in the companion. This supports reusing the r2-named companion for r5's unchanged third-party runtime, despite later owner-application changes. It does not establish missing supplier source provenance.

The companion contains 2,762 entries. Its four embedded source archive hashes were recalculated and match its manifest; see [source inventory](SOURCE-AVAILABILITY.md). Nested source archives were not rebuilt or exhaustively audited file by file. Retained source/build correspondence evidence was reviewed rather than repeated.

## Satisfied and supported

- Owner functional acceptance of Slim r5 is recorded here. Older ZIP metadata saying VM acceptance is pending is historical; the ZIP remains unchanged.
- Complete official Qt 6.10.3 sources, FFmpeg 7.1.3 sources and pinned JQt sources/build scripts are present.
- Retained JQt evidence identifies commit 3827c94935ef0dd3d8680032649db9fca767685a, official build run 25791603866 / job 75758339458 and MSVC2022/Qt 6.10.3.
- The retained offline review establishes a byte-identical Qt SDK WebEngine DLL, hash c19e263399507aa6fd5608720b4460b7c8cdfa0eb535afcbfdd8d8ba96b1b24a, and matching build-specific SPDX/Chromium attribution. Those records and extracted attribution remain in r5's LICENSES/Qt-WebEngine-SDK. The earlier absence of build-specific Chromium attribution evidence is therefore addressed.
- r5 retains LICENSES/, THIRD_PARTY_NOTICES.txt, LICENSING.md and runtime supplier notices. Its evaluation terms preserve third-party rights and owner-controlled LGPL debugging permissions.
- Separate dynamically loaded libraries and documented replacement paths support the shared-library approach. Source delivery and recipient terms still matter.
- Existing records exclude standalone Microsoft runtime DLLs and use the recipient-installed runtime. No new Microsoft entitlement claim or blocker is introduced.

## Actual unresolved blockers for this exact ZIP

1. **MPIR corresponding source.** The shipped mpir.dll has hash e3ec639894c454c249a03412227c3215e55a422cb677eb9c3c7c7f34f5aeb825. Retained evidence identifies a 2024 Core2 build with a build.vc16 path. Stock MPIR 3.0.0 in the companion is explicitly reference only. Obtain the supplier's actual source revision, patches (or supported confirmation of no patches), generated/configuration inputs and build-control recipe for this DLL, and deliver the required materials. A version string, binary import commit or replacement candidate does not close this gap.
2. **J/LGPL debugging scope.** The shipped commercial-marked J engine's license prohibits reverse engineering. MPIR's LGPLv3 combined-work conditions preserve debugging of library modifications. Obtain an applicable supplier clarification/exception or other documented rights covering this exact engine and combined work. Owner evaluation terms cannot grant Jsoftware's rights. This is a specific unresolved conflict, not a conclusion that J redistribution generally requires payment.

These remain blockers even for private delivery to Chris and Eric. No supplier contact was made. A supplier answer must be retained and assessed, not treated as automatic clearance. Rebuilding or substituting runtimes is outside this assignment.

## Remaining completion work

- **Qt/JQt/FFmpeg source completeness:** retain the positive source/version/build evidence, then close a component-by-component checklist identifying any supplier patches, generated inputs, build/install control scripts and non-system dependencies required for the shipped builds. The current BUILD_INFORMATION.md is a short summary; Qt's exact build configuration and FFmpeg's complete build-control/dependency recipe are not established by that summary alone. Record evidence of unmodified upstream sources where applicable; obtain missing material if found. A bit-identical rebuild is not required merely to document this, and no rebuild is authorized.
- **Notices:** reconcile the matching WebEngine SDK records and source notice index against the actual shipped modules, plugins and incorporated code. Record which notices are covered and any missing text. Build-specific WebEngine evidence is substantial progress, but neither an SBOM nor 2,664 source-reference notices alone certifies every shipped component. No particular additional missing copyright text was established in this focused review; the final reconciliation remains unsigned.
- **Relinking:** use the replacement guidance in [BUILD.md](BUILD.md). Confirm the selected LGPL shared-library route for each combined work, preserving modification/debugging rights. Separate application object files are not automatically required when a suitable shared-library mechanism satisfies the applicable license. The unresolved J restriction remains independently material.
- **Delivery:** provide actual, complete source access before or alongside executable distribution. An empty repository and a planned upload do not provide it.
- **Release record:** keep r5's hash and this owner-acceptance addendum alongside the unchanged ZIP. Historical companion reports describe earlier application revisions; they do not represent r5 application source or override this review.
- **Public archive preparation:** the companion includes historical reports, scripts and local audit paths as well as sources. Review that evidence for public suitability and redistribution rights before upload. If a corrected/supplemental source set is needed, version and hash it separately; retain the existing archive and executable unchanged.

## Decision and approval boundary

Do not send Slim r5 as licensing-cleared yet. First resolve the two supplier-specific blockers, complete the source/build and notice reconciliation, and establish the actual delivery route. Owner approval alone cannot supply missing third-party rights.

The previously documented supplier-provisioned r3 edition is a distinct artifact with a distinct distribution scope; its earlier decision does not clear Slim r5.

This review prepares documentation only. Uploading archives, creating/publishing a Release, contacting suppliers or sending binaries requires subsequent owner authorization.

## Controlling references

- [MPIR's LGPLv3 text, especially section 4](https://github.com/wbhart/mpir/blob/mpir-3.0.0/COPYING.LIB).
- [GPLv3 source definition and section 6 delivery routes, incorporated by LGPLv3](https://github.com/wbhart/mpir/blob/mpir-3.0.0/COPYING).
- [Jsoftware published warranty/license](https://www.jsoftware.com/help/user/warranty.htm); the actual shipped runtime/j/license.txt was also read.
- [Qt LGPL guidance](https://www.qt.io/development/open-source-lgpl-obligations).
- Retained local OFFLINE_DISTRIBUTION_REVIEW.md and COMPLIANCE_REPORT.md, companion sources/BUILD_INFORMATION.md, release-evidence/runtime-provenance/runtime-versions.json, release-evidence/offline-review/ and both archive manifests.
