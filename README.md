GoOse
=====

Html Content / Article Extractor in Golang

This is a golang port of "Goose" originaly licensed to Gravity.com
under one or more contributor license agreements.  See the NOTICE file
distributed with this work for additional information
regarding copyright ownership.

Golang port was written by Antonio Linari

Gravity.com licenses this file
to you under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

INSTALL
=======
go get github.com/advancedlogic/GoOse

HOW TO USE IT
=============

```Go
package main

import (
	"github.com/advancedlogic/GoOse"
)

func main() {
	g := goose.New()
	article, _ := g.ExtractFromURL("http://edition.cnn.com/2012/07/08/opinion/banzi-ted-open-source/index.html")

	println("> title", article.Title)
	println("----------------------")
	println("> description", article.MetaDescription)
	println("----------------------")
	println("> keywords", article.MetaKeywords)
	println("----------------------")
	println("> content", article.CleanedText)
	println("----------------------")
	println("> url", article.FinalURL)
	println("----------------------")
	println("> top node", article.TopNode)
	println("----------------------")
	println("> top image", article.TopImage)
	println("----------------------")
}
```

TODO
====

- [ ] better organize code
- [ ] add comments and godoc
- [ ] improve "xpath" like queries
- [ ] add other image extractions techniques (imagemagick)

THANKS TO
=========
```
@Martin Angers for goquery
@Fatih Arslan for set
GoLang team for the amazing language and net/html
```
