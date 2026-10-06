# PoUW-ZK

**Proof-of-Useful-Work L1 Blockchain via Proving System Outsourcing**

Team project 2026/2027 - Faculty of Informatics and Information Technologies, STU in Bratislava - Team 27

## About

Proof-of-Work blockchains waste massive amounts of energy on puzzles that have no value outside consensus,
while Proof-of-Stake tends toward centralization. We are building a prototype **Layer-1 blockchain where
mining power produces something useful: zero-knowledge proofs requested by clients**.

Outsourcing proof generation to miners introduces two core risks: solutions can be **stolen in transit**,
and miners can **amortize work** to gain an unfair advantage. Our protocol is designed to prevent both.

## Research focus

- **Amortization resistance:** can a miner produce many proofs cheaper than one at a time, and do input masking or salt injection prevent it across different proving systems?
- **Progress-freeness:** is each miner's chance to win a block proportional to its power, independent of work already spent?

## Repositories

| Repository | Contents |
| --- | --- |
| `pouw-node` | Reference node in Rust: consensus, mempool, P2P and modular provers |
| `pouw-indexer` | Indexer and real-time API backed by PostgreSQL |
| `pouw-workload` | Synthetic client workload generator |
| `pouw-dashboard` | Web dashboard and block explorer |
| `pouw-deploy` | Full-network deployment, monitoring and end-to-end tests |
| `pouw-docs` | Technical report, architecture models and meeting notes |

Repositories are private during development.

## Team Members

- [Nazar Meredov](https://github.com/Faustynn)
- [Oleksandr Babak](https://github.com/LOGIN)
- [Kostiantyn Cherniakov](https://github.com/LOGIN)
- [Vladimir Riazantsev](https://github.com/LOGIN)
- [Ilia Poliak](https://github.com/LOGIN)
- [Yaroslav Marochok](https://github.com/LOGIN)
- [Nikita Lovkin](https://github.com/LOGIN)

**Supervisors:** Ing. Lukáš Mastiľak, PhD. , Ing. Adam Novocký , doc. Ing. Ivan Homoliak, PhD.

## Key references

- Oleksak, Gazdik, Perešíni, Homoliak — [SNARKChain: Proof-of-Useful-Work Blockchain Consensus with General-Purpose SNARK Marketplace](https://arxiv.org/abs/2510.09729)
- Kattis, Bonneau — [Proof of Necessary Work: Succinct State Verification with Fairness Guarantees](https://eprint.iacr.org/2020/190)
- Groth — [On the Size of Pairing-Based Non-Interactive Arguments](https://doi.org/10.1007/978-3-662-49896-5_11) (EUROCRYPT 2016)
- Chiesa, Lehmkuhl, Mishra, Zhang — Eos: Efficient Private Delegation of zkSNARK Provers (USENIX Security 2023)
- [Arkworks zkSNARK ecosystem](https://github.com/arkworks-rs)
- [Flop Network](https://flop.finance/teaser/) — a proof-of-useful-inference blockchain
