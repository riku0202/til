# ファーストクラス関数 
### 変数に関数を代入
  ```

package main

import (
	"fmt"
	"math/rand"
)

type kelvin float64

func fakeSensor() kelvin {
	return kelvin(rand.Intn(151) + 150)
}

func realSensor() kelvin {
	return 0
}

func main()  {
	sensor := fakeSensor*/var sensor func() kelvinとも書ける/*
	fmt.Println(sensor())

	sensor = realSensor
	fmt.Println(sensor())
}



```     
### 関数をほかの関数に渡す   

```
package main

import (
	"fmt"
	"math/rand"
	"time"
)

type kelvin float64

func measuretemperature(samples int, sensor func() kelvin)  {
for i := 0;i < samples; i++ {
	k := sensor()
	fmt.Printf("%vo K\n",k)
	time.Sleep(time.Second)
}
}

func fakeSensor() kelvin {
	return kelvin(rand.Intn(151) + 150)
}

func main()  {
	measuretemperature(3, fakeSensor)
}


func drawTable(rows int, getRows func(rows int)(string,string))
を
type getRowsFn func(row int)(string string)
func drawTable(rows int,getRow getRowFn)
にできる
```
### クロージャーと無名関数   
```

package main

import "fmt"

type kelvin float64

//sensorの関数型
type sensor func() kelvin

func realSensor() kelvin {
	return 0
}

func calibrate(s sensor, offset kelvin) sensor {
	return func() kelvin {
		return s() + offset
	}
}

func main()  {
	sensor := calibrate(realSensor, 5)
	fmt.Println(sensor())
}





var k kelvin = 294.0
sensor := func() kelvin {
return k
}
fmt.Println(sensor())//294

k++

fmt.Println(sensor())//295
```
