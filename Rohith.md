ROHIT

## 1. Crypto - RSA Warmup

I checked the RSA parameters and found that the modulus n = 3233 could be factored into 53 × 61. 
I calculated φ(n) = 3120 and found the private exponent d = 2753. 
I then decrypted the ciphertext values and converted the results into characters to obtain the flag.

*Flag:* OWASP{rs4_s1mple_d3crypt10n}


## 2. Misc - Cipher Master

I examined the encoded message and found that it used multiple transformations. 
I reversed the string, decoded Base64, applied ROT13, and decoded Base64 again. 
Following these steps revealed the reported flag.

*Flag:* OWASP{mu1t1pl3_3nc0d1ng_l4y3rs}


## 3. Forensics - Digital Footprints

I checked the beach photograph's metadata and found hidden text fragments. 
Some fragments were encoded in hexadecimal, while another was readable text. 
I decoded the hexadecimal values and joined all the fragments in the correct order to recover the flag.

*Flag:* OWASP{m3t4d4t4_t3ll3s_4ll_s3cr3t5}


## 4. Forensics - Ghost in the Text

I checked the text file for hidden spaces and tabs. 
I extracted the trailing whitespace pattern and interpreted it as binary data. 
After decoding the pattern, I recovered the reported flag.

*Flag:* OWASP{wh1t3sp4c3_t3lls_s3cr3t5}


## 5. Reverse Engineering - Rev

I examined the encryption process and found that the program used a timestamp to seed Python's random generator. 
I used the receipt 1e7a4f25daa1ca3b to identify the matching timestamp seed, 1749926557. 
I then recreated the XOR mask and decrypted the encrypted data to recover the flag.

*Flag:* OWASP{3v3ry_s3c0nd_c0unts}


## 6. Reverse Engineering - Code Maze

I analyzed the Python script and found that Base64 encoding, zlib compression, and exec() were used to hide the original code. 
I decoded the Base64 data and decompressed it to inspect the source. 
The script checked a password and displayed the flag when the correct password was entered.

*Password:* s3cr3t

*Flag:* OWASP{0bfu5c4t10n_m4k3s_1t_h4rd3r}


## 7. Misc - 67

I noticed that the message contained only the digits 6 and 7. 
I tried treating them as binary symbols, with 6 representing 0 and 7 representing 1, to investigate the hidden message.

*Flag:* OWASP{c0mpu73r5_d0n7_5p34k_b1n4ry_7h3y_5p34k_67}