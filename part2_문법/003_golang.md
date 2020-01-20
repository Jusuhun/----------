# GoLang

[기본환경설정](https://niceman.tistory.com/128)
[GO의 주요 특징](https://golangkorea.github.io/post/go-start/feature/)

## INI 확장자 처리

터미널에서 `go get gopkg.in/ini.v1`로 페키지 설치

``` go
package main

import (
    "fmt"
    "time"

    "gopkg.in/ini.v1"
)
func main() {
    cfg, err := ini.Load("setting.ini")
    if err != nil {
        panic(err)
    }

    //각종 타입으로 가져올 수 있습니다.
    Bool, err := cfg.Section("types").Key("Bool").Bool()
    String := cfg.Section("types").Key("String").String()
    Int, err := cfg.Section("types").Key("Int").Int()
    Uint, err := cfg.Section("types").Key("Uint").Uint()
    TimeFormat, err := cfg.Section("types").Key("TimeFormat").TimeFormat(time.RFC3339)
    Time, err := cfg.Section("types").Key("Time").Time()

    //각종 타입으로 가져올 때에 기본 값을 지정할 수 있습니다.
    MustString := cfg.Section("Must").Key("MustString").MustString("default")
    MustBool := cfg.Section("Must").Key("MustBool").MustBool(true)
    MustInt := cfg.Section("Must").Key("MustInt").MustInt(10)
    MustUint := cfg.Section("Must").Key("MustUint").MustUint(10)
    MustTimeFormat := cfg.Section("Must").Key("MustTimeFormat").MustTimeFormat(time.RFC3339, time.Now())
    MustTime := cfg.Section("Must").Key("MustTime").MustTime(time.Now())

    //선택해서 가져올 수 있습니다.
    In := cfg.Section("InTypes").Key("In").In("default", []string{"one", "two", "three"})
    InInt := cfg.Section("InTypes").Key("InInt").InInt(0, []int{10, 20, 30})

    //시작과 최소, 최대값을 정하여 범위로 가져올 수 있습니다.
    RangeInt := cfg.Section("Range").Key("RangeInt").RangeInt(1, 0, 20)

    //각종 타입으로 구분자로 분리하여 가져올 수 있습니다.
    Strings := cfg.Section("delimiter").Key("Strings").Strings(",")
    Ints := cfg.Section("delimiter").Key("Ints").Ints(",")
    Uints := cfg.Section("delimiter").Key("Uints").Uints(",")
    Times := cfg.Section("delimiter").Key("Times").Times(",")

    //타입을 검사해서 원하는 타입만 골라서 가져올 수 있습니다.
    ValidInts := cfg.Section("Valid").Key("ValidInts").ValidInts(",")
    ValidTimes := cfg.Section("Valid").Key("ValidTimes").ValidTimes(",")

    //특정 타입외의 다른 타입이 들어오면 오류를 발생시킬 수 있습니다.
    StrictInts, err := cfg.Section("Strict").Key("INTS").StrictInts(",")

    //출력하여 setting.ini의 내용을 확인할 수 있습니다.
    fmt.Print(Bool, String, Int, Uint, TimeFormat, Time,
        MustString, MustBool, MustInt, MustUint, MustTimeFormat, MustTime,
        In, InInt, RangeInt, Strings, Ints, Uints, Times,
        ValidInts, ValidTimes, StrictInts)

    //ini 파일에 값을 쓸 수도 있습니다.
    cfg.Section("").Key("Write_Value").SetValue("SetValue")
    cfg.SaveTo("setiing.ini.local")
}
```

setting.ini

``` ini
Write_Value = SetValue

[types]
Bool       = true
String     = hello
Float64    = 1
Int        = 1
Uint       = 1
TimeFormat = 2019-08-10T20:00:00+09:00
Time       = 2019-08-10T20:00:00+09:00

[Must]
MustString     = default
MustBool       = true
MustInt        = 10
MustUint       = 3
MustTimeFormat = 2019-08-10T22:29:57+09:00
MustTime       = 2019-08-10T22:29:57+09:00

[InTypes]
In    = one
InInt = 10

[Range]
RangeInt = 5

[delimiter]
Strings = hello,world
Ints    = 1,2,3
Uints   = 1,2,3
Times   = 2019-08-10T22:29:57+09:00,2019-08-11T22:29:57+09:00

[Valid]
ValidInts  = hello,world,1,2
ValidTimes = 2019-08-10T22:29:57+09:00 , 0001-00-00

[Strict]
INTS = 1,2,3,hello
```

[참고](https://minwook-shin.github.io/read-and-write-ini-files-ini/)

## 정규식 처리

[정규식활용법](http://pyrasis.com/book/GoForTheReallyImpatient/Unit48)

[파일관련](https://flaviocopes.com/go-list-files/)
[파일관련2](https://xoit.tistory.com/3)

[크로스 컴파일](https://brownbears.tistory.com/68)

[Go응용 배송조회](https://subicura.com/2016/06/13/start-go-shipment-tracking-opensource.html)
