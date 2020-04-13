# Easy onboarding of entities with Well Known DID Configuration (DIF)

Using the [IETF 8615 Well-Known Uniform Resource Identifiers](https://tools.ietf.org/html/rfc8615), the DIF (Decentralized Identity Foundation) has [specified](https://identity.foundation/specs/did-configuration/) one way to facilitate the connection of existing systems and Decentralized Identifiers (DIDs), which is important to facilitate adoption of DIDs in the enterprise arena. The idea is to use the ability of a DID controller to prove it is the same entity that controls an Internet domain.

The entity has to provide proof of a bi-directional relationship between the controller of an Internet domain and a DID via cryptographically verifiable signatures that are linked to a DID's key material.

The details can be found in the DIF document ['Well Known DID Configuration'](https://identity.foundation/specs/did-configuration/) but essentially it means that the DID Configuration resource MUST exist at the domain root, in the IETF 8615 Well-Known Resource directory, as follows.

Assume that an entity has the following domain: `example.com`.
Then at the URL `https://www.example.com/.well-known/did-configuration` there should be a document like the following, with a JSON object containing a DID string and cryptographic proof (in the form of a JWT signed with the specified DID's keys) that verifies **the domain controller and the DID controller are the same entity**.

```json
{
  "entries": [
    {
      "did": "did:ala:quor:redt:123...",
      "jwt": "ewogICJAY29udGV4dCI..."
              ↑ EXAMPLE OF DECODED JWT VALUE
              {
                "iss": "did:ala:quor:redt:123...",
                "domain": "example.com",
                "exp": 1475878357
              }
    }
  ]
}
```