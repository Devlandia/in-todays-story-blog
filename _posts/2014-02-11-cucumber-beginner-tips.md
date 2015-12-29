---
title: Cucumber Beginner Tips
meta_description: Write declarative features
layout: post
permalink: cucumber-beginner-tips
categories: [bdd, cucumber, rspec, ruby, tdd]
---
####Write declarative features

*Instead of:*
{% highlight cucumber %}
Feature: Signing up

  Scenario: Signing up successfully
    Given I go to the home page
    When I click the link "Sign up"
    And I fill in "Email" with "email@fellipebrito.com"
    And I fill in "Password" with "incorrect"
    And I click the button "Sign up"
    Then I should see "My Account"
{% endhighlight %}

*Use:*
{% highlight cucumber %}
Feature: Signing up

  Scenario: Signing up successfully
    Given I open Google
    When I sign up as "email@fellipebrito.com"
    Then I should be signed im
{% endhighlight %}

####Always insert a narrative
{% highlight cucumber %}
Feature: Using cucumber
  In order to specify and implement new features
  As a software developer
  I want to write down scenarios in Cucumber

  Scenario: Writing a scenario
    Given ...
{% endhighlight %}

####Avoid conjunctive steps

*Instead of:*

{% highlight cucumber %}
# feature

---
When I compose an email to "email@fellipebrito.com" and I send it
---
{% endhighlight %}

*Use:*
{% highlight cucumber %}
# feature

---
When I compose an email to "email@fellipebrito.com"
And I send an email
---
{% endhighlight %}

> Based on <a href="https://twitter.com/clemenshelm" target="_blank">Clemens Helm</a> amazing screencast series: Testing Tuesday

 [1]: http://code.fellipebrito.com/wp-content/uploads/2014/02/url.jpg
