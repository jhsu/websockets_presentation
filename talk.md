!SLIDE

# Overview of WebSockets

Joseph Hsu

@jhsu

!SLIDE
## no more nagging

* AJAX polling
* Adobe&reg; Flash&reg; socket
* =(

!SLIDE
## Handshake

@@@ js
    var ws = new WebSocket("ws://echo.websocket.org");
@@@

!SLIDE

## Callbacks

!SLIDE
## onopen

@@@ js
    ws.onopen = function(evt) {
      alert('Let the user know we are connected');
    }
@@@

!SLIDE
## onclose

@@@ js
    ws.close = function(evt) {
      alert('Connection closed.');
    }
@@@

!SLIDE
## onmessage

@@@ js
    ws.onmessage = function(evt) {
      data = evt.data;
      // do magic
    }
@@@

!SLIDE
## Send message

@@@ js
    ws.send("some message / data");
    // or maybe some JSON?
    ws.send("{nickname: 'jhsu', message: 'Hello Everybody!'}");
@@@

!SLIDE
## [Chat](http://jhsu.github.com/websockets-barcamp/test.html)

!SLIDE
## Too lazy to make my own websocket server

* [Pusher.com](pusher.com)


!SLIDE
## [Browser Support](http://caniuse.com/websockets)

* some security issues with the [way it does its handshake](http://www.ietf.org/mail-archive/web/hybi/current/msg04744.html)

!SLIDE
## Using fallbacks

* [Socket.io](http://socket.io/)
* [Faye](http://faye.jcoglan.com/)

!SLIDE
## ws.disconnect(); // THE END
