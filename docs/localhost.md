# Localhost Workaround

In an effort to increase security, [Microsoft has blocked modern applications from connecting to localhost](https://stackoverflow.com/questions/33259763/uwp-enable-local-network-loopback/33263253#33263253) by default. 

Fortunately, there is a temporary workaround available. Please run this command in command prompt after installing Nightingale:

```
checknetisolation loopbackexempt -a -p=S-1-15-2-2472482401-1297737560-3464812208-2778208509-1273584065-1826830168-474783446
```

If you continue to see connection errors to localhost after running the above command, try disabling SSL validation in Nightingale's settings. This is often needed when connecting to a local IIS Express server.

We apologize for the inconvenience, and we appreciate your understanding as we work towards a better solution.

## More helpful links

Description | Link
--- | ---
Official Microsoft docs explaining that UWP apps installed from the store aren't allowed to make network calls to the device they're installed on. | https://docs.microsoft.com/en-us/windows/uwp/debug-test-perf/deploying-and-debugging-uwp-apps#debugging-options
Windows Platform UserVoice requesting for network loopback support. | https://wpdev.uservoice.com/forums/110705-universal-windows-platform/suggestions/36604855-allow-localhost-loopback-capability-in-uwp-apps-de