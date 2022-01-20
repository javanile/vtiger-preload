# 🐯 vtiger (preload)

This is where we discuss and decide once and for all how to implement preload in vtiger.

## What is 'preload'?

The 'preload' is a PHP section used to run code before every kind of requests and foreach requests the appliation in exposed.
This is a middle stage between configuration file loading and application entrypoints.

![Stages](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/javanile/vtiger-preload/main/stages.puml)

