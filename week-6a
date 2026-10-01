import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  const HomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const AppTitle(
          title: 'Custom Widgets Demo',
        ),
        backgroundColor: Colors.green,
      ),
      backgroundColor: Colors.lightGreenAccent,
      body: const SingleChildScrollView(
        padding: EdgeInsets.all(16),
        child: Column(
          children: [
            ProfileCard(
              name: 'Alice',
              role: 'Flutter Developer',
              imageUrl: 'https://i.pravatar.cc/150?img=2',
            ),
            SizedBox(height: 20),
            ProfileCard(
              name: 'Bob',
              role: 'Backend Engineer',
              imageUrl: 'https://i.pravatar.cc/150?img=4',
            ),
            SizedBox(height: 30),
            CounterCard(),
          ],
        ),
      ),
    );
  }
}

class AppTitle extends StatelessWidget {
  final String title;

  const AppTitle({
    super.key,
    required this.title,
  });

  @override
  Widget build(BuildContext context) {
    return Text(
      title,
      style: const TextStyle(
        fontSize: 24,
        fontWeight: FontWeight.bold,
      ),
    );
  }
}

class ProfileCard extends StatelessWidget {
  final String name;
  final String role;
  final String imageUrl;

  const ProfileCard({
    super.key,
    required this.name,
    required this.role,
    required this.imageUrl,
  });

  @override
  Widget build(BuildContext context) {
    return Card(
      elevation: 4,
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(12),
      ),
      child: ListTile(
        leading: CircleAvatar(
          radius: 30,
          backgroundImage: NetworkImage(imageUrl),
        ),
        title: Text(
          name,
          style: const TextStyle(
            fontSize: 18,
            fontWeight: FontWeight.bold,
          ),
        ),
        subtitle: Text(role),
      ),
    );
  }
}

class CounterCard extends StatefulWidget {
  const CounterCard({super.key});

  @override
  State<CounterCard> createState() => _CounterCardState();
}

class _CounterCardState extends State<CounterCard> {
  int _count = 0;

  void _increment() {
    if (_count < 10) {
      setState(() {
        _count++;
      });
    }
  }

  void _decrement() {
    if (_count > 0) {
      setState(() {
        _count--;
      });
    }
  }

  @override
  Widget build(BuildContext context) {
    return Card(
      elevation: 3,
      shape: RoundedRectangleBorder(
        borderRadius: BorderRadius.circular(10),
      ),
      child: Padding(
        padding: const EdgeInsets.all(16),
        child: Column(
          children: [
            const Text(
              'Counter Widget',
              style: TextStyle(
                fontSize: 18,
                fontWeight: FontWeight.w600,
              ),
            ),
            const SizedBox(height: 10),
            Text(
              '$_count',
              style: const TextStyle(
                fontSize: 36,
                color: Colors.blue,
              ),
            ),
            const SizedBox(height: 10),
            ElevatedButton(
              onPressed: _increment,
              child: const Text('Increment'),
            ),
            const SizedBox(height: 8),
            ElevatedButton(
              onPressed: _decrement,
              child: const Text('Decrement'),
            ),
          ],
        ),
      ),
    );
  }
}
