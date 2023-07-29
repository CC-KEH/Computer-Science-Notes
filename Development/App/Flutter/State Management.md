
## State
**State refers to the data that can change within a Flutter application. It includes variables, objects, or any other data that can be updated during runtime.**


## Stateful Widget:

- StatefulWidget is a widget that has mutable(changeable) state.
- It consists of two classes: the StatefulWidget itself and the corresponding State class.
- The StatefulWidget class is immutable and can be rebuilt when the state changes.

``` dart
class MyWidget extends StatefulWidget {
  @override
  _MyWidgetState createState() => _MyWidgetState();
}

class _MyWidgetState extends State<MyWidget> {
  int counter = 0;

  void incrementCounter() {
    setState(() {
      counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Counter: $counter'),
        RaisedButton(
          child: Text('Increment'),
          onPressed: incrementCounter,
        ),
      ],
    );
  }
}
```


## Stateless Widget:

- Immutable
- Single class
**StatelessWidget is a simple and lightweight widget that is mainly used for presenting static content or UI components that don't need to update based on user interaction or data changes. Since it doesn't have mutable state, its build method is called only once during the initial rendering.**

```dart
class MyWidget extends StatelessWidget {
  final String title;

  MyWidget({this.title});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(title),
      ),
      body: Center(
        child: Text('Hello, World!'),
      ),
    );
  }
}
```


## Inherited Widget:

- InheritedWidget allows you to propagate state down the widget tree to its descendants.
- It's useful when you have multiple widgets that need access to the same data.

```dart
class MyData extends InheritedWidget {
  final int counter;

  MyData({this.counter, Widget child}) : super(child: child);

  static MyData of(BuildContext context) {
    return context.dependOnInheritedWidgetOfExactType<MyData>();
  }

  @override
  bool updateShouldNotify(MyData oldWidget) {
    return oldWidget.counter != counter;
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final myData = MyData.of(context);

    return Column(
      children: [
        Text('Counter: ${myData.counter}'),
        RaisedButton(
          child: Text('Increment'),
          onPressed: () {
            // Update the counter using the inherited widget
            MyData.of(context).incrementCounter();
          },
        ),
      ],
    );
  }
}
```


## Local State Management: 
**For simple applications, you can manage state locally within a widget using StatefulWidget. The state is stored in the StatefulWidget and can be modified using the setState() method.**

setState(): The setState() method is used to update the state of a StatefulWidget. It notifies Flutter that the state has changed and triggers a rebuild of the widget



### Provider Package: 
**The Provider package is a popular state management solution in Flutter. It allows you to provide and access data across the widget tree. It uses InheritedWidget internally and simplifies the process of managing state.**

``` dart
import 'package:provider/provider.dart';

class CounterProvider extends ChangeNotifier {
  int _counter = 0;

  int get counter => _counter;

  void incrementCounter() {
    _counter++;
    notifyListeners();
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    final counterProvider = Provider.of<CounterProvider>(context);

    return Column(
      children: [
        Text('Counter: ${counterProvider.counter}'),
        ElevatedButton(
          child: Text('Increment'),
          onPressed: () {
            counterProvider.incrementCounter();
          },
        ),
      ],
    );
  }
}
```


### GetX: 
**GetX is a lightweight, high-performance state management solution for Flutter. It provides a simple API for managing reactive state and dependencies. GetX uses the concept of controllers to manage state and provides reactive widgets for updating the UI.**

```dart
import 'package:get/get.dart';

class CounterController extends GetxController {
  var counter = 0.obs;

  void incrementCounter() {
    counter.value++;
  }
}

class MyWidget extends StatelessWidget {
  final CounterController counterController = Get.put(CounterController());

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Obx(() => Text('Counter: ${counterController.counter.value}')),
        ElevatedButton(
          child: Text('Increment'),
          onPressed: () {
            counterController.incrementCounter();
          },
        ),
      ],
    );
  }
}
```

### Riverpod: 
**Riverpod is a provider package developed by the same team behind Provider. It offers a more modern and simplified API compared to the original Provider package. Riverpod leverages Dart's sound null safety and offers improved performance.**

``` dart
import 'package:flutter_riverpod/flutter_riverpod.dart';

final counterProvider = Provider<int>((ref) => 0);

class MyWidget extends ConsumerWidget {
  @override
  Widget build(BuildContext context, ScopedReader watch) {
    final counter = watch(counterProvider);

    return Column(
      children: [
        Text('Counter: $counter'),
        ElevatedButton(
          child: Text('Increment'),
          onPressed: () {
            context.read(counterProvider).state++;
          },
        ),
      ],
    );
  }
}
```
