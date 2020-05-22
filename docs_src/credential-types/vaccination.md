# Vaccination data model

Taken from [Designing and implementing an immunisation information system](https://www.ecdc.europa.eu/sites/portal/files/documents/designing-implementing-immunisation-information-system_0.pdf).


| **Vaccine provider**                                  |                   |
--------------------------------------------------------|-------------------|
| **Identification** (Name, surname and ID)                 | [Medical Organization (Schema.org)](https://schema.org/MedicalOrganization) |
| Location of the health facility or vaccination centre | [Location (Schema.org)](https://schema.org/location) |
| Type of vaccine provider (private/public)             | String     |
| Contact telephone                                     | [Telephone (Schema.org)](https://schema.org/telephone) |
| Email address                                         | [Email (Schema.org)](https://schema.org/email)     |


| **Vaccine recipient**                                                                | |
---------------------------------------------------------------------------------------|-|
| Unique ID                                                                            | |
| Name, surname, second name                                       | [Birth Date (Schema.org)](https://schema.org/birthDate) |
| Date of birth                                                                        | |
| Sex                                                                                  | |
| Place of residence                                                                   | |
| Telephone number                                                | [Telephone (Schema.org)](https://schema.org/telephone) |
| E-mail address                                                  | [Email (Schema.org)](https://schema.org/email) |
| Occupation                                                                           | |
| Name, surname, unique ID of parents or legal tutor, and relationship to the patient  | |
| Vaccine recipient status indicator on the IIS: provider facility level               | |
| Other potential information fields: ethnicity, patient multiple birth indicator, patient birth order, birth region, birthing facility name                                                         | |


| **Vaccination details**                                             | |
----------------------------------------------------------------------|-|
| Date of administration                                              | https://schema.org/Date |
| Dose                                                                | |
| Brand name                                                          | |
| Antigen(s)                                                          | |
| Batch number                                                        | |
| Reason for refusal                                                  | |
| Reason for contra-indication                                        | |
| Type of vaccination (on/off-routine programme, catch-up campaigns)  | |

