# LayoutBuilder
<p align="center">
<img src="https://docs.google.com/uc?id=1DQ3Kg7U6f1grH56ZllUPmjpzSP7bBN-v" height="649" width="300">
</p>

### Main
```dart
class _MyHomePageState extends State<MyHomePage> {
  final items =
      List<String>.generate(20, (items) => "Reorderable Listview $items");
  final _scrollController = ScrollController();

  @override
  Widget build(BuildContext context) {
    return Material(
      child: LayoutBuilder(
        builder: (context, boxConstraints) {
          return Material(
            child: GridView.builder(
              controller: _scrollController,
              itemCount: items.length,
              gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(
                crossAxisCount: boxConstraints.maxWidth < 600 ? 2 : 3,
              ),
              itemBuilder: (context, index) {
                return Card(
                  color: Colors.blue,
                  child: Container(
                    alignment: Alignment.center,
                    child: Text(
                      items[index],
                      style: TextStyle(color: Colors.white),
                    ),
                  ),
                );
              },
            ),
          );
        },
      ),
    );
  }
}
```
