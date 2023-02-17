# 1. Two Sum
# https://leetcode.com/problems/decode-the-message/

```py

class Solution:
    def decodeMessage(self, key: str, message: str) -> str:
        
        chs = set()
        hm = {}
        alpha = "abcdefghijklmnopqrstuvwxyz"
        i = 0  
        for ch in key:
            if ch not in chs and ch != ' ':
                chs.add(ch)
                hm[ch] = alpha[i]
                i += 1
        output  = ""
        for ch in message:
            if ch == " ":
                output += " "
            else: 
                output += hm[ch]
        return output


## Complexity Analysis
 