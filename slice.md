# スライス　　

### スライスを作る   
slice =: []string{"あ","い","う","え","お"}
　
```
planets := []string {
"水星",
"金星",
"地球",
"火星",
"木星",
"土星",
"天王星",
"海王星",
}

terrestrial := planets[0:4]
gasGiants := planets[4:6]
iceGiants := planets[6:8]
fmt.println(terrestrial,gasGiants,iceGiants)
結果
[水星　金星　地球　火星][木星　土星][天王星　海王星]

```   
### スライスを作成
```
a := make([]string,0,10)
a = append(a,"あ","い","う","え")
```
### append  
```  
a := []string{"あ","い","う","え"}   
a = append(a,"oお")   
fmt.Println(a)   
[あいうえお]   
```
