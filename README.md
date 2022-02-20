# giphy_api_client

A Giphy API Client for Dart compatible with all platforms

Forked from https://pub.dev/packages/giphy_client
Credit to author(s) of original repo
Forked and added null safety due to inactivity on attempts to merge on repo

## Usage

First, register an app at the [Giphy Developers Portal](https://developers.giphy.com).

Then, follow the instructions below:

```dart
import 'package:giphy_api_client/giphy_client.dart';

main() async {
  // Create the client with an api key
  //
  // Visit https://developers.giphy.com to obtain a key
  final client = new GiphyClient(apiKey: 'your_api_key_here');

  // Fetch & print a collection of trending gifs
  final gifs = await client.trending();

  print(gifs);

  // Fetch & print a collection with options
  final nsfwGifs = await client.trending(
    offset: 1,
    limit: 10,
    rating: GiphyRating.r,
  );

  print(nsfwGifs);
}
```

## Features and bugs

Please file feature requests and bugs at the [issue tracker][tracker].

[tracker]: https://github.com/java-james/giphy_client/issues/new
