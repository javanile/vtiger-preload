# 🐯 vtiger (preload)

This is where we discuss and decide once and for all how to implement preload in vtiger.

## What is 'preload'?

The 'preload' is a PHP section used to run code before every kind of requests and for each requests to which the application is targeted.
This is a middle stage between configuration loading and application entrypoints or runtime.

## Why 'preload' is important?

Complex application can have differents entrypoints, for examples vtiger supports various [entrypoints](#vtiger-entrypoints). This means that if I want a portion of my custom code is executed into all of entrypoints I need to copy it into everyone, this is bad. This is the main reason why we need to define an offial 'preload' stage for all developer. For vtiger develper this means that 'preload' is before `Loader.php` but after `config.inc.php`.

### Vtiger entrypoints

Here all the official PHP entrypoints supported by vtiger are listed. Any entrypoint not present in this list should not perform the 'preload' stage.

- index.php
- webservice.php

### Application stages

![Stages](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/javanile/vtiger-preload/main/stages.puml)
