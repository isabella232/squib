[![Gem Version](https://badge.fury.io/rb/squib.svg)](https://rubygems.org/gems/squib)
[![Build Status](https://secure.travis-ci.org/andymeneely/squib.svg?branch=master)](https://travis-ci.org/andymeneely/squib)
[![Dependency Status](https://gemnasium.com/andymeneely/squib.svg)](https://gemnasium.com/andymeneely/squib)

# Squib

Squib is a ruby DSL for prototyping card and board games. Think of it like [nanDeck](http://nandeck.it) done "the Ruby way". Start with some basic commands and generate print-ready PNGs and PDFs. 

Squib is currently pre-release alpha. 

```ruby
require 'squib'

Squib::Deck.new(width: 825, height: 1125, cards: 3) do
  background color: [1.0,1.0,1.0]
  data = xlsx file: 'sample.xlsx'

  rect x: 15, y: 15, width: 795, height: 1095, x_radius: 50, y_radius: 50

  text str: data['name'], x: 250, y: 55, font: 'Arial 54'
  text str: data['level'], x: 65, y: 40, font: 'Arial 72'

  png file: 'icon.png', x: 665, y: 30

  save format: :png
end
```

## Installation

Add this line to your application's Gemfile:

    gem 'squib'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install squib

Note: Squib is based on the `cairo` and `pango` extensions, which require at least Ruby 2.0

## API

API docs to be written. See the `samples` directory.

## Contributing

1. Fork it ( https://github.com/[my-github-username]/squib/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
