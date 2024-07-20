# Flutter_task3
 Explore Flutter’s widget-based UI design approach.  ·         Design and implement user interfaces with a variety of widgets.  ·         Focus on creating responsive and visually appealing layouts.
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Widget Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Flutter Widget Demo'),
      ),
      body: SingleChildScrollView(
        child: Center(
          child: Padding(
            padding: const EdgeInsets.all(16.0),
            child: Column(
              mainAxisAlignment: MainAxisAlignment.center,
              crossAxisAlignment: CrossAxisAlignment.center,
              children: [
             const Text(
                  'Welcome to Flutter!',
                  style: TextStyle(fontSize: 32, fontWeight: FontWeight.bold),
                ),
              const  SizedBox(height: 20),
                Container(
                  decoration: BoxDecoration(
                    border: Border.all(color: Colors.blueAccent),
                    borderRadius: BorderRadius.circular(10),
                  ),
                  child: Padding(
                    padding: const EdgeInsets.all(8.0),
                    child: Image.network(
                      'https://images.unsplash.com/photo-1518818608552-195ed130cdf4?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
                      height: 150,
                    ),
                  ),
                ),
             const   SizedBox(height: 20),
             const   Text(
                  'Flutter is Google\'s UI toolkit for building beautiful, natively compiled applications for mobile, web, and desktop from a single codebase.',
                  style: TextStyle(fontSize: 18),
                  textAlign: TextAlign.center,
                ),
             const SizedBox(height: 20),
                ElevatedButton(
                  onPressed: () {
                    // Add your onPressed code here!
                  },
                  style: ElevatedButton.styleFrom(
                    backgroundColor: Colors.blue,
                    foregroundColor: Colors.white,
                    padding: const EdgeInsets.symmetric(horizontal: 24, vertical: 12),
                  ),
                  child:const  Text('Get Started'),
                ),
                SizedBox(height: 20),
                Container(
                  color: Colors.blue,
                  height: 100,
                  width: double.maxFinite,
                  child: const Center(
                    child: Text(
                      'Expanded Widget',
                      style: TextStyle(color: Colors.white, fontSize: 18),
                    ),
                  ),
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}
