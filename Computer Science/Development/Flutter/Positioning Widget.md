# Align Widget

Used for aligning a child widget inside a parent, for example we can use it to align flutter logo i.e. child of container to the top right side of the container:

```dart
Center(
  child: Container(
    height: 120.0,
    width: 120.0,
    color: Colors.blue[50],
    child: const Align(
      alignment: Alignment.topRight,
      child: FlutterLogo(
        size: 60,
      ),
    ),
  ),
)
```

![[Pasted image 20230710153752.png]]

