Hanish writeup


# CTF Writeups

## 1. Server-Side Template Injection (SSTI)

**References:**
- https://portswigger.net/web-security/server-side-template-injection
- https://swisskyrepo.github.io/PayloadsAllTheThings/Server%20Side%20Template%20Injection/
- https://github.com/m14r41/PentestingEverything

I started by reading about SSTI and testing the input field with `{{7*7'}}`. The unusual output helped me identify a possible Jinja2 template injection. I then tested commands using Python's `os` module and confirmed command execution with `id` and `ls`. Finally, I inspected the application source returned by the command and found the flag.

**Flag:** `OWASP{sst1_4ll0ws_rc3_1f_n0t_s4n1t1z3d_13b995a6b0}`

## 2. Pixel Secret

I tried opening the given PNG file in Notepad, but its contents were unreadable. I then tried several online image analysis tools, including FotoForensics and PNG analyzers. Finally, I uploaded the image to Aperi'Solve, where `zsteg` revealed the hidden flag.

**Flag:** `OWASP{50_11tt13_b1ts_h1d3_b1g_s3cr3t5}`

## 3. Hidden in Plain Sight

I inspected the given file using a hexadecimal dump. I noticed that the flag was visible in the ASCII column, split across two consecutive lines. Combining the text revealed the complete flag.

**Flag:** `OWASP{h3x_d4mp5_4r3_y0ur_fr13nd}`

## 4. Hidden Profile

I noticed that the user's profile URL ended with `/1`. I replaced it with `/0` and found that I could access another profile without proper authorization. The flag was available on that profile.

**Flag:** `OWASP{1d0r_all0ws_un4uth0r1z3d 4cc3ss_367d80650d}`

## 5. What!?

I searched online and found a relevant blog on Hacktron AI. After reading several related blog posts and searching GitHub, I identified the library, the fixing commit, and the affected platform. These details led me to the flag.

- **Library:** libheif
- **Commit ID:** `85e21ad0ecfbf448cf68f76084e7cf46fbdf5223`
- **Platform:** Discourse

**Flag:** `OWASP{libheif_85e21ad0ecfbf448cf68f76084e7cf46fbdf5223_discourse}`
