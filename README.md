# Ocean - Maritime Safety Dashboard

A comprehensive maritime safety dashboard that provides real-time monitoring of ocean hazards, social media alerts, coastal information, and vessel advisory services.

## 🌊 Features

- **Real-time Dashboard**: Monitor maritime hazards and safety incidents
- **Social Media Integration**: Track Twitter for maritime safety-related content using Gopher API
- **Coastal Information**: Small Vessel Advisory Service (SVAS) with interactive maps
- **Government Alerts**: Integration with official maritime safety alerts
- **Interactive Maps**: Leaflet-based mapping with multiple layers and data visualization
- **Data Analytics**: Charts and statistics for hazard analysis and trends

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- pip (Python package installer)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd PROJECT
   ```

2. **Set up Python virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**
   ```bash
   cp .env.example .env
   # Edit .env file with your actual API keys and configuration
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Access the application**
   - Open your browser and navigate to: `http://localhost:5002`

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the project root with the following variables:

```env
# Gopher API Configuration
GOPHER_API_URL=https://data.gopher-ai.com/api/v1/search/live/twitter
GOPHER_AUTH_TOKEN=your_gopher_auth_token_here

# Supabase Configuration
SUPABASE_URL=your_supabase_url_here
SUPABASE_ANON_KEY=your_supabase_anon_key_here

# Flask Configuration
FLASK_DEBUG=True
FLASK_HOST=0.0.0.0
FLASK_PORT=5002
```

### Required API Keys

- **Gopher API**: For Twitter/social media data integration
- **Supabase**: For database and real-time features

## 📁 Project Structure

```
PROJECT/
├── app.py                  # Flask backend application
├── samudradashboard.html   # Main dashboard HTML
├── dashboard33.js          # Dashboard functionality
├── social.js              # Social media integration
├── coastalinfo.js          # Coastal information features
├── auth.html              # Authentication page
├── auth.js                # Authentication logic
├── social.html            # Social media monitoring page
├── requirements.txt        # Python dependencies
├── .env                   # Environment variables (not in repo)
├── .env.example           # Environment variables template
├── .gitignore            # Git ignore file
└── README.md             # This file
```

## 🖥️ Application Components

### Backend (Flask)
- **API Endpoints**: 
  - `/api/twitter/search` - Search Twitter for maritime content
  - `/api/twitter/result/<job_uuid>` - Get search results
  - `/api/config` - Client configuration endpoint
- **Environment Management**: Secure handling of API keys
- **CORS Support**: Cross-origin resource sharing for frontend

### Frontend (JavaScript)
- **Dashboard**: Real-time monitoring interface
- **Maps**: Interactive Leaflet maps with multiple layers
- **Charts**: Data visualization using Chart.js
- **Social Media**: Twitter integration and sentiment analysis
- **Authentication**: User authentication system

## 🔒 Security Features

- **Environment Variables**: API keys stored securely in `.env` file
- **No Hardcoded Secrets**: All sensitive data externalized
- **Git Ignore**: `.env` file excluded from version control
- **Server-side Config**: Client receives configuration through secure API

## 🛠️ Development

### Running in Development Mode

```bash
# Activate virtual environment
source venv/bin/activate

# Run with debug mode (set in .env)
python app.py
```

### Dependencies

- **Flask 2.3.3**: Web framework
- **Flask-CORS 4.0.1**: CORS support
- **Requests 2.31.0**: HTTP client library
- **python-dotenv 1.0.0**: Environment variable management

## 🌐 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/` | GET | Serve main dashboard |
| `/api/config` | GET | Get client configuration |
| `/api/twitter/search` | POST | Initiate Twitter search |
| `/api/twitter/result/<uuid>` | GET | Get search results |
| `/<filename>` | GET | Serve static files |

## 📊 Features in Detail

### Maritime Safety Dashboard
- Real-time hazard monitoring
- Interactive maps with multiple data layers
- Government alerts integration
- Incident reporting and tracking

### Social Media Monitoring
- Twitter search and analysis
- Sentiment analysis of maritime content
- Trending keywords and hashtags
- Real-time social media alerts

### Coastal Information
- Small Vessel Advisory Service (SVAS)
- Weather and sea condition data
- Interactive coastal maps
- Navigation warnings

## 🚨 Troubleshooting

### Common Issues

1. **Module not found errors**
   - Ensure virtual environment is activated
   - Run `pip install -r requirements.txt`

2. **API key errors**
   - Check `.env` file exists and has correct values
   - Verify API keys are valid and active

3. **Port conflicts**
   - Change `FLASK_PORT` in `.env` file
   - Ensure no other services are using the port

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📝 License

[Add your license information here]

## 🆘 Support

For issues and questions:
- Create an issue in the repository
- Check the troubleshooting section
- Review the configuration guide

---

**Note**: This application is designed for maritime safety monitoring. Ensure proper API keys and permissions are configured before deployment.
