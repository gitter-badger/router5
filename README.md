[![npm version](https://badge.fury.io/js/router5.svg)](http://badge.fury.io/js/router5)
[![Build Status](https://travis-ci.org/router5/router5.svg)](https://travis-ci.org/router5/router5)
[![Coverage Status](https://coveralls.io/repos/router5/router5/badge.svg)](https://coveralls.io/r/router5/router5)

# router5

Official website: [router5.github.io](http://router5.github.io)

A simple but powerful HTML5 router, based on [route-node](https://github.com/troch/route-node)
and [path-parser](https://github.com/troch/path-parser).

## What is it?

It is an __HTML5 router__, using history and organising __named routes__ in a __tree__. Browser support
is limited to modern browsers implementing session history: [http://caniuse.com/#search=history](http://caniuse.com/#search=history).

Router 5 supports use of hash in URL, but session history is still required: deciding
to use a hash or not is therefore not a decision based on browser support, but rather a decision based
on server capabilities!

It is aimed at applications rendering a tree of components, but can easily be used elsewhere.
This router is library and framework agnostic, and makes no asumption on your implementation.
It favours __convention over configuration__, by giving you the means to observe route changes
and to react to them. Afterall, why treat route changes any different than data changes?

You can read more about motivations behind it here: [Why router5?](http://router5.github.io/docs/why-router5.html).

To get started, look here: [Get started](http://router5.github.io/docs/why-router5.html)

## Features

- __Use of hash (#)__
- __Default start route__: a default route to navigate to on load if the current URL doesn't match any route. Similar to `$routeProvider.otherwise()` in _Angular ngRoute_ module.
- __Start__ and __stop__
- __Nested named routes__: routes are identified by names and parameters so you don't have to manipulate URLs
directly. Routes can be nested, introducing the notion of _route segments_.
- __Route change listeners__: listen to any route change, or register listeners for a specific route.
- __Route node change listeners__: you can add listeners to be triggered on a specific named route node. They will be triggered if that named route node is the node a component tree needs to be re-rendered from.
- __Segments activation__: you can control whether or not a route can be accessed by specifying a `canActivate`
function per node. Supports asynchronous results.
- __Segments deactivation__: you can register segment components. On a route change, it will ask those components through their `canDeactivate` method if they allow navigation. Similar to _Angular 2_ and _Aurelia_ routers. Supports asynchronous results.
- __Universal JavaScript__: use on client or server side
- __You are in control!__ You decide what to do on a route change and how to do it.


## Guides

- [Configuring routes](http://router5.github.io/docs/configuring-routes.html)
- [Path syntax](http://router5.github.io/docs/path-syntax.html)
- [Listeners](http://router5.github.io/docs/listeners.html)
- [Navigation](http://router5.github.io/docs/navigation.html)
- [Allowing navigation](http://router5.github.io/docs/preventing-navigation.html)
- [Universal applications](http://router5.github.io/docs/universal-applications.html)

## API

- [API Reference](http://router5.github.io/docs/preventing-navigation.html)

## Examples

- [With React](http://router5.github.io/docs/with-react.html)

## Related

- [path-parser](https://github.com/troch/path-parser)
- [route-node](https://github.com/troch/route-node)
- [router5-react](https://github.com/router5/router5-react)
- [router5-deku](https://github.com/router5/router5-deku)
