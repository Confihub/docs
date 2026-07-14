# Confi.cash documentation instructions

## About this project

- This is the public documentation site for Confi.cash, built with Mintlify.
- Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json`.
- Use the Mintlify skill in `.agents/skills/mintlify` for components, configuration, and validation.
- Treat the live product and reviewed source documentation as the source of truth. Do not infer privacy guarantees.

## Terminology

- Write **Confi.cash** for the user-facing product.
- Use **ConfiBatch** only when discussing the underlying protocol or implementation.
- Write **shielded balance**, not anonymous balance.
- Qualify privacy claims by naming the observer: for example, “hidden from chain observers.”
- Use **public Stellar address** for a `G...` address and **shielded address** for a `cb1...` address.
- Call the current network **Stellar testnet**. Never imply that mainnet is supported.
- Use **operator** for the party running the sequencer and relayer.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise—one idea per sentence.
- Use sentence case for headings.
- Bold UI labels: Click **Connect wallet**.
- Use code formatting for addresses, file names, commands, and code references.
- Lead with the user outcome, then explain the mechanism.
- Prefer plain language. Define protocol terms on first use.
- Avoid promotional claims such as “fully private,” “anonymous,” “untraceable,” or “trustless.”

## Public content boundaries

Document:

- User-facing testnet workflows and troubleshooting.
- What chain observers, recipients, liquidity venues, anchors, and the operator can see.
- High-level protocol architecture and browser-side proof generation.
- Public network status, contract identifiers, supported wallets, and supported assets when sourced dynamically or clearly dated.
- Security assumptions, known limitations, and responsible testing guidance.

Do not document:

- Secrets, credentials, signer tokens, private keys, decrypt shares, or their storage locations.
- Host addresses, firewall rules, deployment topology details, SSH procedures, or private monitoring endpoints.
- Internal admin or operator routes, consoles, runbooks, or recovery commands.
- Step-by-step key ceremonies or infrastructure provisioning.
- Exploit reproduction, incident-sensitive details, or attack instructions that are not already intended for public disclosure.
- Private repository paths or links that a public reader cannot access.
- Unreleased roadmap work as if it were available.

## Required safety language

- State that Confi.cash is an experimental testnet proof of concept and must not be used with real funds.
- State that it has not been independently audited.
- State that deposit and withdrawal boundaries are public.
- State that the active amount-blind path does not send plaintext amounts to ordinary relay intake or application logs.
- State that Confi.cash operates enough threshold-committee infrastructure to reconstruct individual swap amounts with quorum-level administrative access. Never claim privacy from Confi.cash itself.
- State that network metadata such as IP address and timing can still be observed by the service operator.
- Distinguish batched swaps from solo settlement; solo settlement makes the individual amount the public net.
