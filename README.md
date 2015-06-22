# AimBrain Mobile Web/Browser SDK

## JavaScript Integration Code

```javascript
<!-- AimBrain -->
<script>
(function(cid, uid, uidstatic) {
    // Create AimBrain Object
    abo = (window.AimBrainObject = {});
    abo.teq = []; abo.uid = uid; abo.cid = cid;
    abo.static = uidstatic;

    // Start collecting touch events
    function th(e) { abo.teq.push(e); }
    ael = addEventListener;
    ael("touchstart", th, true);
    ael("touchmove", th, true);
    ael("touchend", th, true);
    ael("touchcancel", th, true);

    // Load consumption script
    var se = document.createElement('script'),
    fs = document.getElementsByTagName('script')[0];
    se.async = 1; se.src = 'https://cdn.aimbrain.com/1/tc.js';
    fs.parentNode.insertBefore(se, fs)
})('client-id-or-apikey', 'unique-id-per-user', false);
</script>
<!-- End AimBrain -->
```

Place the above script between `<head></head>` tags.

## Object Parameters

`client-id-or-apikey` (*String*) - constant value which can be obtained by emailing founders [] aimbrain.com.

`unique-id-per-user` (*String*) - unique id per user (can be a temporary ID before static ID is known).

`uidstatic` (*Boolean*) - flag to indicate if static user ID is known (true), otherwise implies temporary ID (false).
