[![Build Status](https://travis-ci.org/asafschers/goscore.svg?branch=master)](https://travis-ci.org/asafschers/goscore)
[![Go Report Card](https://goreportcard.com/badge/github.com/asafschers/goscore)](https://goreportcard.com/report/github.com/asafschers/goscore)
[![Coverage Status](https://coveralls.io/repos/github/asafschers/goscore/badge.svg?branch=master)](https://coveralls.io/github/asafschers/goscore?branch=master)
[![GoDoc](https://godoc.org/github.com/asafschers/goscore?status.svg)](https://godoc.org/github.com/asafschers/goscore)
# Goscore

Go scoring API for Predictive Model Markup Language (PMML).

Currently supports Decision Tree, Random Forest and Gradient Boosted Models

Will be happy to implement new models by demand, or assist with any other issue.

Contact me here or at aschers@gmail.com.

## Installation

```
go get github.com/asafschers/goscore
```
## Usage

### Random Forest / Gradient Boosted Model

[Generate PMML - R](https://github.com/asafschers/scoruby/wiki) 

Score by PMML -

```go

modelXml, _ := ioutil.ReadFile("fixtures/model.pmml")
var model goscore.RandomForest // or goscore.GradientBoostedModel
xml.Unmarshal([]byte(modelXml), &model)
score, _ := model.Score(tt.features, "1") // gbm.score doesn't recieve label

```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/asafschers/goscore. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

