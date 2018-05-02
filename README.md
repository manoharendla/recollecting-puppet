# recollecting-puppet
A guide to recollect puppet


### Stage resoruce type  in puppet
Run stages are an additional way to order resources. They allow groups of classes to run before or after nearly everything else, without having to explicitly create relationships with every other class.

A complete run stage example:
```ruby
stage { 'pre':
  before => Stage['main'],
}

class { 'apt-updates':
  stage => 'pre',
}```
