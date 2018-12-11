# Building a Realtime Websocket API in Phoenix

## Abstract

Sometimes consumers of your APIs require near-realtime communication because regular RESTful HTTP apis can be a few milliseconds too slow. These performant and scalable APIs can be made over websocket TCP connections where events are pushed from client and server in near-realtime fashion.

This talk is a story of how I built such an API. We'll look at why this decision to create a websocket API was made and we will take a look at the data that supported this decision. We will take a deep dive into Phoenix websockets, channels, and transports to expose the underlying architecture. Finally, we look at how we tested the API, how we authenticated users over the channels, and how Phoenix helped this all happen with relative ease.

## Details

This is a rough outline of the talk and a list of some of the points to be covered.

* Description of what we were trying to build and the problem we were facing
* Data showing the response times between http endpoint calls and websocket events
* Benefits and drawbacks of polling vs. websockets
* What we did to get users to be able to connect to the websocket API
* What the role of channels are in Phoenix
* Working with channels vs raw websockets in Phoenix
* How different clients (JS vs iOS vs server) can connect to the Websocket API
* What the role of transport is in Phoenix
* What is the difference between PubSub and channels in Phoenix
* How we used the presence API in Phoenix
* How we tested joining channels
* How we tested incoming events
* How we tested outgoing events
* How we implemented authorization in the channels
