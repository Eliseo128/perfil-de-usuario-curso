```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MiApp());
}

class MiApp extends StatelessWidget {
  const MiApp({super.key});

  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      debugShowCheckedModeBanner: false,
      home: PerfilScreen(),
    );
  }
}// fin clase MiApp

class PerfilScreen extends StatelessWidget {
  const PerfilScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('Perfil de Usuario Eliseo Cbtis 128'),
        
        backgroundColor: Colors.amber,
      ),
      body: Center(
        child: Container(
          padding: const EdgeInsets.all(16),
          margin: const EdgeInsets.all(20),
          decoration: BoxDecoration(
            color: Colors.cyan,
            borderRadius: BorderRadius.circular(12),
          ),
          child: Row(
            children: [
              const CircleAvatar(
                radius: 40,
                backgroundImage: NetworkImage(
                  'https://www.gstatic.com/flutter-onestack-prototype/genui/example_1.jpg',
                ),
              ),
              const SizedBox(width: 20),
              Expanded(
                child: Column(
                  crossAxisAlignment: CrossAxisAlignment.start,
                  mainAxisSize: MainAxisSize.min,
                  children: const [
                    Text('Eliseo Cbtis 128',
                        style:
                            TextStyle(fontSize: 20, fontWeight: FontWeight.bold)),
                    Text('Desarrollador Flutter del Cbtis 128'),
                    Text('eliseo@email.com'),
                  ],
                ),
              )
            ],
          ),
        ),
      ),
    );
  }
}// fin clase PerfilScreen
```
