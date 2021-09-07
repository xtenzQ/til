# Spring Bean Lifecycle

Bean lifecycle looks like this:
`Container started` -> `Bean instantiated` -> `Dependencies Injected` -> `Internal Spring Processing` -> `Init Method` -> `Bean is ready to use` -> `Custom destroy method` -> `Stop`

Spring container creates singleton instance by default.
Two most popular scopes are: **singleton**, **protoype** (creates new bean instance for each request).

For prototype instance, Spring doesn't call the `destroy method`. Container hands prototype instance to the client so the client should release its resources. To build custom destroy method we should create a **custom bean processor** to keep track of **prototype scope beans**, it should also implement `DisposableBean` interface. Also we can ignore `destroy-method` attribute in config.

<hr>

[Return](../../../)