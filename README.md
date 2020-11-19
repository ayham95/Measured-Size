# measured_size

A flutter widget that calculates the size of it's child in runtime.

## Getting Started
[MeasuredSize](lib/measured_size.dart) Calculated the size of it's child
in runtime. All you have to do is to wrap your widget with
[MeasuredSize](lib/measured_size.dart) and listen to size changes.


![](example.gif)

### Usage

Complete [example](example)

```dart
MeasuredSize(
              onChange: (Size size) {
                setState(() {
                  print(size);
                });
              },
              child: Text(
                '$_counter',
                style: Theme.of(context).textTheme.headline4,
              ),
            );
```

`onChange` will be called when the [Size] changes.

`onChange` will return the value **ONLY** once if it didn't change, and
it will **NOT** return a value if it's equals to `Size.zero`
