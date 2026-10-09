# Third-party notices

Visual DITA includes the components below. Their licences govern those components; nothing in the Visual DITA
licence limits the rights they give you.

## OASIS DITA document type definitions

The content models compiled from the document type definitions of DITA 1.0, 1.1, 1.2, 1.3 and the DITA 2.0 draft,
in the standard DITA packages (`out/standard/`).

> Darwin Information Typing Architecture (DITA) Version 1.3, OASIS Committee Specification 01, 30 June 2015.
> Copyright © OASIS Open 2015. All rights reserved.
> Source: <http://docs.oasis-open.org/dita/dita/v1.3/dita-v1.3-part0-overview.html>

> DITA 1.0, 1.1 and 1.2 document type definitions: Copyright © OASIS Open 2005, 2006, 2009; Copyright © IBM
> Corporation 2001, 2004.

> DITA 2.0 draft document type definitions (OASIS release v2.0-beta03, <https://github.com/oasis-tcs/dita> and
> <https://github.com/oasis-tcs/dita-techcomm>): Copyright © OASIS Open 2018. All rights reserved.

Distributed under the OASIS IPR Policy (<https://www.oasis-open.org/policies-guidelines/ipr/>), which permits
copying and distribution of the specification and its artefacts provided the copyright notice and this
paragraph are included. OASIS does not endorse Visual DITA and takes no position on its conformance.

## ProseMirror

The editor's document model, view and commands:
`prosemirror-commands`, `prosemirror-gapcursor`, `prosemirror-history`, `prosemirror-keymap`,
`prosemirror-model`, `prosemirror-schema-list`, `prosemirror-state`, `prosemirror-tables`,
`prosemirror-transform`, `prosemirror-view`, and their dependencies `orderedmap`, `rope-sequence` and
`w3c-keyname`.

> Copyright © 2015-2017 by Marijn Haverbeke <marijn@haverbeke.berlin> and others.
>
> MIT licence — see <https://github.com/ProseMirror/prosemirror/blob/master/LICENSE>.

## xmldom

XML parsing and serialisation outside the browser (`@xmldom/xmldom`).

> Copyright 2019 - present Christopher J. Brody and other contributors.
> Copyright 2012 - 2017 @jindw <jindw@xidea.org> and other contributors.
>
> MIT licence — see <https://github.com/xmldom/xmldom/blob/master/LICENSE>.

## node-sqlite3-wasm and SQLite

The project's index, behind DITA Search, where a file is used and Go to Symbol in Workspace: SQLite with its
full-text search, compiled to WebAssembly by `node-sqlite3-wasm`, shipped in `out/node_modules/node-sqlite3-wasm`
with its licence.

> node-sqlite3-wasm: Copyright (c) 2022-2024 Tobias Enderle.
>
> MIT licence — see <https://github.com/tndrle/node-sqlite3-wasm/blob/main/LICENSE>.

> SQLite is in the public domain: <https://www.sqlite.org/copyright.html>.

## vscode-languageclient

The client for the optional DITA language server (`vscode-languageclient`, `vscode-languageserver-protocol`,
`vscode-jsonrpc`).

> Copyright © Microsoft Corporation. All rights reserved.
>
> MIT licence — see <https://github.com/microsoft/vscode-languageserver-node/blob/main/License.txt>.

## temml

Converts LaTeX to MathML for the equation editor (the formula is stored as MathML, with the LaTeX kept as a
MathML annotation). Bundled into the page script.

> Copyright (c) 2021-2025 Ron Kok.
> MIT licence — see <https://github.com/rontrz/temml/blob/main/LICENSE>.

## SaxonJS

Runs the project's Schematron rules. Shipped as Saxonica issues it, unmodified, in `out/node_modules/saxonjs-he`
(SaxonJS) and `out/node_modules/xslt3-he` (its XSLT compiler), each with its licence.

> Copyright © Saxonica Ltd. Saxonica Public License, Version 2.0, December 2024: see
> `out/node_modules/saxonjs-he/LICENSE.txt`.
>
> DISCLAIMER. THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS." ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDERS OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## SchXslt2

Turns Schematron rules into XSLT 3.0 for SaxonJS; its transpiler, compiled, in `out/schematron/transpile.sef.json`.

> Copyright (c) David Maus.
> MIT licence — see <https://codeberg.org/SchXslt/schxslt2>.

## DITA Open Toolkit

The headings of a task's sections in each language (Before you begin, About this task, Procedure, Results, What to do
next), as DITA-OT 4.4.0 writes them: taken from its `org.dita.base` strings (`xsl/common/strings-*.xml`) into
`common/media/task-labels.css`, part of the page.

> This file is part of the DITA Open Toolkit project. Copyright 2004, 2005 IBM Corporation.
> Licensed under the Apache License, Version 2.0 (below). Source: <https://www.dita-ot.org/>

## Mammoth's reader, and what it uses

Reads Word documents (`.docx`) for **Import Word Document…** and **Convert Word Document to DITA…**: the reading half
of Mammoth (`mammoth`), which Visual DITA carries changed, with what it uses: reading the document's zip (`jszip`,
`pako`, `lie`, `immediate`, `setimmediate`, `readable-stream`, `safe-buffer`, `string_decoder`,
`process-nextick-args`, `isarray`, `core-util-is`, `inherits`, `util-deprecate`) and its helpers (`underscore`,
`dingbat-to-unicode`, `base64-js`).

> `mammoth`: Copyright (c) 2013, Michael Williamson. `dingbat-to-unicode`: Copyright (c) 2021, Michael Williamson.
> BSD 2-Clause licence.
>
> `jszip`: Copyright (c) 2009-2016 Stuart Knightley, David Duponchel, Franz Buchinger, António Afonso. Offered under
> the MIT licence or the GPL version 3; used here under the MIT licence.
>
> `pako`: Copyright (C) 2014-2017 by Vitaly Puzrin and Andrei Tuputcyn, MIT licence; its zlib port: (C) 1995-2013
> Jean-loup Gailly and Mark Adler, zlib licence.
>
> `underscore`: Copyright (c) 2009-2022 Jeremy Ashkenas, Julian Gonggrijp, and DocumentCloud and Investigative
> Reporters & Editors. `lie`: Copyright (c) 2014-2018 Calvin Metcalf, Jordan Harband. `immediate`: Copyright (c) 2012
> Barnesandnoble.com, llc, Donavon West, Domenic Denicola, Brian Cavalier. `setimmediate`: Copyright (c) 2012
> Barnesandnoble.com, llc, Donavon West, and Domenic Denicola. `readable-stream`, `string_decoder`, `core-util-is`:
> Copyright Node.js contributors. `safe-buffer`: Copyright (c) Feross Aboukhadijeh. `process-nextick-args`: Copyright
> (c) 2015 Calvin Metcalf. `isarray`: Copyright (c) 2013 Julian Gruber. `util-deprecate`: Copyright (c) 2014 Nathan
> Rajlich. `base64-js`: Copyright (c) 2014 Jameson Little. MIT licence.
>
> `inherits`: Copyright (c) Isaac Z. Schlueter. ISC licence.

## Rust crates in the Visual DITA core

The Visual DITA core (`out/vd-core.wasm`, compiled from Rust) includes these crates. Where a crate is offered under "MIT or Apache-2.0", Visual DITA uses it under the MIT licence.

| Crate | Version | Licence | Copyright |
|---|---|---|---|
| `sha2` | 0.10.9 | MIT | © 2006-2009 Graydon Hoare, © 2009-2013 Mozilla Foundation, © 2016 Artyom Pavlov |
| `digest` | 0.10.7 | MIT | © 2017 Artyom Pavlov |
| `block-buffer` | 0.10.4 | MIT | © 2018-2019 The RustCrypto Project Developers |
| `crypto-common` | 0.1.7 | MIT | © 2021 RustCrypto Developers |
| `ed25519` | 2.2.3 | MIT | © 2018-2023 RustCrypto Developers |
| `signature` | 2.2.0 | MIT | © 2018-2023 RustCrypto Developers |
| `chacha20poly1305` | 0.10.1 | MIT | © 2019 The RustCrypto Project Developers |
| `chacha20` | 0.9.1 | MIT | © 2019-2023 The RustCrypto Project Developers |
| `poly1305` | 0.8.0 | MIT | © 2015-2019 RustCrypto Developers |
| `aead` | 0.5.2 | MIT | © 2019 The RustCrypto Project Developers, © 2019 MobileCoin, LLC |
| `cipher` | 0.4.4 | MIT | © 2016-2020 RustCrypto Developers |
| `universal-hash` | 0.5.1 | MIT | © 2019-2020 RustCrypto Developers |
| `inout` | 0.1.4 | MIT | © 2022 The RustCrypto Project Developers, © 2022 Artyom Pavlov |
| `opaque-debug` | 0.3.1 | MIT | © 2018-2024 The RustCrypto Project Developers |
| `zeroize` | 1.9.0 | MIT | © 2018-2026 The RustCrypto Project Developers |
| `generic-array` | 0.14.7 | MIT | © 2015 Bartłomiej Kamiński |
| `typenum` | 1.20.1 | MIT | © 2014 Paho Lurie-Gregg |
| `cfg-if` | 1.0.5 | MIT | © 2014 Alex Crichton |
| `ed25519-dalek` | 2.2.0 | BSD 3-Clause | © 2017-2019 isis agora lovecruft |
| `curve25519-dalek` | 4.1.3 | BSD 3-Clause | © 2016-2021 isis agora lovecruft, © 2016-2021 Henry de Valence; portions © 2012 The Go Authors |
| `subtle` | 2.6.1 | BSD 3-Clause | © 2016-2017 Isis Agora Lovecruft, Henry de Valence; © 2016-2024 Isis Agora Lovecruft |

Sources: <https://github.com/RustCrypto>, <https://github.com/dalek-cryptography>,
<https://github.com/fizyk20/generic-array>, <https://github.com/paholg/typenum>, <https://github.com/rust-lang/cfg-if>.

## The Apache License 2.0

> Apache License
> Version 2.0, January 2004
> http://www.apache.org/licenses/
>
> TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
>
> 1. Definitions.
>
> "License" shall mean the terms and conditions for use, reproduction,
> and distribution as defined by Sections 1 through 9 of this document.
>
> "Licensor" shall mean the copyright owner or entity authorized by
> the copyright owner that is granting the License.
>
> "Legal Entity" shall mean the union of the acting entity and all
> other entities that control, are controlled by, or are under common
> control with that entity. For the purposes of this definition,
> "control" means (i) the power, direct or indirect, to cause the
> direction or management of such entity, whether by contract or
> otherwise, or (ii) ownership of fifty percent (50%) or more of the
> outstanding shares, or (iii) beneficial ownership of such entity.
>
> "You" (or "Your") shall mean an individual or Legal Entity
> exercising permissions granted by this License.
>
> "Source" form shall mean the preferred form for making modifications,
> including but not limited to software source code, documentation
> source, and configuration files.
>
> "Object" form shall mean any form resulting from mechanical
> transformation or translation of a Source form, including but
> not limited to compiled object code, generated documentation,
> and conversions to other media types.
>
> "Work" shall mean the work of authorship, whether in Source or
> Object form, made available under the License, as indicated by a
> copyright notice that is included in or attached to the work
> (an example is provided in the Appendix below).
>
> "Derivative Works" shall mean any work, whether in Source or Object
> form, that is based on (or derived from) the Work and for which the
> editorial revisions, annotations, elaborations, or other modifications
> represent, as a whole, an original work of authorship. For the purposes
> of this License, Derivative Works shall not include works that remain
> separable from, or merely link (or bind by name) to the interfaces of,
> the Work and Derivative Works thereof.
>
> "Contribution" shall mean any work of authorship, including
> the original version of the Work and any modifications or additions
> to that Work or Derivative Works thereof, that is intentionally
> submitted to Licensor for inclusion in the Work by the copyright owner
> or by an individual or Legal Entity authorized to submit on behalf of
> the copyright owner. For the purposes of this definition, "submitted"
> means any form of electronic, verbal, or written communication sent
> to the Licensor or its representatives, including but not limited to
> communication on electronic mailing lists, source code control systems,
> and issue tracking systems that are managed by, or on behalf of, the
> Licensor for the purpose of discussing and improving the Work, but
> excluding communication that is conspicuously marked or otherwise
> designated in writing by the copyright owner as "Not a Contribution."
>
> "Contributor" shall mean Licensor and any individual or Legal Entity
> on behalf of whom a Contribution has been received by Licensor and
> subsequently incorporated within the Work.
>
> 2. Grant of Copyright License. Subject to the terms and conditions of
> this License, each Contributor hereby grants to You a perpetual,
> worldwide, non-exclusive, no-charge, royalty-free, irrevocable
> copyright license to reproduce, prepare Derivative Works of,
> publicly display, publicly perform, sublicense, and distribute the
> Work and such Derivative Works in Source or Object form.
>
> 3. Grant of Patent License. Subject to the terms and conditions of
> this License, each Contributor hereby grants to You a perpetual,
> worldwide, non-exclusive, no-charge, royalty-free, irrevocable
> (except as stated in this section) patent license to make, have made,
> use, offer to sell, sell, import, and otherwise transfer the Work,
> where such license applies only to those patent claims licensable
> by such Contributor that are necessarily infringed by their
> Contribution(s) alone or by combination of their Contribution(s)
> with the Work to which such Contribution(s) was submitted. If You
> institute patent litigation against any entity (including a
> cross-claim or counterclaim in a lawsuit) alleging that the Work
> or a Contribution incorporated within the Work constitutes direct
> or contributory patent infringement, then any patent licenses
> granted to You under this License for that Work shall terminate
> as of the date such litigation is filed.
>
> 4. Redistribution. You may reproduce and distribute copies of the
> Work or Derivative Works thereof in any medium, with or without
> modifications, and in Source or Object form, provided that You
> meet the following conditions:
>
> (a) You must give any other recipients of the Work or
> Derivative Works a copy of this License; and
>
> (b) You must cause any modified files to carry prominent notices
> stating that You changed the files; and
>
> (c) You must retain, in the Source form of any Derivative Works
> that You distribute, all copyright, patent, trademark, and
> attribution notices from the Source form of the Work,
> excluding those notices that do not pertain to any part of
> the Derivative Works; and
>
> (d) If the Work includes a "NOTICE" text file as part of its
> distribution, then any Derivative Works that You distribute must
> include a readable copy of the attribution notices contained
> within such NOTICE file, excluding those notices that do not
> pertain to any part of the Derivative Works, in at least one
> of the following places: within a NOTICE text file distributed
> as part of the Derivative Works; within the Source form or
> documentation, if provided along with the Derivative Works; or,
> within a display generated by the Derivative Works, if and
> wherever such third-party notices normally appear. The contents
> of the NOTICE file are for informational purposes only and
> do not modify the License. You may add Your own attribution
> notices within Derivative Works that You distribute, alongside
> or as an addendum to the NOTICE text from the Work, provided
> that such additional attribution notices cannot be construed
> as modifying the License.
>
> You may add Your own copyright statement to Your modifications and
> may provide additional or different license terms and conditions
> for use, reproduction, or distribution of Your modifications, or
> for any such Derivative Works as a whole, provided Your use,
> reproduction, and distribution of the Work otherwise complies with
> the conditions stated in this License.
>
> 5. Submission of Contributions. Unless You explicitly state otherwise,
> any Contribution intentionally submitted for inclusion in the Work
> by You to the Licensor shall be under the terms and conditions of
> this License, without any additional terms or conditions.
> Notwithstanding the above, nothing herein shall supersede or modify
> the terms of any separate license agreement you may have executed
> with Licensor regarding such Contributions.
>
> 6. Trademarks. This License does not grant permission to use the trade
> names, trademarks, service marks, or product names of the Licensor,
> except as required for reasonable and customary use in describing the
> origin of the Work and reproducing the content of the NOTICE file.
>
> 7. Disclaimer of Warranty. Unless required by applicable law or
> agreed to in writing, Licensor provides the Work (and each
> Contributor provides its Contributions) on an "AS IS" BASIS,
> WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or
> implied, including, without limitation, any warranties or conditions
> of TITLE, NON-INFRINGEMENT, MERCHANTABILITY, or FITNESS FOR A
> PARTICULAR PURPOSE. You are solely responsible for determining the
> appropriateness of using or redistributing the Work and assume any
> risks associated with Your exercise of permissions under this License.
>
> 8. Limitation of Liability. In no event and under no legal theory,
> whether in tort (including negligence), contract, or otherwise,
> unless required by applicable law (such as deliberate and grossly
> negligent acts) or agreed to in writing, shall any Contributor be
> liable to You for damages, including any direct, indirect, special,
> incidental, or consequential damages of any character arising as a
> result of this License or out of the use or inability to use the
> Work (including but not limited to damages for loss of goodwill,
> work stoppage, computer failure or malfunction, or any and all
> other commercial damages or losses), even if such Contributor
> has been advised of the possibility of such damages.
>
> 9. Accepting Warranty or Additional Liability. While redistributing
> the Work or Derivative Works thereof, You may choose to offer,
> and charge a fee for, acceptance of support, warranty, indemnity,
> or other liability obligations and/or rights consistent with this
> License. However, in accepting such obligations, You may act only
> on Your own behalf and on Your sole responsibility, not on behalf
> of any other Contributor, and only if You agree to indemnify,
> defend, and hold each Contributor harmless for any liability
> incurred by, or claims asserted against, such Contributor by reason
> of your accepting any such warranty or additional liability.
>
> END OF TERMS AND CONDITIONS

## The MIT Licence

The components above marked "MIT licence" are covered by these terms:

> Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
> documentation files (the "Software"), to deal in the Software without restriction, including without
> limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the
> Software, and to permit persons to whom the Software is furnished to do so, subject to the following
> conditions:
>
> The above copyright notice and this permission notice shall be included in all copies or substantial portions
> of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED
> TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL
> THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF
> CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
> DEALINGS IN THE SOFTWARE.

## The BSD 3-Clause Licence

`ed25519-dalek`, `curve25519-dalek` and `subtle`, with the copyright notices listed above, are covered by these
terms:

> Redistribution and use in source and binary forms, with or without modification, are permitted provided that
> the following conditions are met:
>
> 1. Redistributions of source code must retain the above copyright notice, this list of conditions and the
>    following disclaimer.
> 2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the
>    following disclaimer in the documentation and/or other materials provided with the distribution.
> 3. Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote
>    products derived from this software without specific prior written permission.
>
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED
> WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
> PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY
> DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
> PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
> CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
> OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH
> DAMAGE.

Portions of `curve25519-dalek` were originally derived from Adam Langley's Go ed25519 implementation
(<https://github.com/agl/ed25519/>), Copyright © 2012 The Go Authors. All rights reserved. Those portions are
under the same three conditions and disclaimer, with the third condition reading: "Neither the name of Google Inc.
nor the names of its contributors may be used to endorse or promote products derived from this software without
specific prior written permission."

## The BSD 2-Clause Licence

`mammoth`, `lop`, `option` and `dingbat-to-unicode`, with the copyright notices listed above, are covered by these
terms:

> Redistribution and use in source and binary forms, with or without modification, are permitted provided that
> the following conditions are met:
>
> 1. Redistributions of source code must retain the above copyright notice, this list of conditions and the
>    following disclaimer.
> 2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the
>    following disclaimer in the documentation and/or other materials provided with the distribution.
>
> THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED
> WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
> PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY
> DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
> PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
> CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
> OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH
> DAMAGE.

## The ISC Licence

`inherits`, with the copyright notice listed above, is covered by these terms:

> Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby
> granted, provided that the above copyright notice and this permission notice appear in all copies.
>
> THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING
> ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL,
> DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS,
> WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE
> USE OR PERFORMANCE OF THIS SOFTWARE.

## The zlib Licence

The zlib port in `pako`, (C) 1995-2013 Jean-loup Gailly and Mark Adler, is covered by these terms:

> This software is provided 'as-is', without any express or implied warranty. In no event will the authors be held
> liable for any damages arising from the use of this software.
>
> Permission is granted to anyone to use this software for any purpose, including commercial applications, and to
> alter it and redistribute it freely, subject to the following restrictions:
>
> 1. The origin of this software must not be misrepresented; you must not claim that you wrote the original
>    software. If you use this software in a product, an acknowledgment in the product documentation would be
>    appreciated but is not required.
> 2. Altered source versions must be plainly marked as such, and must not be misrepresented as being the original
>    software.
> 3. This notice may not be removed or altered from any source distribution.
