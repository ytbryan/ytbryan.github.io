---
title: Hello world!
author: ytbryan
layout: post
permalink: /hello-world/
categories: work startup uncategorized
tags:
dsq_thread_id:
  - 2292154959
---

I wrote this article to remind myself about Pyspark and Spark.
Two technologies that I grow to love.

Spark is a wonderful technology for processing large amount of data.

In this tutorial, I will be using Pyspark, a Python wrapper around the
spark API to interact with Spark. For a background, Spark is a technology
written in Scala.

## Background
> Software required: Homebrew, Spark, PySpark, Pip, Pyenv
> Machine used: MacOS and Macbook

## Installing Spark

```
brew install spark
```
## Installing Python 3.x
> MacOS comes with python 2.x

To use the latest python, which I recommend, simply:

```
brew install python3
```
A common irritation is to call python 3.x code using `python3`
to fix this small annoyance, simply use `aka generate py="python3"`
to generate an alias

> most tutorial teaches the tetious way of setting up spark.
> But not in this tutorial.

## Installing PySpark

```
pip install pyspark
```

I digress, Python has a distribution problem of 2.x and 3.x.
To fix this, use `pyenv local 2.7` or `pyenv local 3.5`

And because of legacy issues, we will encounter syntax issues.
Most syntax issues can be resolved by a simple parentheses ()
`e.g print "something" should be print("something")`


## To run pyspark

```
  pyspark
```

Go to localhost:4040 to see a spark UI running in browser.


## To run sample Code
simply run
```
  spark-submit pi.py
```
The sample code can be found in `example/src/main/python` of all spark 2.x distribution
