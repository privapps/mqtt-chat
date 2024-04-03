## Ad hoc E2E Encrypted Group Chat

### What
This project is a fully functional, minimalist, ad hoc, end-to-end encrypted web group chat. It uses MQTT as backend for all message delivery which is more reliable than WebRTC.

### Why
After concluding the [Go group chat](https://github.com/privapps/gchat/), I am now seeking a more standardized backend solution, moving away from self-invented protocols. One such option is the Simple (or Streaming) Text Orientated Messaging Protocol (STOMP). Additionally, MQTT, with its support for WebSockets, presents another viable alternative. My interest is piqued particularly by MQTT's availability of free public servers, making it a natural choice for exploration.

### How
The backend is replaced with free public MQTT Server which supports websocket.

On the client side, I did minimum changes which is similar as my [go group chat](https://github.com/privapps/gchat/). It uses plain javascript without any framework.

### Note
Due to MQTT's design catering to high-latency and unreliable networks, if your chat agent becomes disconnected, your mobile screen turns off for example, upon reconnection, the server seamlessly **replays** any missed messages. This feature proves invaluable, ensuring uninterrupted communication flow. By the way, you can try this with public mqtt emqx broker.

### Demo
A live demo is at https://privapps.github.io/mqtt-chat/

