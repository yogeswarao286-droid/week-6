import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

// Custom Header Style
const TextStyle customHeaderStyle = TextStyle(
  fontSize: 26,
  fontWeight: FontWeight.bold,
  color: Colors.teal,
);

// Custom Body Style
const TextStyle customBodyStyle = TextStyle(
  fontSize: 16,
  color: Colors.black87,
);

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Theme Demo',
      debugShowCheckedModeBanner: false,

      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(
          seedColor: Colors.teal,
        ),

        scaffoldBackgroundColor: Colors.grey.shade200,

        // Text Theme
        textTheme: const TextTheme(
          titleLarge: TextStyle(
            fontSize: 24,
            fontWeight: FontWeight.bold,
          ),
          bodyMedium: TextStyle(
            fontSize: 16,
          ),
        ),

        // Elevated Button Theme
        elevatedButtonTheme: ElevatedButtonThemeData(
          style: ElevatedButton.styleFrom(
            backgroundColor: Colors.teal,
            foregroundColor: Colors.white,
            padding: const EdgeInsets.symmetric(
              horizontal: 24,
              vertical: 12,
            ),
            textStyle: const TextStyle(
              fontSize: 16,
              fontWeight: FontWeight.w600,
            ),
          ),
        ),

        // Card Theme
        cardTheme: CardThemeData(
          elevation: 5,
          shape: RoundedRectangleBorder(
            borderRadius: BorderRadius.circular(12),
          ),
          margin: const EdgeInsets.all(10),
        ),
      ),

      home: const HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  const HomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    final ThemeData theme = Theme.of(context);

    return Scaffold(
      appBar: AppBar(
        title: const Text('Themed UI'),
        backgroundColor: Colors.teal,
        foregroundColor: Colors.white,
      ),

      body: Padding(
        padding: const EdgeInsets.all(20),

        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            // Custom Header
            const Text(
              'Welcome to Flutter!',
              style: customHeaderStyle,
            ),

            const SizedBox(height: 20),

            // Card
            Card(
              child: Padding(
                padding: const EdgeInsets.all(16),

                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  children: [
                    Text(
                      'User Info',
                      style: theme.textTheme.titleLarge,
                    ),

                    const SizedBox(height: 10),

                    const Text(
                      'Name: John Doe',
                      style: customBodyStyle,
                    ),

                    const SizedBox(height: 5),

                    Text(
                      'Role: Developer',
                      style: theme.textTheme.bodyMedium,
                    ),
                  ],
                ),
              ),
            ),

            const SizedBox(height: 20),

            // Styled Button
            ElevatedButton(
              onPressed: () {
                ScaffoldMessenger.of(context).showSnackBar(
                  const SnackBar(
                    content: Text('Styled Button Clicked'),
                  ),
                );
              },
              child: const Text('Styled Button'),
            ),
          ],
        ),
      ),
    );
  }
}
