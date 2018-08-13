# RC4 took an L - 40 Points

Alphabet = **#_23456789abcdefghijklmnopqrstuvwxyz**

Key= **pq_xc589r3nb#mgjtkh7w2dlfvy4eaoi6uzs**

Ciphertext: **wpwt#5ng4_qbitp#8mq59r_g866c4t59c6vy6tisj4af6bprfnbd_wrq2wjmr4ld_s26a7i#biiyqjolq8lus_wfusfkj8xv2qrrv3etab_marovc#uuoueyl**

Its a stream cipher. I started working on rc4 encryption algorithm and did not get any results for a long time.

My friend hinted me look at the description again before banging on rc4. The description said "took an L". Then, after a few searches I came to know that there is an algorithm called LC4.
That's why it's called "took an L".

I found a github repo that implemented lc4 algorithm,
https://github.com/dstein64/LC4/blob/master/documentation.md

Then the flag is easily decrypted.

![rc4_l](https://user-images.githubusercontent.com/42334661/44051118-9a5c3404-9f56-11e8-94a3-56c00951a613.png)


### Flag: tjctf{elsie_four_is_not_rc4}

This was pretty straight forward if you figure out it is lc4.






