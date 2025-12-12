# 🚗 Nairobi Smart Traffic Monitoring System

A React-based web application for visualizing simulated real-time traffic conditions across Nairobi. This project demonstrates interactive data visualization and IoT data analysis using modern web technologies and the Elastic Stack.

## ✨ Features

- **🗺️ Interactive Traffic Maps** - Real-time visualization of traffic conditions across Nairobi's major routes
- **📊 Data Visualization** - Charts and heatmaps showing congestion levels, vehicle counts, and average speeds
- **📈 Real-Time Analytics** - Live monitoring of IoT sensor data simulating vehicle movement
- **🔍 Congestion Detection** - Automatic identification and highlighting of congested areas
- **📱 Responsive Design** - Works seamlessly on desktop and mobile devices
- **🔄 Elasticsearch Integration** - Backend data ingestion and analysis using ELK Stack
- **📊 Kibana Dashboards** - Advanced analytics and historical trend analysis

## 🏗️ Architecture

### Frontend
- **React 19** - Modern UI framework with hooks and concurrent features
- **React Google Maps API** - Interactive mapping components for Nairobi's geography
- **Chart.js / Custom Visualizations** - Data visualization for traffic metrics

### Data Pipeline
- **Elasticsearch** - Distributed search and analytics engine for storing and querying traffic data
- **Kibana** - Data exploration and visualization platform for advanced analytics
- **Mock IoT Sensors** - Simulated traffic data generation for development and testing

### Simulated Data
- Vehicle count data per location
- Average vehicle speeds
- Congestion levels (Low, Medium, High, Critical)
- Real-time timestamp data

## 🚀 Getting Started

### Prerequisites
- Node.js 14+ and npm
- Git
- (Optional) Docker for running Elasticsearch & Kibana

### Frontend Setup

1. **Clone the repository**
```bash
git clone https://github.com/MeriamKalekye/traffic-monitoring-web.git
cd traffic-monitoring-web
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment** (if needed)
```bash
echo "REACT_APP_API_URL=http://localhost:5000" > .env.local
```

4. **Start development server**
```bash
npm start
```

The application will open at `http://localhost:3000`

### Elasticsearch & Kibana Setup (Optional)

To use the full ELK Stack for data ingestion and advanced analytics:

```bash
docker-compose up -d
```

This will start:
- **Elasticsearch** on `http://localhost:9200`
- **Kibana** on `http://localhost:5601`

For Kibana configuration:
1. Go to http://localhost:5601
2. Create an index pattern for traffic data
3. Build custom dashboards for visualization

## 📖 Usage Guide

### Running the Application

**Development Mode:**
```bash
npm start
```
Runs the app in development mode with hot reload.

**Production Build:**
```bash
npm run build
```
Creates optimized production build in the `build/` folder.

**Run Tests:**
```bash
npm test
```
Launches the test runner in interactive watch mode.

### Using the Dashboard

1. **View Traffic Map** - The main page displays an interactive map of Nairobi
2. **Check Congestion Levels** - Color-coded areas show traffic intensity:
   - 🟢 Green: Low traffic
   - 🟡 Yellow: Medium congestion
   - 🟠 Orange: High congestion
   - 🔴 Red: Critical congestion
3. **View Analytics** - Charts show traffic trends and peak hours
4. **Hover for Details** - Get specific information about vehicle counts and speeds

### Connecting to Elasticsearch

To push traffic data to Elasticsearch:

1. Configure the backend data ingest pipeline
2. Set up index mappings in Elasticsearch
3. Create Kibana visualizations for historical analysis

## 📊 Data Structure

Traffic data points include:
```json
{
  "timestamp": "2025-12-12T12:00:00Z",
  "location": "Tom Mboya Street",
  "coordinates": {
    "latitude": -1.2850,
    "longitude": 36.8172
  },
  "vehicle_count": 145,
  "average_speed": 15.5,
  "congestion_level": "High"
}
```

## 🛠️ Tech Stack

**Frontend:**
- React 19
- React Router
- React Google Maps API
- Chart.js for data visualization
- CSS3 for styling

**Data & Analytics:**
- Elasticsearch 8.x
- Kibana 8.x
- Mock IoT simulation data

**DevOps:**
- Docker & Docker Compose
- npm for package management
- Git for version control

## 📁 Project Structure

```
traffic-monitoring-web/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── TrafficMap.js
│   │   ├── Dashboard.js
│   │   ├── Analytics.js
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── styles/
├── package.json
├── README.md
└── .env.example
```

## 🔧 Available Scripts

- `npm start` - Run development server
- `npm build` - Create production build
- `npm test` - Run tests
- `npm run eject` - Eject from Create React App (one-way operation)

## 📈 Visualization & Analytics

### Real-Time Monitoring
- Live traffic flow visualization
- Real-time congestion alerts
- Vehicle movement tracking

### Historical Analytics
- Daily/weekly traffic patterns
- Peak hour analysis
- Congestion trend reports
- Speed distribution charts

### Advanced Analytics (Kibana)
- Custom dashboard creation
- Time-series analysis
- Location-based filtering
- Comparative analysis between routes

## 🎯 Use Cases

- **City Planning** - Identify congestion patterns for infrastructure improvements
- **Traffic Management** - Optimize traffic light timing based on real-time data
- **Route Planning** - Suggest alternative routes to avoid congestion
- **Public Transportation** - Adjust bus schedules based on traffic conditions
- **Emergency Response** - Prioritize ambulance/fire truck routes based on traffic

## 🐛 Troubleshooting

### Map not loading
- Check Google Maps API key is configured
- Verify internet connection
- Check browser console for errors

### Elasticsearch connection fails
- Ensure Elasticsearch is running on localhost:9200
- Check Docker containers are up: `docker ps`
- Verify network connectivity

### Data not updating
- Check mock data generator is running
- Verify Elasticsearch connection
- Check browser developer tools for API errors

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

MIT License - See LICENSE file for details

## 🙋 Support & Questions

For issues, questions, or suggestions:
- Open an issue on [GitHub](https://github.com/MeriamKalekye/traffic-monitoring-web/issues)
- Check existing documentation in the repo
- Review Elasticsearch and Kibana docs for analytics questions

---

**Nairobi Smart Traffic Monitoring System**: Making Nairobi's traffic smarter, one data point at a time. 🚗📊✨
