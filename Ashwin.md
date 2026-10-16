Ashwin

## 1. Crypto — XOR Riddle

I inspected the binary and found that its bytes had been reversed. After restoring the ELF executable, I checked the flag-validation function and identified an XOR operation using the key 0x5A. I used the same key to decrypt the stored bytes and recover the flag.

*Flag:* OWASP{fr0m_741l_70_h34d}



## 2. Crypto - Caesar's Secret

I read the question and identified it as a Caesar cipher because it mentioned Julius Caesar and a shift between 1 and 25. I used my Python Caesar Cipher tool and tried different shift keys one by one. On my 12th attempt, I got the readable message.

**Flag:** `OWASP{c43s4r_c1ph3r_1s_34sy_t0_cr4ck}`


## 3. Crypto - Encoding Chaos

The challenge says:

Someone sent me this encoded message, but I can't figure out what encoding was used. Can you decode it and find the flag?
Hint: It's not just one layer...

So from the hint itself, I figured it probably wasn't just normal Base64. The encoded string also looked like Base64 because it had the usual characters and ended with =.

I first decoded it using Base64 and got another string that also looked like Base64, so I decoded that again.

Basically I just kept checking the output after every decode. It was kind of repetitive, but the hint says there are multiple layers, so I assumed I had to keep going.

After decoding it a few times, I got this:

T1dBU1B7YjRzMzY0XzFzX24wdF8zbmNyeXB0MTBufQ==

This still looked like Base64, so I decoded it one more time.

That gave:

OWASP{b4s364_1s_n0t_3ncrypt10n}

So the flag is:

Flag: OWASP{b4s364_1s_n0t_3ncrypt10n}



## 4. Crypto - Weak Lock

I read the question and understood that it used XOR encryption with a simple key. I used my XOR tool and tried different key values. When I tried key 65 (`0x41`), I got a readable output.

**Flag:** `OWASP{w34k_k3y_m4k3s_34sy_w0rk}`
