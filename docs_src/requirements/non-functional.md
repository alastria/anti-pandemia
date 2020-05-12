# Non-functional requirements

## Massive onboarding of citizens should not overload the blockchain network

- Integrated with EBSI (European Blockchain Services Infrastructure) and reusing the ESSIF components, where EBSI will have a global public registry of official health institutions (similar to the registry for Universities). The EBSI registry should be accessible externally by anybody in read mode, to verify the public identities of the health institutions. However, the application can be configured to work using any other blockchain network with compatible interfaces. Additionally, the application can reuse many of the components already available for the Diplomas use case in EBSI.

- In an initial phase of the application, it is not strictly necessary that the citizens have an official identity issued by the government (ESSIF). For crisis management it could be enough that they self-issue a DID which is then used in the credential issued by the practitioner when performing the test or vaccination procedure to the citizen.


- Credentials are stored in-app except practitioner credentials representing their identities, which are stored in a public registry. Stale/old data is deleted.

- An interactive and patient focused e-consent system will be included in order to ensure the highest consent rate possible, integrated with the health status credentials.

- Citizen data is only read by practitioners, not stored (equivalent of showing a piece of paper, but not copying it).

- The important exception being the case for government data analysis, for crisis management purposes.

## PIA (Privacy Impact Assessment) for anything written by the citizen to the blockchain

If the citizen writes anything to the blockchain, there should be a PIA performed to assess the privacy of the system.

