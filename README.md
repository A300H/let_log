# let_log

LetLog is a log system that supports both IDE and in-app display, and supports log and network

Language: [English](README.md) | [中文简体](README_ZH.md)

## Getting Started

API inspired by web

**Example code**

```dart
// log
Console.log("this is log");

// debug
Console.debug("this is debug", "this is debug message");

// warn
Console.warn("this is warn", "this is a warning message");

// error
Console.error("this is error", "this is a error message");

// test error
try {
    final aa = {};
    aa["aaa"]["sdd"] = 10;
} catch (a, e) {
    Console.error(a, e);
}

// time test
Console.time("timeTest");
Console.endTime("timeTest");

// log net work
Console.net(
    "api/user/getUser",
    data: {"user": "yung", "pass": "xxxxxxx"},
    head: null,
);
Console.endNet(
    "api/user/getUser",
    data: {
    "users": [
        {"id": 1, "name": "yung", "avatar": "xxx"},
        {"id": 2, "name": "yung2", "avatar": "xxx"}
    ]
    },
);

// log net work
Console.net("ws/chat/getList", data: {" chanel": 1}, type: "Socket");
Console.endNet(
    "ws/chat/getList",
    data: {
    "users": [
        {"id": 1, "name": "yung", "avatar": "xxx"},
        {"id": 2, "name": "yung2", "avatar": "xxx"}
    ]
    },
);

// clear log
// Console.clear()
```

> For a detailed example, please refer to [here](example/lib/main.dart).

**IDE Display results**

![Let Log](images/ide.png)

**Display logs in the app**

```dart
Widget build(BuildContext context) {
    return Console();
}
```

> For a detailed example, please refer to [here](example/lib/main.dart).

**App log**

![Let Log](images/log.png)

**App network**

![Let Log](images/net.png)

**App search**

![Let Log](images/search.png)

**Setting**

Custom category names

```dart
// setting
// Console.enabled = false;
// Console.maxLimit = 10;
// Console.showAsReverse = true;
Console.setNames(
    log: "😄",
    debug: "So_1F41B",
    warn: "❗",
    error: "❌",
    request: "So_2B06_️",
    response: "⬇️",
);
```

Results:

![Let Log](images/name.png)

## Feature

-   [x] Support for both IDE printing and in-app presentation

-   [x] Also supports logging, error, time statistics, network and other information output.

-   [x] Interface imitates the web console class, providing log, debug, warn interface, error, time, endTime, net, endNet, etc.

-   [x] Support for filtering log content by category

-   [x] Support for filtering log content by keywords

-   [x] Support for copy log content

-   [x] Serves as both Http and Socket

-   [x] Statistics for network support packet size, duration

-   [x] Support for custom log category symbols, you can use emoji sentiment as a sort if you like.

-   [x] Multi-colored output logs within the app to make error logs more visible

-   [x] Support for automatic switching between black and white skin according to the app

-   [x] Support for some custom logging settings

## github

> [https://github.com/yungzhu/let_log](https://github.com/yungzhu/let_log)

If you like it, give it a star, thanks.
