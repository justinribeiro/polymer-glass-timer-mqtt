# &lt;glass-timer&gt;

> Custom element that connects to a MQTT broker and listens for millisecond data from Google Glass.

## The setup

For this to work, a few things are needed.

1. You need a broker that implements websockets. I built Mosquitto's 1.4 branch with libwebsockets and use that on Google Compute Engine.
2. You need to edit, build and side load my GDK glass timer example (see [justinribeiro/glass-gdk-timer-mqtt](https://github.com/justinribeiro/glass-gdk-timer-mqtt)).
3. This tag utilizes [Eclipe Paho's JavaScript client](http://www.eclipse.org/paho/clients/js/). The version included here is not minified.

## Install

Install the component using [Bower](http://bower.io/):

```sh
$ bower install justinribeiro/polymer-glass-timer-mqtt --save
```

Or [download as ZIP](https://github.com/polymer-glass-timer-mqtt/archive/master.zip).

## Usage

1. Import Web Components' polyfill:

    ```html
    <script src="bower_components/platform/platform.js"></script>
    ```

2. Import Custom Element:

    ```html
    <link rel="import" href="bower_components/polymer-glass-timer-mqtt/glass-timer.html">
    ```

3. Start using it!

    ```html
    <glass-timer></glass-timer>
    ```

## Options

Host and Port are required. I would sersiouly consider changing the default topic as well. :-)

Attribute     | Options     | Default      | Description
---           | ---         | ---          | ---
`title`       | *string*    | `Glass Timer` | Title of the timer
`host`        | *string*    | ``            | Hostname/IP address of your broker w/websocket
`port`        | *int*       | ``            | Port your broker w/websocket is running on
`topic`        | *string*       | `#`            | Topic on broker to listen to
`debug`       | *bool*      | false         | Enable console.log debugging

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

For detailed changelog, check [Releases](https://github.com/justinribeiro/polymer-glass-timer-mqtt/releases).

## License

[Apache 2 License](http://opensource.org/licenses/Apache-2.0)
