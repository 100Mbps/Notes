# ping
```python
#python2
import struct
import pyshark
'''
尝试解析协议失败，后来网查wp发现了 pyshark这个库，可以按协议读取数据
filePath = '/home/hanrongjie/Downloads/ping.pcap'
# fr = open(file, 'rb').read()
# print fr[1]
result = ''
with open(filePath,"rb") as f:
    f.seek(39)
    bytes = bytearray(f.read())
    for i in range(0,38):
        result += chr(bytes[i*0x5a1+43]) #算是提醒 然并卵，wireshark打开已经是解析过的二进制文件，而你读的是原始的二进制文件
#print result     
'''
cap = pyshark.FileCapture('/home/hanrongjie/Downloads/ping.pcap', display_filter="icmp && icmp.type==8")
flag = ''
for i in range(0, 38):
    result = cap[i].icmp.data[0]+cap[i].icmp.data[1]
    flag += chr(int(result,16))
print(flag)
cap.close()
```
