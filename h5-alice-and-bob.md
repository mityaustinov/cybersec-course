# H5_AliceAndBob

## x. Read and summarize (with some bullet points)
### € Schneier 2015: Applied Cryptography:

#### Chapter 1 - Foundations

**Key terms**

Plaintext &rarr; Encryption &rarr; Ciphertext &rarr; Decryption &rarr; Original plaintext

**Crypthography** (art and science of keeping message secure) practiced by *cryptographers.* 

**Cryptoanalysis** (art and science of breaking ciphertext) practiced by *cryptoanalysts.* 

**Cryptology** (branch of mathematics encompassing both cryptography and cryptanalysis) practiced by *cryptologists.* 

**Sender and receiver**

**Sender** (A) is an actor who sends the message. **Receiver** (B) is the one who receives it. Besides that in crypography context Sender is the one who encypts the message and Receiver is who decrypts it.\

Note to self and reader: Alice and Bob are placeholder names used for describing two parties of communication, A and B.

**Messages and Encryption**

Message can be a text file, a bitmap, a stream of digitized voice, video, image.

Plaintext is denoted by M, for message, or P, for plaintext.

Ciphertext is denoted by C. 

The encryption function E, operates on M to produce C: *E(M) = C* 

In the reverse process, the decryption function D operates on C to produce M: *D(C) = M*

The whole point of encrypting and then decrypting a message is to recover the original plaintext: *D(E(M)) = M*

**Algorithms and Keys**

A cryptographic algorithm (cipher), is the mathematical function for encryption and decryption.

Restricted algorithm based on keeping the way that algorithm works a secret. Restricted algorithms are inadequate by today's standards, because if someone accidentally reveals the secret, everyone must change their algorithm. They neither allow quality control or standardization. Despite these drawbacks, restricted algorithms are enormously popular for low-security applications.

Modern cryptography solves this problem with a key (K). Both the encryption and decryption operations use this key, so the functions now are:

*E<sub>K</sub>(M) = C*

*D<sub>K</sub>(C) = M*

*D<sub>K</sub>(E<sub>K</sub>(M)) = M*

Some algorithms use a different encryption key (K1) and decryption key (K2):

*E<sub>K1</sub>(M) = C*

*D<sub>K2</sub>(C) = M*

*D<sub>K2</sub>(E<sub>K1</sub> (M)) = M*

**Symmetric Algorithms**

Symmetric (sometimes conventional) algorithms, are algorithms (secret-key, single-key, or one-key algorithms) where the encryption key can be calculated from the decryption key and vice versa. These algorithms require that the sender and receiver agree on a key before they can communicate securely. As long as the communication needs to remain secret, the key must remain secret.

Algorithms that operate on the plaintext a single bit (or byte) at a time are called stream algorithms. Algorithms that operate on the plaintext in groups of bits (64 bits—large blocks) are called block algorithms or block ciphers.

**Public-Key Algorithms**

Public-key (asymmetric) algorithms are designed so that the key used for encryption is different from the key used for decryption.

Anyone can use the public key (the encryption key can be made public) to encrypt a message, but only a specific person with the corresponding decryption key can decrypt the message.

In these systems, the encryption key is often called the public key, and the decryption key is often called the private key.

Sometimes, messages will be encrypted with the private key and decrypted with the public key; this is used in digital signatures.

#### Chapter 2 - Protocol Building Blocks, sections

The chapter focuses on public-key cryptography. A symmetric algorithm is like a safe with one combination: whoever knows it can both lock and unlock, but both people must share that secret first. In 1976, Diffie and Hellman introduced a system with two different keys, one public, one private. It works like a mailbox: anyone can drop mail in through the slot (encrypt with the public key), but only the owner with the key can take mail out (decrypt with the private key). You can't work out the private key from the public one.

This solves the biggest problem of symmetric encryption: agreeing on a secret key without meeting first. Alice just looks at Bob's public key, encrypts, and sends. An eavesdropper (Eve) who sees the public key and the encrypted message still can't read it. In a network, everyone publishes their public key, so you can message anyone, like regular mail.

The challenge with public-key crypto is that it isn't used to encrypt actual messages, because it's very slow (symmetric is 1000+ times faster) and vulnerable to guessing attacks when the possible messages are few.

The solution for the challenge are hybrid systems which use use both. Public-key crypto securely shares a one-time session key, then a fast symmetric algorithm uses that key to encrypt the conversation. This is also safer because the session key is created when needed and destroyed after, so no long-lived key sits around to be stolen, and the private key is only used briefly.

### Karvinen 2023: PGP - Send Encrypted and Signed Message - gpg

The material is a hands-on tutorial on how to sen private and verified messages, using PGP with the gpg command-line tool. Alice sends a secret message to Tero. Encryption keeps others from reading it; signing proves it really came from Alice and wasn't changed. Alice is simulated with a separate folder to make practice easy on one computer.

Each person has a public key (shared freely) and a private key (secret). They're used in opposite directions:

* Alice encrypts with Tero's public key, and only Tero's private key can open it.
* Alice signs with her own private key, and Tero verifies with Alice's public key to confirm it's her.

**Setting up trust.** The two exchange public keys and check that each key really belongs to the right person by comparing its fingerprint over a trusted channel (a phone call). The keys can travel over the untrusted internet; only the fingerprint check needs to be trustworthy.

**Sending.** Alice runs one command that encrypts and signs her message, producing a block of plain text safe to paste anywhere. Tero decrypts it with his private key, and gpg confirms "Good signature from Alice."

PGP lets two people communicate privately and prove their identities over an untrusted network, as long as they verify each other's key fingerprints once at the start.

## a. Pubkey today

One of my most frequent daily uses is regular internet browsing. Each time I visit a website over HTTPS, my browser receives the website's public key inside its certificate. The website (the server) keeps the matching private key secret. My browser uses the public key to verify the server and to securely agree on a shared session key. From that moment public key is not used anymore in this session, as both sides use a faster shared key to encrypt everything in both directions, so a malicious actor on the network can't read my password or bank details. So the public key does the setup, the server's private key proves its identity, and the shared symmetric key does the actual work during the session. [What happens in a TLS handshake?](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/)

## b. Encrypt a message

## c. Eve and Mallory

## d. Password management

## e. Refer to sources

## f. Details of PGP

## g. Cryptopals

## References

* Cloudflare: [What happens in a TLS handshake?](https://www.cloudflare.com/learning/ssl/what-happens-in-a-tls-handshake/). Cloudflare Learning Center. Read on 23.11.2026.
* Schneier, B. 2015: [Applied Cryptography: Protocols, Algorithms and Source Code in C](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/). 20th Anniversary Edition, Wiley. Read on 21.11.2026:
  * Chapter 1 – Foundations, section 1.1 [Terminology](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/08_chap01.html#chap01-sec001) (Sender and Receiver, Messages and Encryption, Algorithms and Keys, Symmetric Algorithms, Public-Key Algorithms).
  * Chapter 2 – Protocol Building Blocks, section 2.5 [Communications Using Public-Key Cryptography](https://learning.oreilly.com/library/view/applied-cryptography-protocols/9781119096726/10_chap02.html#chap02-sec005).
* Karvinen, T. 2023: [PGP - Send Encrypted and Signed Message - gpg](https://terokarvinen.com/2023/pgp-encrypt-sign-verify/). Read on 21.11.2026.
* Karvinen, T. 2026. Cyber Security – 2026 late autumn, homework h4. Accessed 21.11.2026. [https://terokarvinen.com/cyber-security/#h4](https://terokarvinen.com/cyber-security/).