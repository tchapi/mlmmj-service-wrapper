# mlmmj-service-wrapper

A very straightforward **init.d** and **systemd** wrapper for mlmmj (http://mlmmj.org) and [mlmmj-simple-web)interface](https://github.com/tchapi/mlmmj-simple-web-interface).

#### init.d

Just add the scripts (remove the `.initd` at the end) in `/etc/init.d` and then `sudo update-rc.d mlmmj defaults`.

#### systemd

Just add the scripts (`.service`) in `/etc/system/systemd` and then `sudo systemctl daemon-reload`.

### Customisation

You want to change the directory of the web interface node index before launching the script :

    WEBSCRIPT="cd /home/yourUser/groups && node index.js -- mlmmjweb"

You can then `sudo service mlmmj start` to start mlmmj as a daemon.
