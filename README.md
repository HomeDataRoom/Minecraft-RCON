# Minecraft RCON
A fork of a simple Minecraft RCON Web Console using PHP, Bootstrap and JavaScript. Currently in active development.

Inspired by [Minecraft-RCON-Console](https://github.com/ekaomk/Minecraft-RCON-Console) and using [PHP-Minecraft-Rcon](https://github.com/thedudeguy/PHP-Minecraft-Rcon).
## Configuration

1. Edit your Minecraft server `server.properties` configuration file in order to enable RCON:
```
enable-rcon=true
rcon.port=25575
rcon.password=xtMJsVtmx0XypuId7jIb
```
2. Restart your Minecraft server.
3. Download/Clone the Minecraft RCON Web Console files and edit the `config.php` file. Use the same rcon password and port that you used in `server.properties`:
```
$rconHost = "localhost";
$rconPort = 25575;
$rconPassword = "xtMJsVtmx0XypuId7jIb";
```

## Warnings

* Provided as it is, **this console has no authentication check**, so anybody with access to this console can run any commands on the Minecraft server. Please check the documentation below about how to set up basic HTTP authentification on your web server, in order to restrict the access to the console:
 * [For Apache 2.4 users](https://httpd.apache.org/docs/2.4/howto/auth.html)
 * [For NGinx users](https://nginx.org/en/docs/http/ngx_http_auth_basic_module.html)
* Use a strong custom RCON password for more security. Do not use the default one in `config.php`.
* Set up your firewall in order to allow only the web server to communicate with the Minecraft server through the RCON port set, for more security.