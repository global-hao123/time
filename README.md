# Time UI component

A UI component which can get the server time, get a Date object's calendar format and set a Date object's time zone.

## Compatibility

- IE 6-10, Firefox, Opera, Chrome, Safari
- ltr / rtl
- Windows / Mac

## Usage

All the functions are encapsulated into `Gl.time()`, which is under `Gl` namespce.

Get server time(it will return a Date object), with the optional param, you can also set a callback function:

```
/**
 * Gl.time.getTime(callback);
 * @param {function} callback (optional)
 */
var date = Gl.time.getTime();
var date2 = Gl.time.getTime(function () {
    console.log("success");
});
```

And also, you can get the server time by a global variable(it's a Date object):

```
var date = Gl.serverNow;
```

----------------------

Get a Date object's calendar format(without the optional param, it will use the server time):

```
/**
 * Gl.time.getForm(date);
 * @param {Date} date (optional)
 */
var format = Gl.time.getForm();

var date = new Date();
var format2 = Gl.time.getForm(date);
```

It will return an Object like this:

```
{
    CD: "三十",
    CM: "十月",
    IM: "المحرم",
    IW: "الاثنين",
    M: "Dezembro",
    W: "Seg",
    cd: 30,
    cm: 10,
    d: "02",
    gd: "壬寅",
    gm: "癸亥",
    gy: "癸巳",
    hh: 18,
    id: 29,
    im: 1,
    isleap: false,
    iw: 2,
    iy: 1435,
    jd: 2456628,
    m: 12,
    mm: 14,
    ss: 41,
    sx: "蛇",
    thy: 2556,
    w: 1,
    y: 2013
}
```

----------------------

Set time zone to a Date Object:

```
/**
 * Gl.time.setTimezone(tz, date);
 * @param {String} tz Time zone which you wanna set
 * @param {Date} date {optional}
 */
var tz8 = Gl.time.setTimezone('+8');
var tzm2 = Gl.time.setTimezone('-2');

var date = new Date();
var tz3 = Gl.time.setTimezone('+3', date);
```

## Release History

* 2013/12/02 - v1.1.0
    - Add setTimezone function.

## Authors

* [fengkun](http://gitlab.pro/u/fengkun)
* [wangmingfei](http://gitlab.pro/u/wangmingfei)

