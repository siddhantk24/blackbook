# Clone the repository
git clone https://github.com/yourusername/fake-product-detection.git
cd fake-product-detection

# Install dependencies
npm install
```

2. Database Setup
```bash
# Create a .env file in the project root and add:
DATABASE_URL=postgresql://postgres:your_password@localhost:5432/fake_product_detection

# Initialize the database
npm run db:push
```

3. Start the Application
```bash
# Start the development server
npm run dev
```

4. Access the Application
- Open your browser and navigate to: http://localhost:5000
- If you get a connection error, try these troubleshooting steps:
  - Make sure no other application is using port 5000
  - Check if the server is running (you should see "Server is running" in the terminal)
  - Try accessing through http://127.0.0.1:5000 instead of localhost

## Common Issues

If you see "Unable to connect":
1. Check if the terminal shows the server running message
2. Make sure your firewall isn't blocking the connection
3. Try stopping and restarting the server
4. Check if port 5000 is available using:
```bash
# On Windows
netstat -ano | findstr :5000

# On Mac/Linux
lsof -i :5000