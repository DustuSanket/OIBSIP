# Chat Application

## Description
The Chat Application is a real-time messaging platform built with Python, designed to facilitate seamless communication between users. This project demonstrates proficiency in Python programming, real-time communication, and web development.

## Features
- **Real-time Messaging**: Instant chat between users.
- **User Authentication**: Secure login and registration system.
- **Private and Group Chats**: Options for both one-on-one and group conversations.
- **Emoji Support**: Enrich chats with emojis.
- **Message Notifications**: Get notified of new messages.
- **User Presence**: Shows online/offline status of users.

## Technologies Used
- **Frontend**: HTML, CSS, JavaScript (for client-side interface)
- **Backend**: Python (Flask/Django)
- **Database**: SQLite/PostgreSQL
- **WebSocket**: For real-time communication
- **Authentication**: JWT for secure authentication

## Installation
### Prerequisites
- [Python](https://www.python.org/) installed on your machine
- [Virtualenv](https://pypi.org/project/virtualenv/) for creating a virtual environment

### Steps
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/chat-application.git
    ```
2. Navigate to the project directory:
    ```sh
    cd chat-application
    ```
3. Create and activate a virtual environment:
    ```sh
    virtualenv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```
4. Install the necessary dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage
1. Start the backend server:
    ```sh
    python app.py  # or `python manage.py runserver` if using Django
    ```
2. Open your browser and go to `http://localhost:5000` (or `http://localhost:8000` for Django) to access the chat application.

## Example Code Snippet
Here is an example of setting up a WebSocket connection in Flask using Flask-SocketIO:

```python
from flask import Flask, render_template
from flask_socketio import SocketIO, send

app = Flask(__name__)
app.config['SECRET_KEY'] = 'secret!'
socketio = SocketIO(app)

@socketio.on('message')
def handleMessage(msg):
    print('Message: ' + msg)
    send(msg, broadcast=True)

if __name__ == '__main__':
    socketio.run(app)
