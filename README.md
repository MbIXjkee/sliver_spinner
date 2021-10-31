# Sliver-spinner

<img src="https://i.ibb.co/6m0d6wG/sliver-spinner.gif" width="200" alt="Sliver-spinner-demo">

## Description

Simple sliver that spin when moving out from leading edge of viewport.

## How to use

For using you have to place this widget in scrollable area. It may look like:

```dart
class DemoScreen extends StatelessWidget {
  static const urls = <String>[
    'https://www.stockvault.net/data/2018/12/30/258501/preview16.jpg',
    'https://www.stockvault.net/data/2010/10/01/115175/preview16.jpg',
    'https://www.stockvault.net/data/2011/04/18/122242/preview16.jpg',
    'https://www.stockvault.net/data/2014/03/26/155336/preview16.jpg',
    'https://www.stockvault.net/data/2018/12/30/258501/preview16.jpg',
    'https://www.stockvault.net/data/2010/10/01/115175/preview16.jpg',
    'https://www.stockvault.net/data/2011/04/18/122242/preview16.jpg',
    'https://www.stockvault.net/data/2014/03/26/155336/preview16.jpg',
    'https://www.stockvault.net/data/2018/12/30/258501/preview16.jpg',
    'https://www.stockvault.net/data/2010/10/01/115175/preview16.jpg',
    'https://www.stockvault.net/data/2011/04/18/122242/preview16.jpg',
    'https://www.stockvault.net/data/2014/03/26/155336/preview16.jpg',
  ];

  const DemoScreen({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: CustomScrollView(
        slivers: urls
            .map(
              (url) =>
              Spinner(
                child: ClipRRect(
                  borderRadius: BorderRadius.circular(20),
                  child: Image.network(
                    url,
                    fit: BoxFit.cover,
                    height: 300,
                  ),
                ),
              ),
            )
            .toList(),
      ),
    );
  }
}
```

## Maintainer

[Mikhail Zotyev](https://github.com/MbIXjkee)
