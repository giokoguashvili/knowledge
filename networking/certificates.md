# PKI

- **SSL** - Secure Socket Layer
- **TLS** - Transport Layer Security
- Cryptography
    - Asymmetric 
    - Symmetric 
- X.509 - s a standard that defines the format of the digital certificate
- ASN.1 - Abstract Syntax Notation One - formal language
- Certificates Types 
    - Based on Validation Level
        - DV - Domain Validated
        - OV - Organization Validated 
        - EF - Extended Validated
    - Based on the Number of Domains they Secure
        - Single Domain Certificate
        - Wildcard SSL Certificate
        - Unified SSL Certificate /Multi-Domain SSL Certificate/SAN Certificate
- **CA** - Certificate Authority
- **ICA** - Intermediate Certificate Authority
- **CSR** - Certificate Signing Request
- **CRL** - Certificate Revocation List 
- **CDP** - CRL Distribution Point
- **FQDN** - Fully Qualified Domain Name
- **OCSP** - Online Certificate Status Protocol

## **SSL Certificate Formats**


![SSL Certificate Formats](https://user-images.githubusercontent.com/8178412/208239315-81e3d049-b9af-407f-b0ff-c3d14ca0013d.png)

**X.509  (ANS.1)**
- Data Structure
    - Base64 ASCII
        - PEM
        - PKCS#7
    - Binary
        - DER
        - PKCS#12

## Certificate Signing Request
![Certificate Request and Responce](https://user-images.githubusercontent.com/8178412/208239340-419a2c48-2aeb-4a29-9447-9c9ed7bf3be0.png)

- [tuansoibk/cryptography-file-formats.md](https://gist.github.com/tuansoibk/0b1f279be5c1b782d95f4e15af1442cb)
- [What is a Pem file and how does it differ from other OpenSSL Generated Key File Formats?](https://serverfault.com/a/9717/435541)
- [Certificate CA Validation](https://gist.github.com/genaromadrid/9075d315e949fb4b3760db5c36c9a8ca)