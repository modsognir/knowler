Rundown
=======

[![Gem Version](https://badge.fury.io/rb/rundown.png)](http://badge.fury.io/rb/rundown) [![Build Status](https://travis-ci.org/modsognir/rundown.png)](https://travis-ci.org/modsognir/rundown) [![Code Climate](https://codeclimate.com/github/modsognir/sentiment_parser.png)](https://codeclimate.com/github/modsognir/sentiment_parser) [![Coverage Status](https://coveralls.io/repos/modsognir/rundown/badge.png)](https://coveralls.io/r/modsognir/rundown)

Rundown is a simple Natural Language Processor built with Ruby, inspired by [Knwl.js](https://github.com/loadfive/Knwl.js). Rundown scans through text, user data, or just about anything for likely data of interest, phone numbers, dates, locations, emails, times, as well as likelyhood of spam and overall emotion.

## Installation

Add this line to your application's Gemfile:

    gem 'sentiment_parser'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install sentiment_parser

## Usage

    rd = Rundown.parse("I'll see you on the 18th, give me a ring on 07912 345 678. - Jerertt, me@example.com")
    
    rd.emails
    => ["me@example.com"]

    rd.phones
    => ["07912 345 678"]

    rd.sentiment
    => -0.5333

    rd.dates
    => [#<Date: 2013-12-18>]

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

###Known Issues

* Phone numbers need country code

###Licence

Project released under an MIT license.
