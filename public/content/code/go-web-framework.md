+++
author = "Tin NG"
date = "2016-12-28T23:16:29+07:00"
description = ""
tags = []
title = "The best Golang web framework for you"

+++

# Don't use framework

The standard library has everything you need.

The power of Go doesn't lie in concurrency like you may imagine. But instead in the design of `interfaces`.

Say in Go, you have a function that accepts an interface as a parameter. And you have another `struct` that implement every method of that interface. Then this struct is acceptable for the function. 

To a larger scope, every struct that implement all the methods of that interface is eligible for the function.

Now imagine this. You're developing a web application in Golang, and the router is getting slower (for example), and you want to replace the it by something faster than the standard library one. 

This would be problematic if you use a web framework cause everything would be glued in 1 piece. On the other hand, you can just find a router implementation on Github and plug it in seamlessly. Because the opensource router was implemented to conform to the standard library `router` interface, so that your program would accept it with no problem at all.

You can read up more about interfaces at [http://jordanorelli.com/post/32665860244/how-to-use-interfaces-in-go](http://jordanorelli.com/post/32665860244/how-to-use-interfaces-in-go)
