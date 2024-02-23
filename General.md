**#ASCII**
Mình sẽ sử dụng vòng lặp for và lệnh _chr_ để chuyển đổi các phần tử trong mảng thành ký tự ASCII
<pre>
  asciichar = [99, 114, 121, 112, 116, 111, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
for num in asciichar:
    print(chr(num), end='')
</pre>

  =>OUTPUT: crypto{ASCII_pr1nt4bl3}
![image](https://github.com/hoahangsau/CryptohackChallenge/assets/153940762/6f29e1f9-67c2-43e5-a325-a45dcff3a985)

**#Hex**
Mình sẽ sử dụng hàm <pre>bytes.fromhex()</pre> để chuyển đổi từ hex sang bytes
<pre>
  hex ="63727970746f7b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d"
flag = bytes.fromhex(hex)
print(flag)
</pre>
=>OUTPUT:b'crypto{You_will_be_working_with_hex_strings_a_lot}'
![Screenshot 2024-02-23 142225](https://github.com/hoahangsau/CryptohackChallenge/assets/153940762/4dc34072-d512-4ff8-b0dc-d73ee5f52032)

**#Base64**
Trước tiên phải import thư viện base64, sau đó decode đoạn hex thành bytes và encode sang base64 bằng hàm <pre>base64.b64encode()</pre>
<pre>
  import base64
hex ="72bca9b68fc16ac7beeb8f849dca1d8a783e8acf9679bf9269f7bf"
bytes = bytes.fromhex(hex)
flag = base64.b64encode(bytes)
print(flag)
</pre>
![Screenshot 2024-02-23 144848](https://github.com/hoahangsau/CryptohackChallenge/assets/153940762/f75f3306-e21e-4156-bf62-a269cc9e0775)

**#BytesAndBigIntegers**
Sau khi install pycryptodome thì chúng ta có thể import được các method bytes_to_long() và long_to_bytes()
<pre>long_to_bytes() : chuyển đổi từ số nguyên dạng long sang chuỗi bytes, còn bytes_to_long() thì ngược lại</pre>
<pre>
  from Crypto.Util.number import long_to_bytes
long = 11515195063862318899931685488813747395775516287289682636499965282714637259206269
bytes = long_to_bytes(long)
print(bytes)
</pre>
![Screenshot 2024-02-23 162732](https://github.com/hoahangsau/CryptohackChallenge/assets/153940762/567d8deb-d466-441d-9e7b-cdb5a793687d)

**#EncodingChallenge**
