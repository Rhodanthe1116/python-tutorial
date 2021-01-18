# 簡易密碼學

* Python複習
  * 字串複習
  * ASCII複習（chr, ord）
  * and, or複習
* 名詞解釋
* 凱薩加密
* Unicode
* xor加密
  * 先備知識：二進位

## 複習：ascii

文字在電腦裡面是以數字儲存，而ascii是早期用來規範文字轉成數字的對應表

```python
print(ord("a")) # 97
print(chr(97)) # a
```

## 一些名詞

* 字串 String：如`'abc', 'ABC'`
* 字元 Character：只有一個字的字串，如`'a', 'B'`



* 密碼：Cipher
* 明文：Plaintext
* 密文：Ciphertext
* 加密：Encrypt
* 解密：Decrypt

## 凱薩加密 Caecar Cipher 

將所有文字同時位移k

![1](.gitbook/assets/image%20%28106%29.png)

### 範例

* 明文: my\_secret 
* 密文: p\|bvhfuhw（經過往後位移3）

### 實作

#### 凱薩加密一個字元

a -&gt; d

```python
char = 'a'
k = 3
cipher_int = ord(char) + k   # 97 + 3
# 100
cipher_char = chr(cipher_int)
# 'd'
```

錯誤示範

```python
char = 'a'
k = 3
cipher_int = char + k   # 'a' + 3 => TypeError!!
```

#### 凱薩加密一個字串

```python
plain = 'my_secret'
cipher = ''
k = 3

for char in plain:
    cipher_int = ord(char) + k
    cipher += chr(cipher_int)

print(f'plaintext:  {plain}')
print(f'ciphertext: {cipher}')
# plaintext:  my_secret
# ciphertext: p|bvhfuhw
```

可以改變任意的偏移量k，製造不同的密文！

```python
plain = 'my_secret'
cipher = ''
k = -2

for char in plain:
    cipher_int = ord(char) + k
    cipher += chr(cipher_int)

print(f'plaintext:  {plain}')
print(f'ciphertext: {cipher}')
# plaintext:  my_secret
# ciphertext: kw]qcapcr
```

#### 中文也可以

註：中文是以unicode編碼

```python
plain = '這是我的秘密'
cipher = ''
k = 3

for char in plain:
    cipher_int = ord(char) + k
    cipher += chr(cipher_int)

print(f'plaintext:  {plain}')
print(f'ciphertext: {cipher}')
# plaintext:  這是我的秘密
# ciphertext: 逜昲戔皇秛寉
```

### 破解

1. 暴力破解：嘗試各種偏移k，並從中尋找看起來正確的
2. 頻率分析：以英文為例，e, t這些字母很常出現，把密文中常出現的字視為e或t，推出偏移量k

![](.gitbook/assets/image%20%28111%29.png)

#### 暴力破解

嘗試各種偏移k，並從中尋找看起來正確的，通常偏移量不會太多

```python
cipher = 'p|bvhfuhw'
plain = ''

for k in range(1, 26):
    for char in cipher:
        plain_int = ord(char) - k
        plain += chr(plain_int)
    
    print(f'plaintext:  {plain}, k = {k}')
    plain = ''

'''
plaintext:  o{augetgv, k = 1
plaintext:  nz`tfdsfu, k = 2
plaintext:  my_secret, k = 3    <- plain text
plaintext:  lx^rdbqds, k = 4
plaintext:  kw]qcapcr, k = 5
plaintext:  jv\pb`obq, k = 6
plaintext:  iu[oa_nap, k = 7
'''
```

## Unicode 萬國碼：近代常用編碼

早期ascii只有一些英文，而unicode收集各國語言及符號，資料量龐大。

編號大體上是這樣安排：

* 前128個編號，與ASCII完全相同。
* 前65536個編號，是世界各國常見文字。
* 前4294967296個編號，是世界各國罕見文字。

unicode.org：[https://home.unicode.org/](https://home.unicode.org/)

unicode表：[https://unicode-table.com/en/search/?q=26680](https://unicode-table.com/en/search/?q=26680) 

也包含中文、顏文字等，也可以出現在Python中！

```python
print(ord("核")) # 26680
print(chr(26680)) # 核

print(ord("果")) # 26524
print(chr(26524)) # 果

print(ord("💩")) # 128169
print(chr(128169)) # 💩

```

## XOR加密

### 先講結論

* 加密：明文 XOR 密鑰 =&gt; 密文
* 解密：密文 XOR 密鑰 =&gt; 明文

#### 範例

* 加密：'P' XOR 'k' =&gt; ';'
* 解密：';' XOR 'k' =&gt; 'P'

線上工具[http://xor.pw/](http://xor.pw/)

可以發現明文可以經過密鑰變成密文，而密文也可以再利用同樣的密鑰再解密成明文，所以只要雙方把密鑰藏好，就可以安全的進行傳輸，不會洩漏明文。

不過單純的XOR還是很容易被破解，因此也不能亂用，需要做其他變化。而其實很多現實世界的加密方法都是基於XOR的變化，因此XOR還是很重要。

### 實作

#### 可以用套件

```python
pip install pycryptodome
```

```python
from Crypto.Util.strxor import strxor

plain = b'my_secret'
key =   b'randomkey'

cipher_bytes = strxor(plain, key)

print(f'ciphertext: {cipher_bytes.hex()}')
# ciphertext: 1f1831170a0e19000d

plain = strxor(cipher_bytes, key)
print(f'plaintext:  {plain}')
# plaintext:  b'my_secret'
```

或是自己寫xor函數

```python
def xor(a, b):
    return bytes([x ^ y for x, y in zip(a, b)])

plain = b'my_secret'
key =   b'randomkey'

cipher_bytes = xor(plain, key)

print(f'ciphertext: {cipher_bytes.hex()}')
# ciphertext: 1f1831170a0e19000d

plain = xor(cipher_bytes, key)
print(f'plaintext:  {plain}')
# plaintext:  b'my_secret'
```

注意以上的型態不是單純的字串，而是bytes 。並且密文輸出的時候建議加上.hex\(\)轉成十六進位。至於原因需要了解它的原理，但對初學者來說稍微複雜了點，但只要知道這些目前觀念跟用法，就可以稍微玩一下

### 原理

### XOR

* 之前學過的AND, OR, NOT
* 再加一個XOR

![](.gitbook/assets/image%20%28108%29.png)

XOR

![](.gitbook/assets/image%20%28112%29.png)

問題：字串轉成ascii會大於1，怎麼做XOR？

### 進位制

* 平常我們看到的數字是十進位（decimal），由0~9表示 
* 二進位（binary）可以將數字只由0跟1表示 
* 十六進位（hexadecimal）可以將數字由0~9跟a~f表示

```python
'''
chr     ord     bin           hex
字元    十進位   二進位          十六進位
P       80      0101 0000		  50
k       107     0110 1011     6B	
---------------------------------------
;       59	    0011 1011	    3B
'''
```

```python
'''
chr     ord     bin             hex
字元    十進位   二進位          十六進位
m      	109	    0110 1101       6D	
r       114	    0111 0010	    72		
---------------------------------------
???     31	    0001 1111	    1f
'''
```

![](.gitbook/assets/image%20%28109%29.png)

* 不是文字，沒辦法輸出，因此須以hex十六進位儲存 
* 且Python的bytes型態輸出會以十六進位顯示，可以解決字串輸出問題 
* （也可以轉成二進位，但會太長）



