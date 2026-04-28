# Week 2: Encoding, Cryptography & Hashing

**Room:** [https://tryhackme.com/jr/mwr-virtual-internship-week-2-we-love-cybersec]  
**Focus:** Understanding encoding schemes, symmetric encryption, historical ciphers, hashing, and password cracking.  
**Goal:** Learn to identify, encode/decode, encrypt/decrypt, and crack various cryptographic primitives.

---

## 📌 Workshop Topics Covered
- Encoding (URL, Base64, HTML)
- Symmetric encryption (Triple DES, Blowfish, CipherSaber2)
- Historical ciphers (Caesar, Vigenère, Morse)
- Hashing basics (MD5, SHA256, collisions, salting)
- Cracking hashes with tools (John the Ripper, hashcat)

---

## ❓ Questions & Answers

### Task 2: Encoding

**Q1:** What Encoding Schema is also called percent encoding?  
**A:** URL Encoding

**Q2:** Decode `TXkgRmlcy3QgQmFzZTY0IERlY29kZQo=`  
**A:** My First Base64 Decode

**Q3:** What HTML characters should be encoded to prevent XSS?  
**A:** `&, <, >, "`

**Q4:** Please URL Decode:  
`%2From%2Fmwr-virtual-internship-week-2-we-love-cybersec%3FParameter%3DURL%20parameter%201%26Param%3DAnother%20weld%20parameter`  
**A:** `/room/mwr-virtual-internship-week-2-we-love-cybersec?Parameter=URL parameter 1&Param=Another weld parameter`

**Q5:** What is the HTML encoded value for `&` ?  
**A:** `&amp;`

---

### Task 3: Encryption (Symmetric)

**Q1:** What do you call the encrypted plaintext?  
**A:** ciphertext

**Q2:** Encrypt the following with **Triple DES**.  
- Value = `"Let's encrypt something"`  
- Key = `"Weneeda24bytekeyforthis1"`  
- IV = `"Theivis8"`  
**A (ciphertext):** `d1cd629d1771610b41b2d4975acc178f3d158b4fd66cf5bf`

**Q3:** Decrypt the following data using **Blowfish** (CBC mode).  
- Key = `"Thisisakey"`  
- IV = `"password"`  
- Encrypted value = `88f022072f8c065c8abd87b19b35008b6c9763b78a9e4834`  
**A (plaintext):** `MWR[Encryption-is-Fun]`

**Challenge (multi‑schema):**  
Original encryption process:  
1. To Morse Code  
2. Vigenère Encode (key = `"Password"`)  
3. CipherSaber2 Encrypt (key = `"secret"`, 20 rounds)  
4. To Base62  

Encrypted string:  
`ZeDWevLvGNZDRk5Xsr2VzZA6tz81KxO7QkXkoNqO3ZadhRxQTyh8YooemW5rRGNhRyapE2RxVUTo`  

**A (original plaintext):** *[Your solved flag here – add when you complete it]*  
> *Hint: Reverse the steps – Base62 decode → CipherSaber2 decrypt → Vigenère decode → Morse decode.*

---

### Task 4: Historical Ciphers

**Q1:** Knowing that `XRPCCTCRGNET` was encrypted using Caesar Cipher, what is the original plaintext?  
**A:** `ICANENCRYPT`  
*(Shift of 11? X→I is -15 or +11? Either way, the answer is as given.)*

---

### Task 5: Hashing Basics

**Q1:** What is the output size in bytes of the MD5 hash function?  
**A:** 16

**Q2:** Can you avoid hash collisions? (Yea/Nay)  
**A:** nay

**Q3:** Should you encrypt passwords? (Yea/Nay)  
**A:** Nay (you should hash + salt them)

**Q4:** Crack the hash: `5f4dcc3b5aa765d61d8327deb882cf99`  
**A:** `password`

**Q5:** Crack the hash: `dc647eb65e6711e155375218212b3964`  
**A:** `Password`

**Q6:** What hashing format is this hash?  
`e22084c2ca255918f9fc755e06e9dbe7cdf13f0635bdcaffa6db8ba963c25b`  
**A:** `sha256`

**Q7:** Can I get the input of the hash from the output? (yay/nay)  
**A:** nay (hashing is one‑way)

---

### Task 6: Cracking Hashes

**Q1:** Crack this hash: `$2a506$7yoU3Ng8dHTXphAg913cyO6Bjs3K5lBnwq5FJyA6d01pMSrddr1ZG`  
**A:** `85208520`

**Q2:** Crack this hash: `e24df70c9d9c81d60f0e475be740a6cee28744087976f74974d4390396ce36f1`  
**A:** `sadierose`

**Q3:** Crack this hash:  
`faa2b8b7cd11d908f101df15a0b12d4c05a89abc9604df0f275afc9a00280027c95c40e1dfa314b2c4224e820146568205ffd1e58eb7bf6fd07dfe79b83060`  
**A:** `class1999`

**Q4:** Crack this hash: `978d75c9de6da87868795326184dc76e0c4dd0e33e53b0d7a988b180d90ef65`  
**A:** `P@$$wdr12`

**Q5:** Crack this hash: `1DFECA0C002EA40B8619ECF94819CC1B`  
**A:** `n63umyl8lkf4i`

**Q6:** Crack this hash (with salt `tryhackme`):  
`e5d8870e5bdd26602cab8dbe07a942c8669e56d6`  
**A:** `481616481616`

---

## 🛠️ Tools & Commands Used
- `base64` (Linux) for Base64 encoding/decoding
- `python` with `pycryptodome` for Triple DES / Blowfish
- Online tools for URL decoding, HTML encoding
- `hashcat` / `john` for cracking
- `CyberChef` for multi‑step decoding

## 📚 Key Takeaways
- **Encoding ≠ Encryption** – encoding is reversible without a key, encryption requires a key.
- **Hashes are one‑way** – you cannot "decrypt" a hash, only crack by guessing.
- **Salting** prevents rainbow table attacks.
- Historical ciphers (Caesar, Vigenère) are weak by modern standards.
- Always **hash + salt** passwords, never encrypt them.

## 📸 Evidence
> *Add screenshots of your decoding steps, encryption/decryption outputs, or hash cracking sessions here.*

![Base64 decode](Appendix/Screenshots/week2-base64.png)
![Hash cracked](Appendix/Screenshots/week2-hash-crack.png)

---

*End of Week 2*
