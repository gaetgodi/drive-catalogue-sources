# Source availability

Status: archives retained locally; **no source assets or GitHub Release published**. Distribution clearance remains pending. See the [Slim r5 review](SLIM-R5-REVIEW.md).

## Retained companion

Filename: `DriveCatalogue-RC5-offline-Windows-x64-slim-r2-companion-sources.zip`  
Size: 1,351,105,579 bytes  
SHA-256: `d99786903c9c23a005f7ea1aa2a8b75679387dc0e4eae53d1bf7580ef9f4b75e`

This same companion supports Slim r5's unchanged third-party runtime; its historical application evidence is not an r5 application-source export.

| Embedded source | Bytes | SHA-256 |
| --- | ---: | --- |
| sources/qt-everywhere-src-6.10.3.tar.xz | 1315591828 | cbc81e726b0ff3c0cdb0219bf74545e91cec013c4a8503c20f93f83d73dff5d2 |
| sources/ffmpeg-7.1.3.tar.xz | 11032252 | f0bf043299db9e3caacb435a712fc541fbb07df613c4b893e8b77e67baf3adbe |
| sources/qtide-3827c94935ef0dd3d8680032649db9fca767685a.tar.gz | 16669093 | 14e6a5b88dcc520ccd16c84ff864f9dbac98ab0ae873c3ac570f7aeeb0d21935 |
| sources/reference-only/mpir-3.0.0.tar.bz2 | 2572041 | 52f63459cf3f9478859de29e00357f004050ead70b45913f2c2269d9708675bb |

**MPIR is reference only: the corresponding source/build mapping for the shipped DLL remains unresolved.** Matching version labels do not establish complete corresponding source.

## Planned Release asset arrangement

A version-specific source Release is appropriate in principle. The companion is below GitHub's current 2 GiB per-asset limit. Keep large archives out of Git; attach the archive, SHA-256 file, source/build inventory and any necessary supplements as explicit Release assets. GitHub's automatically generated “Source code” ZIP/tarball contains this documentation repository, not the companion sources. [GitHub release documentation](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases).

For a separately hosted executable download, put a conspicuous version-specific source link and checksum next to the executable download and in its delivery message/addendum. Provide equivalent access without additional charge and maintain availability. GPLv3 section 6(d) permits a different source server subject to those conditions; this does not waive other component obligations. [Controlling GPLv3 text](https://github.com/wbhart/mpir/blob/mpir-3.0.0/COPYING).

For direct delivery, provide the companion and any required supplements at the same time through the same delivery channel. For physical media, include the source on the medium under the applicable delivery route. Do not substitute an unsupported “available on request” promise.

The unchanged r5 ZIP currently promises direct simultaneous companion delivery until public availability is established, and retention for at least three years after the last copy is given out. Honor that existing commitment; it is not a universal three-year expiry for network-source obligations. Preserve the ZIP and use an external version-specific addendum for updated links, acceptance status and any supplements.

Before owner-authorized publication: resolve the review gates, review historical evidence for public suitability, choose the tag, record all asset hashes, and ensure the asset links work for recipients. No tag, Release or download URL is asserted to exist yet.
