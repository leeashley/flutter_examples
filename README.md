# Flare
<p align="center">
<img src="https://docs.google.com/uc?id=18gnZn8IBZS9noe_7LA0COiQ5yWPVqfBu" height="649" width="300">
</p>

### Dependencies
<p>On the root of the project, you should create the folder <b>flare</b>, and add the file <b>.flr</b></p>

```dart
dependencies:
  flutter:
    sdk: flutter
flare_flutter: ^1.7.3

assets:
 - flare/Teddy.flr
```

```dart
class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Material(
      child: Center(
        child: FlareActor("flare/Teddy.flr",
            alignment: Alignment.center,
            fit: BoxFit.contain,
            animation: "idle"),
      ),
    );
  }
}
```
