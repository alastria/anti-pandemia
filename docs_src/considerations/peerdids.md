# Ledger-based vs Peer DIDs

ESSIF-MVP1 and the current AlastriaID implementation use “classic” **ledger-based** DIDs (i.e. DIDs registered on a Blockchain). In [DIF](https://identity.foundation/) (Decentralized Identity Foundation), other types of DIDs are available, such as “peer” DIDs that are **not registered** on a blockchain/DLT.

The following considerations apply to “classic” ledger-based DIDs:

* They can be called “omnidirectional” or **“anywise”** identifiers, because **anyone** (with read access to the DLT used for DID registration) can **resolve them globally**.

* They require privacy considerations due to certain attributes of Blockchains (e.g. immutability) which are in tension with the GDPR.

* They are particularly useful for DID Subjects who are Issuers of Verifiable Credentials (because Verifiable Credentials contain information about the Issuer, e.g. their DID).

* They are resolved using a global “source of truth” based on strong consistency and integrity guarantees offered by Blockchains and similar networks.

The following considerations apply to “peer” DIDs:

* They can be called “unidirectional” or “pairwise” identifiers, meaning that **only one party** other than the DID Subject (or a limited group of parties) **can resolve them**.

* The use of such identifiers is considered **best practice** under a principle known as **directed identity** and since they are not registered on a Blockchain there are no tensions with data protection regulations.

* They may have **weaker consistency and integrity guarantees** than “classic” ledger-based DIDs (because they are not stored on a Blockchain).

In order to facilitate massive onboarding of citizens, we will enable the usage of **pairwise** DIDs, in addition to the current ledger-based DIDs. When it is not practical or feasible to use ledger-based DIDs, the citizens will have the possibility to use pairwise DIDs.
Essentially, the onboarding process consists on the creation of the SSI identity, in the form of a DID.
In this use case, we do not require that citizen identities are of the highest level according to the eIDAS classification and we can start with lower levels and escalate levels later.