# Today I Learned 

![TIL](assets/images/what_did_you_learn_today.png "TIL")

## Description

Following from [hashrocket](http://til.hashrocket.com) we thought it would be good to do the same for [belfast elixir](http://www.belfastelixir.org).

## Contribution

### Does it have to be about Elixir?

No, not really. It can be workflow related (like a short cut in vim or vscode) or it can be about TDD or DDD. However it wouldn't make much sense to have an article on Django here (unless they tie in with Elixir somehow). So you know, use your common sense :)

### How do I contribue

#### Fork it!

[Fork](https://help.github.com/en/articles/fork-a-repo) the repo.

#### Ask us!

If we know you ask [holsee](https://www.github.com/holsee) or [swm](https://www.github.com/swmcc) to be added as a contributor. Create a branch then put up a PR. 

Any questions about contribution can be answered in the `#beam` room in the [Irish Tech Community](http://irishtechcommunity.com/)

#### Adding an article

To add a new article you simply create a new file in the `_posts` directory. The file must conform the following convention:

`YYYY-MM-DD-then-the-title.html`

The page is a mix of `html` and `yaml`. The first portion is `yaml` and holds metadata of the post and looks like this:

```YAML
---
layout: default
title: "The First Post"
date: 2019-07-04 01:03:00 +0000
published: 2019-07-04 01:03:00 +0000
comments: true
categories: development
tags: [something, something2]
github: "https://github.com/alainpham/quarkus-kafka-camel-servlet"
---
```

All fairly self explanatory. The main body of the post is written in `html` so its pretty easy to write the body of the blog post. The first two paragraphs should be used as a general introduction to the article. This isn't a hard rule but plesae ensure you have an introduction for the blog post. After your introduction please use:

```HTML
<!--more-->
```

If using system commands please keep them within a `<pre></pre>`.
If using a programming language please use:

```liquid
{% highlight java %}
package agilabs;
import javax.enterprise.event.Observes;
import javax.enterprise.inject.Produces;
import javax.inject.Inject;
import org.apache.camel.CamelContext;
import org.apache.camel.ProducerTemplate;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import io.quarkus.camel.core.runtime.InitializedEvent;
import io.smallrye.reactive.messaging.annotations.Emitter;
import io.smallrye.reactive.messaging.annotations.Stream;

public class CamelWiring{
```

All articles should have a title, use the default layout, be correctly timestamped and have tags associated with it.

Please use the information below to start an instance of the site and check that it renders correctly.

## Development Info

This repo uses [rvm](https://rvm.io/). Please ensure you have it installed before proceeding.

```
git clone git@github.com:belfastelixir/til.belfastelixir.org.git
cd til.belfastelixir.org
gem install bundler
bundle
jekyll s
```