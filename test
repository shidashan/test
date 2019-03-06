package main

import (
	"fmt"
	"regexp"
)

var reg = regexp.MustCompile("^[\u4e00-\u9fa5_a-zA-Z0-9]$")

func main() {
	str := ":1000\r\n+"
	StrFilterNon(&str)
	fmt.Println(str)
}

func StrFilterNon(src *string) {
	results := ""
	for _, c := range *src {
		if reg.MatchString(string(c)) {
			results += string(c)
		}
	}

	*src = results
}
