# flutter-dart

`.vscode/settings.json`
=======================
1. Disable auto-format because I am not keen with default dart style
2. Hide 80 chars line 
3. Disable closing labels

```json
{
    "[dart]": {
        "editor.formatOnSave": false,
        "editor.formatOnType": false,
        "editor.rulers": [],
    },
    "dart.closingLabels": false
}
```

Routes
======
1. In `main.dart`, when you create `MaterialApp`, configure
   routes property as follows:
   ```dart
    ...
      home: HomePage(),
      routes: {
//      "/" :    (_) => HomePage(),     // redundant if home property is already set
        "/1":    (_) => FirstPage(),
        "/2":    (_) => SecondPage(),
      },
    ...
   ```

2. to make navigation to any defined route, this example makes
    navigator go to defined route '/1' 
    ```
        Navigator.pushNamed(context, "/1");
    ```

3. to get back, you can use same method as above or just use `Navigator.pop(context)` 
   which is similar to `window.history.back()` in javascript

4. if `home` property is set, you don't have to define a route named `"/"`