### Abbreviations

    | Definition              | Description
----|-------------------------|--------------------------------------------------------------------------------------------------
KDC |	Key Distribution Center | Comprises TGS and AS.
TGS |	Ticket Granting Service | Issues Kerberos tickets to authenticated users for specific services identified by their SPN
AS  |	Authentication Server   | Authenticates users based on their TGT
TGT |	Ticket Granting Ticket  | Issued by the DC, used by the client to authenticate with the KDC/AS
SPN |	Service Principle Name  | Identifier for the resource server, consumes and validates Kerberos tickets


Sources: http://www.roguelynn.com/words/explain-like-im-5-kerberos/
