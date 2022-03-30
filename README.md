# runlength-js
### A run-length encoder in JavaScript ###


Run-length encoding is one of the most trivial forms of data compression methods. It works by combining runs of characters into a value containing the number of times that character is repeated in the run and the actual character itself.

So something like:

UUUXXXXXXXXXXXXXXXXXXXXTTTTTKKKKK

would be encoded to:

3U20X5T5K

In this case, the encoded version of the text has been reduced by ~73%. But note that there may be cases where the encoded text would end up larger than the actual (decoded) plain text; this happens when the text contains many isolated characters rather than runs of characters.

Take for example abcdefghijklmnopqrstuvwxyz (26 characters); if you 'compress' that using a run-length algorithm, you'll end up with 1a1b1c1d1e1f1g1h1i1j1k1l1m1n1o1p1q1r1s1t1u1v1w1x1y1z (52 characters) which is a 100% increase from the decoded version.

The demo of the encoder is at http://dreasgrech.com/upload/runlength/

Note that as of current, the code does not handle instances where the decoded text contains digits.

![image](https://user-images.githubusercontent.com/501697/160917359-ec89e1b9-4020-4578-9b86-4abecef6ea1c.png)


