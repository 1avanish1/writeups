# vault-door-4
the following code is relevant to the flag.
```java
byte[] myBytes = {
            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,
            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,
            0142, 0131, 0164, 063 , 0163, 0137, 0146, 064 ,
            'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' ,
        };
        ```
 We observe that the data is segmented to 4 different types,
 one is in decimal,one is in hex,on is octal and last is just the characters.
 Running it through https://gchq.github.io/CyberChef/ i got the flag.
