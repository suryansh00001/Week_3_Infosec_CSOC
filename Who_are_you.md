This is very clear that we have to modify headers
after modifying the first header user-agent: PicoBrowser
we get this 
![image](https://github.com/user-attachments/assets/beb22e12-02e9-4321-b524-48dac9b6af73)

after searching what should I do... again chat gpt helped me
![image](https://github.com/user-attachments/assets/8699d01a-2200-4f7a-9315-7e62d0955d10)
I did that

![image](https://github.com/user-attachments/assets/72fd7223-927c-40fe-92f4-771476ce8b50)

Now I have to make a date from 2018

#Date: Sun, 14 Oct 2018 10:00:00 GMT
![image](https://github.com/user-attachments/assets/d9b0e67d-8b1f-47b7-aa3a-8d50183a6f70)

after searching I get to know that I have to make DNT as 1.. #DNT: 1
![image](https://github.com/user-attachments/assets/37a225b9-72f3-4df5-9a32-055592c7e792)

google asks me to spoof my location with some false header Accept-Language: sv-SE,sv;q=0.9, X-Forwarded-For: 46.246.123.10
![image](https://github.com/user-attachments/assets/c188b3c9-b4c8-4918-9aeb-5ee25b214dc4)
got the flag

    picoCTF{http_h34d3rs_v3ry_c0Ol_much_w0w_0da16bb2}




