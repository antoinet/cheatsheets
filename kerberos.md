### Abbreviations

    | Definition                | Description
----|---------------------------|--------------------------------------------------------------------------------------------------
KDC |	Key Distribution Center | Comprises TGS and AS.
TGS |	Ticket Granting Service | Issues Kerberos tickets to authenticated users for specific services identified by their SPN
AS  |	Authentication Server   | Authenticates users based on their TGT
TGT |	Ticket Granting Ticket  | Issued by the DC, used by the client to authenticate with the KDC/AS
SPN |	Service Principle Name  | Identifier for the resource server, consumes and validates Kerberos tickets
    |   keytab                  | File contains pairs of Kerberos principals and encrypted keys (which are derived from the Kerberos password). You can use a keytab file to authenticate to various remote systems using Kerberos without entering a password. 


Sources: 
* http://www.roguelynn.com/words/explain-like-im-5-kerberos/
* https://kb.iu.edu/d/aumh
* http://tools.ietf.org/html/rfc4559
* https://msdn.microsoft.com/en-us/library/ms995329.aspx
* https://msdn.microsoft.com/en-us/library/ms995330.aspx
