import 'package:flutter/material.dart';

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Messaging App'),
      ),
      body: ListView.builder(
        itemCount: 10, // Example: Replace with actual data
        itemBuilder: (context, index) {
          return ListTile(
            leading: CircleAvatar(
              child: Text('A'), // Example: Display user initials or image
            ),
            title: Text('User $index'), // Example: Display user name
            subtitle: Text('Last message'), // Example: Display last message
            onTap: () {
              // Navigate to chat page
              Navigator.push(
                context,
                MaterialPageRoute(builder: (context) => ChatPage()),
              );
            },
          );
        },
      ),
    );
  }
}

class ChatPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('AATHI'), // Example: Display user's name
      ),
      body: Column(
        children: <Widget>[
          Expanded(
            child: ListView.builder(
              reverse: true, // Messages start from bottom
              itemCount: 5, // Example: Replace with actual message count
              itemBuilder: (context, index) {
                return Align(
                  alignment: index % 2 == 0 ? Alignment.centerLeft : Alignment.centerRight,
                  child: ListTile(
                    title: Text('hi $index'), // Example: Display message
                  ),
                );
              },
            ),
          ),
          Container(
            padding: EdgeInsets.all(7.0),
            child: Row(
              children: <Widget>[
                Expanded(
                  child: TextField(
                    decoration: InputDecoration(
                      hintText: 'Type your message...',
                    ),
                  ),
                ),
                IconButton(
                  icon: Icon(Icons.send),
                  onPressed: () {
                    // Send message functionality
                  },
                ),
              ],
            ),
          ),
        ],
      ),
    );
  }
}

void main() {
  runApp(MaterialApp(
    home: HomePage(),
  ));
}
