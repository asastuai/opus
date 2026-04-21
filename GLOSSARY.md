# Glossary

A reference for every technical term used across Opus and Kybalion. Organized by domain, written to be understood, not just defined.

---

## Hermetic Philosophy

**Kybalion**
Book published in 1908 that codifies the Seven Hermetic Principles. Attributed to "Three Initiates." The principles themselves are much older — traced to the Corpus Hermeticum (1st-3rd century CE) and the Emerald Tablet (6th-8th century CE).

**Hermes Trismegistus**
"Thrice-Great Hermes." Syncretic figure combining the Greek god Hermes with the Egyptian god Thoth. The mythological source of hermetic teachings. Not a historical person — a symbol for the tradition itself.

**Emerald Tablet**
Ancient alchemical text containing the phrase "As above, so below." In this project, its core claim is formalized as a mathematical theorem: `veil(a) + veil(b) = veil(a + b)` — the definition of homomorphism. The ancients described the same structure that modern cryptography rediscovered in 2009.

**Corpus Hermeticum**
Collection of texts from the 1st-3rd century CE on hermetic philosophy, cosmology, and the nature of mind. Historical source predating the Kybalion by ~1700 years.

**The Seven Principles**

- **Mentalism** — "The All is Mind; the Universe is Mental." Everything is information. In the project: formalized as a trait requiring any type to be reducible to its informational essence and reconstructible from it. NaN (corruption) cannot manifest — it's rejected at the type level.

- **Correspondence** — "As above, so below; as below, so above." Patterns repeat across scales. In the project: formalized as structure-preserving mappings between domains. This IS homomorphic encryption — operations performed "above" (in encrypted space) correspond exactly to operations "below" (in plaintext). The Emerald Tablet described this 1100 years before Gentry formalized it in 2009.

- **Vibration** — "Nothing rests; everything moves; everything vibrates." In the project: formalized via the Discrete Fourier Transform. Every piece of data has a vibrational signature — a frequency decomposition that reveals hidden structure. The DFT converts data from spatial domain to frequency domain and back without loss.

- **Polarity** — "Everything is dual; opposites are identical in nature, different only in degree." Not boolean (true/false) but a continuous spectrum between poles. In the project: the qubit satisfies this trait natively — |0> and |1> are poles, superposition is position between them. The Bloch sphere IS a polar spectrum in 3D.

- **Rhythm** — "Everything flows, out and in; the pendulum-swing manifests in everything." In the project: formalized as cyclic computation with the Law of Neutralization — a master can dampen the swing. Computationally, this is constant-time execution (preventing timing attacks). Also: period detection via autocorrelation — which is exactly what Shor's algorithm does to break RSA.

- **Causality** — "Every cause has its effect; every effect has its cause." In the project: formalized as causal chains with provenance tracking. Every value knows its origin — first cause (Prima) or derived from parents. This IS a blockchain: each block caused by the previous, traceable to genesis.

- **Generation** — "Gender is in everything; everything has its masculine and feminine principles." Not biological sex — creative dynamics. Generative force (expands possibilities) and formative force (selects, shapes). In the project: KeyForge generates many candidates, then selects by quality. This is the GAN pattern: Generator (generative) vs Discriminator (formative).

**Planes of Manifestation**
Three levels: Physical (dense, measurable), Mental (conceptual), Spiritual (subtle, potential). Ordered hierarchy where higher planes contain lower. In the project: an enum with derived ordering.

**Ain Soph**
"Without limit" in Hebrew Kabbalah. Void — pure potential. In the project: `Information::Void` at the Spiritual plane. The hash of nothing is NOT zero — void has its own signature.

---

## Alchemy

**Magnum Opus**
"The Great Work" — the ultimate goal of alchemy: transmutation of base matter into gold, or more abstractly, the perfection of any substance. In the project: the name of the intent-aware stream cipher, because it composes all seven principles into a single functioning artifact.

**Materia Prima**
"First matter" — the raw, undifferentiated substance from which all things emerge. In the project: the cryptographic key or seed before transformation.

**Solve et Coagula**
"Dissolve and reconstitute." The fundamental alchemical operation. In the project: the Hadamard gate implements this exactly — H|0> = |+> (dissolve certainty into superposition), H|+> = |0> (reconstitute certainty). And H squared = Identity — the operation is its own inverse. Dissolution and reconstitution are the same act, separated by context.

**Philosopher's Stone**
The final artifact of the Great Work. Unifies all principles. In the project: the complete Hermetic Computing framework — hash, cipher, quantum model, provenance — all under seven axioms.

**Athanor**
The alchemical furnace where transformation occurs. In the project: metaphor for the Magnum Opus internal state — all seven principles operating in unity.

**The Four Stages of the Work**

- **Nigredo** (Black) — Decomposition. Breaking down into components. In the project's development: the specification phase, where principles were formally broken down.
- **Albedo** (White) — Purification. First four principles implemented, 40 tests passing.
- **Citrinitas** (Yellow/Gold) — First gold. The Hermetic Hash achieved 0.5001 avalanche ratio.
- **Rubedo** (Red) — Completion. All seven principles + Magnum Opus, 87 tests passing.

**The Seven Alchemical Stages** (used in the Hermetic Hash)

1. **Calcination** — Reduction by fire. In the hash: input normalization to 64 floating-point values.
2. **Dissolution** — Breaking apart in water. In the hash: DFT decomposition into frequency spectrum.
3. **Separation** — Isolating components. In the hash: splitting into magnitude (visible) and phase (hidden).
4. **Conjunction** — Marriage of opposites. In the hash: non-linear combination of magnitude and phase.
5. **Fermentation** — Living transformation. In the hash: 7 rounds of cyclic mixing with prime-spaced reaches.
6. **Distillation** — Purification. In the hash: folding 64 values down to 32 via symmetric correspondence.
7. **Coagulation** — Crystallization. In the hash: converting floating-point to bytes via XOR-folding.

**Coniunctio**
The alchemical marriage of opposites (Red King and White Queen). Stage 4 in the hash — where magnitude and phase are combined irreversibly.

**Coincidentia Oppositorum**
"Coincidence of opposites." The philosophical concept that complementary forces unite to create something neither could alone. In the project: the thesis of human-AI collaboration — human direction + AI formalization = emergent creation.

---

## Cryptography

**Hash Function**
A function that takes any input and produces a fixed-size output (the "hash" or "digest"). One-way: easy to compute, practically impossible to reverse. Used for integrity verification, digital signatures, data structures.

**Avalanche Effect**
Property of a good hash: changing one bit of input changes approximately 50% of output bits. Named because a small change "avalanches" through the entire output. The Hermetic Hash achieves 0.5001 — practically perfect (0.5000 is theoretical ideal).

**Avalanche Ratio**
The measured fraction of output bits that flip when one input bit changes. Calculated over many samples. 0.5 = perfect diffusion. Below 0.45 or above 0.55 = problematic.

**Collision**
When two different inputs produce the same hash output. A good hash makes this astronomically unlikely. The Hermetic Hash: 0 collisions in 1000 test inputs.

**Collision Resistance**
The property that finding two inputs with the same hash should be computationally infeasible.

**Diffusion**
Shannon's property: each bit of plaintext influences many bits of ciphertext. Achieved in the project via Vibration (DFT spreading input across frequency bins).

**Confusion**
Shannon's property: the relationship between key and ciphertext should be complex and non-linear. Achieved via Polarity (non-linear polar transmutation).

**Stream Cipher**
Encrypts data one byte at a time by XOR-ing with a keystream. The Magnum Opus is a stream cipher where the keystream is generated from all seven hermetic principles.

**Keystream**
A pseudorandom sequence of bytes used in a stream cipher. Generated deterministically from a key (and in Magnum Opus, from intent). XOR-ed with plaintext to produce ciphertext.

**Plaintext**
The original, unencrypted message.

**Ciphertext**
The encrypted message. Should be indistinguishable from random noise.

**XOR (Exclusive OR)**
Bitwise operation: 1 if bits differ, 0 if same. Critical property: it's self-inverse. `a XOR b XOR b = a`. This means encryption and decryption are the same operation — Solve et Coagula computationally.

**Homomorphism**
A structure-preserving mapping between algebraic structures. If f is a homomorphism: `f(a + b) = f(a) + f(b)`. You can operate on the transformed values and get the same result as operating on the originals and then transforming. This is the mathematical formalization of "As above, so below."

**Homomorphic Encryption**
Encryption that allows computation on ciphertexts. `encrypt(a) + encrypt(b) = encrypt(a + b)`. You can compute without ever seeing the data. Craig Gentry formalized this in 2009. The Emerald Tablet described the same structure ~1100 years earlier.

**Fully Homomorphic Encryption (FHE)**
Homomorphic encryption supporting arbitrary computations (not just addition or multiplication, but both). The holy grail of encrypted computation.

**Isomorphism**
A perfect, lossless correspondence between two structures. Every homomorphism has a "gap" (information lost in translation). An isomorphism has no gap — it's a perfect mirror. In the project: the "Philosopher's Stone of mappings."

**Gematria**
Ancient system assigning numerical values to letters. Hebrew Gematria: Aleph=1, Bet=2, ... Tav=400. Example: "Emet" (Truth) = 441. In the project: formalized as a Correspondence (many-to-one mapping — going up is deterministic, going down requires context).

**Side-Channel Attack**
Extracting secrets from physical implementation details (timing, power consumption, electromagnetic emissions) rather than breaking the math.

**Timing Attack**
A side-channel attack that measures how long operations take. If an operation takes different time depending on secret data, the timing leaks the secret.

**Constant-Time Execution**
Writing code so execution time doesn't depend on secret values. In hermetic terms: the Law of Neutralization — dampening the pendulum swing so rhythm reveals nothing.

**Post-Quantum Cryptography (PQC)**
Cryptographic algorithms designed to resist attacks from quantum computers. Lattice-based, code-based, hash-based. Current standard: CRYSTALS-Kyber.

**Lattice-Based Cryptography**
Security based on the difficulty of finding short vectors in high-dimensional lattices. Foundation of most PQC schemes.

**CRYSTALS-Kyber**
NIST-standardized key encapsulation mechanism based on lattice problems. Planned integration: `Correspondence<LatticePlain, LatticeCipher>`.

**Learning With Errors (LWE)**
Adding deliberate noise until the original signal is unrecoverable. Foundation of lattice-based PQC. In hermetic terms: Vibration — adding noise is adding frequencies until the original is buried.

**Attribute-Based Encryption**
Encryption where decryption rights depend on policy attributes. The Magnum Opus goes further: intent is bound to the keystream itself, not just to access policy.

**EIP-712**
Ethereum standard for signing structured data. Used in SUR Protocol for type-safe transaction signatures.

**FNV Hash**
Fowler-Noll-Vo hash. Simple, fast hash used in the project for CausalId generation. Uses prime 0x100000001b3 as multiplier.

---

## Quantum Computing

**Qubit**
Quantum bit. Unlike classical bits (0 or 1), a qubit exists in superposition of both states simultaneously. Described by two parameters: theta (polar angle) and phi (phase angle) on the Bloch sphere.

**Superposition**
A qubit in state alpha|0> + beta|1> — existing as a weighted combination of both possibilities until measured. Not "both at once" — more like "uncommitted between poles." In hermetic terms: position on the polar spectrum.

**|0> and |1>**
The two basis states (poles) of a qubit. |0> = negative pole (theta=0), |1> = positive pole (theta=1). Measurement always collapses to one of these.

**|+> and |->**
Superposition states. |+> = equal mix of |0> and |1> with phase 0. |-> = equal mix with phase pi. Key discovery in the project: both have identical polarity (0.5) and identical measurement probabilities (50/50) but different phase. This is the Polarity-Vibration entanglement — two principles are not independent.

**Bloch Sphere**
3D representation of qubit state. North pole = |0>, South pole = |1>. Every point on the sphere is a valid qubit state. The equator contains all equal superpositions (differing in phase). This IS a polar spectrum in three dimensions.

**Hadamard Gate**
Single-qubit gate that creates superposition from a definite state (and vice versa). H|0> = |+> (dissolve), H|+> = |0> (reconstitute). H squared = Identity — self-inverse. This is Solve et Coagula implemented as a quantum operation.

**Born Rule**
The probability of measuring outcome |0> is |alpha|^2, outcome |1> is |beta|^2. Named after Max Born (1926). In the project: used to prove that |+> and |-> give identical measurement probabilities despite different phases.

**Measurement Collapse**
When measured, a qubit "collapses" from superposition to a definite state. The unobserved outcome's probability is lost. Irreversible.

**Phase**
The hidden angular parameter of a qubit. Doesn't affect measurement probabilities directly but critically affects interference. The "occult" dimension — invisible but consequential. Key to the Polarity-Vibration entanglement discovery.

**Entanglement**
When two qubits are correlated such that measuring one instantly determines the other, regardless of distance. The state of the pair cannot be described independently.

**Decoherence**
Environmental noise destroying superposition. The qubit "leaks" into its environment and loses quantum properties. The rhythm of noise.

**Shor's Algorithm**
Quantum algorithm that breaks RSA encryption by finding the period of modular exponentiation. Uses the Quantum Fourier Transform — which is the Vibration principle applied in quantum domain. Shor's finds Rhythm.

**Grover's Algorithm**
Quantum search algorithm that amplifies the amplitude (vibration) of the target state. Finds a needle in N haystacks in sqrt(N) steps instead of N. Uses the Vibration principle.

**Quantum Fourier Transform (QFT)**
Quantum version of the Discrete Fourier Transform. Core component of Shor's algorithm. Decomposes quantum states into frequency components — Vibration in quantum domain.

**Quantum Error Correction**
Techniques to protect quantum information from decoherence. In hermetic terms: correcting "polar drift" — keeping qubits on their intended position on the spectrum.

---

## Mathematics

**Fourier Transform**
Mathematical operation that decomposes any signal into its constituent frequencies. Reveals hidden periodic structure. Named after Joseph Fourier (1822).

**Discrete Fourier Transform (DFT)**
The Fourier Transform for discrete data (as opposed to continuous signals). Takes N samples, produces N frequency components. Used in the project to implement Vibration.

**Inverse DFT (IDFT)**
Reverses the DFT — converts from frequency domain back to spatial domain. Critical property: DFT followed by IDFT recovers the original data exactly. Perfect roundtrip.

**Frequency Domain**
Representation of data as a sum of frequencies rather than as sequential values. The DFT converts spatial domain to frequency domain. Reveals structure invisible in the original representation.

**Spectrum**
The set of frequency components that make up a signal. Each component has amplitude (how much) and phase (when in the cycle). The "vibrational fingerprint" of data.

**Amplitude**
The intensity or magnitude of a frequency component. How strongly that frequency is present.

**Phase (signal)**
Where in the oscillation cycle a frequency component starts. Two signals can have identical amplitude spectra but different phases — they sound the same but are temporally offset.

**Resonance**
When two frequencies form a simple ratio (2:1 = octave, 3:2 = fifth). Indicates harmonic compatibility. In the project: detected automatically via ratio analysis.

**Autocorrelation**
Measuring how similar a signal is to a shifted version of itself. If the signal repeats every N samples, autocorrelation peaks at lag N. This is how period detection works — and how Shor's algorithm finds the period that breaks RSA.

**NaN (Not a Number)**
A special floating-point value representing undefined results (0/0, sqrt(-1)). In the project: NaN cannot manifest — `from_essence(&f64::NAN)` returns None. Corruption is rejected at the type level. This wasn't designed — it emerged because it was the only coherent implementation of Mentalism.

**Chi-Squared Test**
Statistical test measuring whether observed data matches expected distribution. For a hash: output bytes should be uniformly distributed. The Hermetic Hash: chi-squared = 244.26 (expected ~255 for uniform).

**Bijection**
A mapping that is both one-to-one (injective) and onto (surjective). Every element maps to exactly one element and vice versa. An isomorphism is a bijection that also preserves structure.

---

## Blockchain & DeFi

**DeFi (Decentralized Finance)**
Financial protocols operating on blockchains without traditional intermediaries. Automated market makers, lending, derivatives — all executed by smart contracts.

**Smart Contract**
Self-executing code deployed on a blockchain. Once deployed, it runs exactly as written — no one can modify it. The rules are the rules.

**Automated Market Maker (AMM)**
A smart contract that provides liquidity for trading without an order book. Uses a mathematical formula (usually x*y=k) to determine prices.

**Liquidity Pool**
Tokens locked in a smart contract that traders can swap against. Liquidity providers deposit tokens and earn fees.

**Flash Loan**
A loan that must be borrowed and repaid within a single transaction. If not repaid, the entire transaction reverts as if it never happened. Enables arbitrage without capital.

**Reentrancy Attack**
Attack where a malicious contract calls back into the vulnerable contract before the first call finishes, exploiting inconsistent state. The DAO hack (2016) used this. In the project: Juan understood this before knowing what a for loop was.

**Perpetual Futures**
Derivatives contracts with no expiration date. Traders can go long or short with leverage. Price kept close to spot via funding rate mechanism.

**Funding Rate**
Periodic payment between long and short traders in perpetual futures. Keeps the perpetual price anchored to spot price. If longs pay shorts, price is above spot; if shorts pay longs, price is below.

**Liquidation**
Forced closure of a leveraged position when collateral falls below maintenance margin. The liquidation engine does this automatically.

**Liquidation Cascade**
Chain reaction: one liquidation pushes the price, triggering more liquidations, which push the price further. Can cause flash crashes.

**Oracle**
External data feed providing off-chain information (prices, etc.) to smart contracts. Examples: Pyth, Chainlink.

**MEV (Maximal Extractable Value)**
Profit available to block producers by reordering, inserting, or censoring transactions. Includes front-running, back-running, and sandwich attacks.

**Sandwich Attack**
An MEV attack: attacker places a buy order before your trade (front-run) and a sell order after (back-run), profiting from the price impact you caused.

**x402 Protocol**
HTTP 402 Payment Required — a micropayment standard for web services. Pay-per-request model for AI agents. Not a competitor to wallets — it's a transport layer for payments.

**Base (L2)**
Coinbase's Layer 2 network on Ethereum. Optimistic rollup — inherits Ethereum security with lower fees and faster transactions.

**Base Sepolia**
Test network for Base. Where contracts are deployed and tested before mainnet.

**Invariant**
A property that must remain true regardless of state transitions. Example: in an AMM, x*y must always equal k. Violations indicate bugs or attacks.

**State Machine**
A system defined by its states and the rules for transitioning between them. Every blockchain is a state machine — transactions are state transitions.

---

## Programming & Software

**Trait (Rust)**
An interface defining required behavior. Any type that implements a trait guarantees it provides certain methods. In the project: each hermetic principle is a trait — any type can "be Mentalism" by implementing to_essence() and from_essence().

**Associated Type**
A type defined within a trait. Example: `Mentalism::Essence` — each implementation of Mentalism defines what its "essence" type is.

**Type Safety**
The compiler catches type errors before the program runs. If it compiles, certain classes of bugs are impossible. In the project: NaN rejection is a type-level guarantee.

**Trait Composition**
A type implementing multiple traits simultaneously. Example: Qubit implements both Polarity and Vibration — proving these principles are not independent.

**Roundtrip**
Converting data to another representation and back, verifying no information is lost. Example: bytes -> DFT -> IDFT -> bytes. If the result matches the input, the roundtrip is perfect.

**Cargo**
Rust's package manager and build system. `cargo test` runs tests, `cargo build` compiles, `cargo run` executes.

**Forge**
Foundry's testing framework for Solidity smart contracts. `forge test` runs the test suite.

**npm**
Node.js package registry. `npm publish` makes a package available to the world. PayClaw was published as `payclaw-ai@0.1.0`.

**SDK (Software Development Kit)**
A package providing tools for building on top of a platform. PayClaw is an SDK for giving AI agents wallets.

**MCP (Model Context Protocol)**
Standard for connecting tools and data sources to AI models. Vigil provides 8 MCP tools for agent integration.

**Monorepo**
A single repository containing multiple related packages/projects. Used in PayClaw and Vigil.

**WASM (WebAssembly)**
Binary instruction format that runs in web browsers at near-native speed. The Kybalion playground compiles Rust to WASM for in-browser execution.

---

## AI & Machine Learning

**GAN (Generative Adversarial Network)**
Neural architecture with two competing networks: Generator creates samples, Discriminator evaluates them. The competition drives improvement. In hermetic terms: Generator = generative force, Discriminator = formative force. The Generation principle, computationally.

**Emergence**
Properties arising from the interaction of components that no component possesses individually. In the project: computationally proven with EmergentNumber — `emerge(2, 2) = 4`, and 4 is a perfect square (a property neither 2 possesses). 1 + 1 > 2.

**Transcendence (computational)**
When a result possesses qualities absent from all inputs. Not just "different" — categorically new. `transcends(result, inputs)` returns true when result has properties no input had.

**Hallucination (AI)**
When a model confidently produces false information. Relevant to the collaboration: the human acts as the verification layer, catching when the AI generates plausible but incorrect code.

**Token Limit**
Maximum conversation length before the AI loses context. In the project: the reason Juan had to re-establish context hundreds of times. He was the persistent memory the AI lacked.

---

## Information Theory

**Information**
In the project: a recursive enum type with four variants — Number, Symbol, Composite, and Void. Everything is information (Mentalism). Not an abstract concept — a concrete data type.

**Essence**
The informational core of any value. Must be extractable (to_essence) and reconstructible (from_essence) without loss. If you can't roundtrip the essence, the type doesn't satisfy Mentalism.

**Entropy**
Measure of uncertainty or randomness. Higher entropy = more unpredictable = better for cryptographic keys. Used in KeyForge to evaluate candidate quality.

**Shannon's Properties**
Claude Shannon (1949) defined two requirements for secure ciphers: confusion (complex key-ciphertext relationship) and diffusion (each plaintext bit influences many ciphertext bits). The Hermetic Hash achieves both through Polarity (confusion) and Vibration (diffusion).

---

## Novel Concepts (coined in this project)

**Hermetic Computing**
The complete framework. Seven hermetic principles formalized as Rust traits, composed into working cryptographic primitives. Not metaphor — operational code with 87 passing tests.

**Hermetic Hash**
256-bit hash with seven alchemical stages. Avalanche ratio 0.5001 (0.015% from perfect). Zero collisions. Each stage maps to an alchemical operation AND a hermetic principle.

**Magnum Opus Cipher**
The world's first intent-aware stream cipher. Semantic purpose is a cryptographic parameter: same key + same plaintext + different intent = different ciphertext. Wrong intent decrypts to garbage.

**Intent-Aware Cryptography**
The concept that *why* you encrypt something should shape *how* it's encrypted. Not metadata attached after the fact — the intent is woven into the keystream generation itself.

**Emerald Tablet Theorem**
Formal proof that `veil(a) + veil(b) = veil(a + b)` — the additive homomorphism property. Named because the Emerald Tablet's "As above, so below" describes exactly this structure.

**Polarity-Vibration Entanglement**
Discovery: |+> and |-> have identical polarity (0.5) and identical measurement probabilities but different phase. Phase is a vibrational property. Therefore Polarity and Vibration are not independent principles — they're entangled at the quantum level. This was not designed; it emerged from the formalization.

**Spectral Logic**
Decision-making on continuous spectra instead of binary true/false. Replaces boolean with SpectralValue — a named position between two poles with a degree of commitment.

**Causal Accumulator**
Running hash of all prior output in the Magnum Opus cipher. Each byte generated changes the internal state — making the cipher causally irreversible. Implements the Causality principle.

**KeyForge**
Key generation implementing the Generation principle. Generative phase: expand seed into 16 candidates. Formative phase: evaluate entropy quality and select the best. Creation through the dance of expansion and selection.

**EmergentNumber**
Data type that detects mathematical properties (prime, even, fibonacci, perfect square) and proves emergence computationally. `emerge(2, 2)` produces 4, which gains "perfect_square" — a property neither input had.

**Law of Neutralization**
Hermetic concept: the master dampens the pendulum's swing. Computationally: constant-time execution. The rhythm of the code reveals nothing to an attacker. The swing is neutralized.

---

## Audio & Music

**Dark Psytrance**
Subgenre of psychedelic trance music. Dark, industrial, mechanical, hypnotic. 145-155 BPM typically. The Darkpsy-engine generates this programmatically.

**Sound Synthesis**
Creating sound from mathematical components (oscillators, filters, effects) rather than recording it. The Darkpsy-engine uses Python for this.

**Surge XT**
Open-source software synthesizer integrated into the Darkpsy-engine for sound generation.

---

*This glossary is part of [Opus](https://github.com/asastuai/opus) — the documented account of a 46-day human-AI collaboration.*
