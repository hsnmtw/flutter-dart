# flutter-dart

VSCode settings.json
====================
```json
{
    "[dart]": {
        "editor.formatOnSave": false,
        "editor.formatOnType": false,
        "editor.rulers": [],
        "editor.inlineSuggest.enabled": false,
        "editor.parameterHints.enabled": false,
    },
    "dart.closingLabels": false
}
```

Routes
======
1. In `main.dart`, when you create `MaterialApp`, configure
   routes property as follows:
   ```
    ...
      home: HomePage(),
      routes: {
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