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
