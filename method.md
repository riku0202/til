# メソッド
### 型を宣言して使う
```
type celsius float64

var temperature celsius = 20
fmt.Println(temperature)

```   
func (キーワード)(k(名前) kelvin(型))(レシーバ)celsius()(メソッド名) celsius(戻り値の型)　　　

```
var k kelvin = 294.0
var c celsius 

c = kelvinToCelsius(k)　関数を呼び出す   
c = k.celsius()　　メソッドを呼び出す
```
練習問題
celsius型、fahrenheit型、kelvin型を使うプログラムを開き、それぞれのメソッドを作って、どの温度型からも、ほかの温度に変換できるようにする。   

```

package main

import "fmt"

type celsius float64
type kelvin float64
type fahrenheit float64

func (c celsius) fahrenheit() fahrenheit {
	return fahrenheit((c * 9.0 / 5.0) + 32.0)
}

func (c celsius) kelvin() kelvin {
	return kelvin(c + 273.15)
}

func (f fahrenheit) celsius() celsius {
	return celsius((f - 32.0) * 5.0 / 9.0)
}

func (f fahrenheit) kelvin() kelvin {
	return kelvin(f.celsius().kelvin())
}

func (k kelvin) celsius() celsius {
	return celsius(k - 273.15)
}

func (k kelvin) fahrenheit() fahrenheit {
	return k.celsius().fahrenheit()
}

func main()  {
	var k kelvin = 294.0
	c := k.celsius()
	fmt.Print(k,"K is",c,"°C")
}
```
