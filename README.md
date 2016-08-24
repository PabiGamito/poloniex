# Poloniex

[![Gem Version](https://badge.fury.io/rb/poloniex.png)](http://badge.fury.io/rb/poloniex)

This gem provides a ruby wrapper to the poloniex.com api: [Link](https://poloniex.com/api)
## Installation

Add this line to your application's Gemfile:

    gem "poloniex", :git => "git://github.com/PabiGamito/poloniex.git"

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install poloniex

## Usage

All methods provided by ```Poloniex``` are class methods, and are of the same name as the api ( except that "return"s have been removed ).

For example, ```https://www.poloniex.com/public?command=returnTicker``` is written as ```Poloniex.ticker```

The Poloniex module accepts a setup block for configuration:

```
Poloniex.setup do | config |
    config.key = 'my api key'
    config.secret = 'my secret token'
end
```

GET requests ( to /public ) do not need authentication, and therefor do not need Poloniex to be configured.

POST requests ( to /tradingApi ) will need authentication, and you will have to have your own key and secret token.



## Contributing

1. Fork it
2. Commit your changes (`git commit -am 'Add some feature'`)
3. Push to your forked repository (`git push`)
4. Create a new Pull Request
