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

