---
title: Hello World!
meta_description: there has been an awakening in the force.
author: fellipe
layout: post
permalink: hello-world
categories:
  - rspec
  - rubocop
  - ruby
---
Here we go!

**spec/lib/hello_spec.rb**
{% highlight ruby %}
require 'spec_helper'
require 'hello'

describe HelloWorld do
  it 'is quoted by Fellipe Brito' do
    hello_world = HelloWorld.new
    expect(hello_world.author).to be == 'Fellipe Brito'
  end

  it 'starts with empty quote' do
    hello_world = HelloWorld.new
    expect(hello_world.quote).to be == ''
  end

  it 'says Hello World!' do
    hello_world = HelloWorld.new
    hello_world.quote = 'Hello World!'
    expect(hello_world.quote).to be == 'Hello World!'
  end

end
{% endhighlight %}

**lib/hello.rb**
{% highlight ruby %}
class HelloWorld
  attr_accessor :author, :quote

  def initialize
    @author = 'Fellipe Brito'
    @quote = ''
  end
end
{% endhighlight %}

**rubocop**
{% highlight bash %}
[~/dev/hello]$ rubocop lib/hello.rb
Inspecting 1 file
1 file inspected, no offences detected
{% endhighlight %}

**rspec**
{% highlight bash %}
[~/dev/hello]$ rspec spec/lib/hello_spec.rb
...

Finished in 0.00156 seconds
3 examples, 0 failures
{% endhighlight %}
