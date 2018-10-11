*Backup, restore, and sync the prefs and settings*
[dotfiles](https://dotfiles.github.io/)

```javascript 
function getGeoByIp(request, reply) {
  const ipAddress = requestIp.getClientIp(request);

  const defaultCountry = { country: 'NL', continent: 'EU' };
  if (ipAddress === 'localhost' || ipAddress === '127.0.0.1') {
    reply(defaultCountry);
  } else {
    geoip2.lookupSimple(ipAddress, (err, result) => {
      if (err || !result) {
        reply(defaultCountry);
      } else if (result) {
        reply(result);
      }
    });
  }
}
```