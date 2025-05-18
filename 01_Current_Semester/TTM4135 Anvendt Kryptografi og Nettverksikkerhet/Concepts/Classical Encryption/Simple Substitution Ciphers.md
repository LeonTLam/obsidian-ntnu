---
tags:
  - Concept
---
# Concept for [[Classical Encryption Techniques.md]]

## Caesar Cipher

Moves the $i$-th letter of an alphabet to the $(i+j)$-th letter. The key is the value $j$..

Instead of writing out the whole substitution table, we can define encryption and decryption as follows:

$$\begin{aligned}
\text{Encryption: }c_i = (a_i+j)\bmod n\\
\text{Decryption: }a_i = (c_i-j)\bmod n\\
\text{where }n=26 \text{ or } n=27 \text{ (size of alphabet)}
\end{aligned}$$
### Cryptanalysis of Caesar Cipher

Only need to find where one of the most frequent characters is shifted to.

Suppose ciphertext:

$$\text{PACGHJUHHCRICGRFWRUCRICPHGLFLQH}$$
First, count characters. Most common characters are C and H with freq. 5 each.

If we assume space "∇" is in the alphabet, we try:

1. ∇ -> H, j=8 since ∇= 0.
$$\text{HTVZ∇BM∇∇VJA. . .}$$
	Not correct, no recognizable words and double white-space.

2. ∇ -> C, j=3
$$\text{MY∇DEGREE∇OF∇DOCTOR∇OF∇MEDICINE}$$

## Random Simple Substitution Cipher

assigns random character of the alphabet to another character of the alphabet.

Encryption and decryption defined by the substitution table which randomly permutes the alphabet.

If alpha. has 26 char., there are 26! keys which is greater than $10^{26}$. This is too many keys to search even with modern computers.

Caesar cipher is a special case of the random simple substitution cipher.

### Cryptoanalysis of random substitution

1. Use frequency analysis on the characters of the alphabet.
2. Decipher the following ciphertext:
$$\text{FJLTXCFWKOVLHKJVKCBCOTEEVLPKCKJVJSTWTJYVKJVOJSTSBPLVITWCWPVDBIT WICKTKQLVPHYTPRBJSTQLVYTKKJSCJETSCGTUHKJPTKYLFRTPETXCBTKJFXCJTJ STGCZHTVOCGVZJCXTJTLCJCSHWPLTPOLCWYKFOJSTCQQCLCJHKVQTLCJTKEFJSV HJCQQLTYFCRZTETCLJSTCXVLJFATXTWJKSVHZPRTYCZYHZCJTPCJCGTLBZVEOFI HLTKCBQTLYTWJESFYSFKZCLITFWYVWJFWHVHKVQTLCJFVWFJEVHZPQLVPHYTXVL TJSCWYHRFYXTJTLKVOICKCBTCLKCBCZFJJZTZTKKJSCWVWTYTWJFXTQTLYHRFYX TJTLJSTYCHKJFYKVPCFKYVWKJCWJZBLTYHQTLCJTPCWPFKWTGTLPTKJLVBTPJST KVZTQLVPHYJJSCJPFKCQQTCLKFKJSTPFKJFZZTPECJTLWVEVWTYHRFYXTJTLVOE CJTLQLVPHYTKXVLTJSCWYHRFYXTJTLKVOICKJSTTDQTWKTFWECJTLJSTWPVTKWV JCXVHWJJVCYTWJFXTQTLYHRFYXTJTLJSTILTCJOCYJVLVOJSTTDQTWKTLTKFPTK FWJSTTZTYJLFYTWTLIBJSTYVKJVOKHLGTFZZCWYTEFZZRTXFWFXHXCWPJSTITWT LCZTDQTWKTKCPZFRFJHX}$$

#### Frequency analysis of ciphertext

| No. | Char. | %    | Freq. |
| --- | ----- | ---- | ----- |
| 1   | T     | 15.4 | 110   |
| 2   | J     | 10.2 | 73    |
| 3   | C     | 8.3  | 59    |
| 4   | K     | 6.7  | 48    |
| 5   | L     | 6.7  | 48    |
| 6   | V     | 6.3  | 45    |
Since E ant T are most frequent characters in English, we can assume E -> T and T - J in the substitution table.
Start by looking for English words like THE or other common trigrams.