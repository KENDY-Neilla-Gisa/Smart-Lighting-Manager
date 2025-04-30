# Smart Lighting Manager 💡

A modern web application for automated light control using MQTT protocol, featuring an intuitive scheduler interface and real-time control capabilities.

## Features ✨

- **Intuitive Web Interface**: Clean, modern design for easy schedule management
- **Real-time Control**: Instant communication through WebSocket technology
- **Reliable Automation**: Precise scheduling with MQTT protocol
- **Hardware Integration**: Direct control of Arduino-based relay systems
- **Mobile Responsive**: Works seamlessly on all devices

## System Architecture 🏗️

### Frontend Application
- Modern UI built with HTML5, CSS3, and JavaScript
- Real-time updates using WebSocket connection
- Responsive design with Bootstrap framework
- Intuitive time picker for schedule management

### Backend Services
- **WebSocket Server**: Handles real-time communication
- **MQTT Integration**: Manages device communication
- **Arduino Controller**: Controls physical relay hardware
- **Scheduling System**: Precise timing control

## Getting Started 🚀

### Prerequisites
- Python 3.x
- Arduino board with relay module
- Modern web browser
- Internet connection for MQTT broker access

### Installation

1. **Clone the repository**
   ```bash
   git clone [your-repository-url]
   cd [repository-name]
   ```

2. **Set up Python environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: .\venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Configure Arduino**
   - Connect relay to pin 7
   - Upload the sketch from `arduino/relay.ino`
   - Note your COM port for configuration

4. **Start the application**
   ```bash
   python websocket_server.py
   ```

5. **Access the interface**
   - Open `http://localhost:8000` in your browser
   - Set your desired schedule
   - Monitor the status in real-time

## Configuration ⚙️

### Default Settings
- MQTT Broker: 157.173.101.159:1883
- WebSocket: ws://localhost:8765
- HTTP Server: http://localhost:8000
- Arduino Relay Pin: 7

### Customization
You can modify these settings in their respective configuration files:
- `websocket_server.py`: MQTT and WebSocket settings
- `arduino/relay.ino`: Pin configurations
- `static/style.css`: UI customization

## Technical Details 🔧

### Communication Flow
1. User sets schedule through web interface
2. WebSocket server receives and processes schedule
3. MQTT messages trigger relay state changes
4. Arduino executes physical light control

### Security Considerations
- MQTT broker requires no authentication (development setup)
- WebSocket communication is unencrypted
- Recommended to implement SSL/TLS in production

## Troubleshooting 🔍

Common issues and solutions:
1. **Connection Failed**
   - Verify MQTT broker accessibility
   - Check network connectivity
   - Ensure correct port configurations

2. **Relay Not Responding**
   - Verify Arduino connection
   - Check relay wiring
   - Confirm correct COM port settings

3. **Schedule Not Working**
   - Verify server time synchronization
   - Check WebSocket connection status
   - Monitor MQTT message flow

## Contributing 🤝

Contributions are welcome! Please feel free to submit pull requests.

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License 📄

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments 🙏

- Built with modern web technologies
- Inspired by home automation needs
- Community-driven improvements welcome
"# Smart-Lighting-Manager" 
