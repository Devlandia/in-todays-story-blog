---
title: Cucumber Beginner Tips
author: fellipe
layout: post
permalink: /2014/02/cucumber-beginner-tips/
perfect_quote_author:
  - 
perfect_quote_where:
  - 
categories:
  - bdd
  - cucumber
  - rspec
  - ruby
  - tdd
---
[<img class="aligncenter size-full wp-image-63" alt="url" src="http://code.fellipebrito.com/wp-content/uploads/2014/02/url.jpg" width="265" height="190" />][1]<span style="line-height: 1.5;"> </span>**Write declarative features**

*Instead of:*

<pre class="lang:sh decode:true" title="Wrong way to write features">Feature: Signing up

  Scenario: Signing up successfully
    Given I go to the home page
    When I click the link "Sign up"
    And I fill in "Email" with "email@fellipebrito.com"
    And I fill in "Password" with "incorrect"
    And I click the button "Sign up"
    Then I should see "My Account"</pre>

*Use:*

<pre class="lang:sh decode:true" title="Write declarative features">Feature: Signing up

  Scenario: Signing up successfully
    Given I open Google
    When I sign up as "email@fellipebrito.com"
    Then I should be signed im</pre>

**Always insert a narrative**

<pre class="lang:sh decode:true" title="Always insert a narrative">Feature: Using cucumber
  In order to specify and implement new features
  As a software developer
  I want to write down scenarios in Cucumber

  Scenario: Writing a scenario
    Given ...</pre>

**Avoid conjunctive steps  
***Instead of:*

<pre class="lang:sh decode:true" title="Conjunctive Steps"># feature

---
When I co,pose an email to "email@fellipebrito.com" and I send it
---</pre>

*Use:*

<pre class="lang:sh decode:true" title="Avoiding conjunctive steps"># feature

---
When I compose an email to "email@fellipebrito.com"
And I send an email
---</pre>

> Based on <a href="https://twitter.com/clemenshelm" target="_blank">Clemens Helm</a> amazing screencast series: Testing Tuesday

 [1]: http://code.fellipebrito.com/wp-content/uploads/2014/02/url.jpg