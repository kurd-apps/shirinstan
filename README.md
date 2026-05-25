# 🏪 Shirinstan - Cashier POS System

A modern, feature-rich Point-of-Sale system built with vanilla JavaScript and Supabase.

## 🚀 Quick Start

### Prerequisites
- Node.js 16+ 
- Supabase account (https://supabase.io)

### Installation

```bash
# Clone the repository
git clone https://github.com/kurd-apps/shirinstan.git
cd shirinstan

# Install dependencies
npm install
```

### Configuration

1. **Create `.env` file** (copy from `.env.example`):
```bash
cp .env.example .env
```

2. **Update `.env` with your Supabase credentials**:
```env
VITE_SUPABASE_URL=https://your-project.supabase.co
VITE_SUPABASE_ANON_KEY=your_anon_key_here
```

3. **Start the server**:
```bash
npm start
# Server runs at http://localhost:3000
```

## 🔐 How .env Connects with HTML

The app now automatically loads Supabase credentials from `.env`:

1. **Backend** (`server.js`): 
   - Reads `.env` file using `dotenv` package
   - Exposes `/api/config` endpoint with Supabase credentials

2. **Frontend** (`shirinstan.html`):
   - On page load, fetches `/api/config`
   - Automatically connects to Supabase if credentials are available
   - Falls back to manual setup form if not configured

### Security Notes
✅ `.env` file is **never** exposed to the browser  
✅ Credentials are stored securely in `localStorage` after connection  
✅ `.env` is in `.gitignore` - never committed to Git  

## 📋 Features

- 🛒 **POS System** - Fast checkout with product search
- 📊 **Dashboard** - Real-time sales analytics
- 📦 **Inventory** - Product and stock management
- 💰 **Accounting** - Expense tracking and P&L analysis
- 👥 **Customers** - Customer database and loyalty tracking
- 📈 **Reports** - Monthly sales and profit analysis
- 🔄 **Demo Mode** - Try without Supabase connection

## 🛠 Tech Stack

- **Frontend**: Vanilla JavaScript, Tailwind CSS
- **Backend**: Node.js, Express
- **Database**: Supabase (PostgreSQL)
- **Styling**: Tailwind CSS, Font Awesome

## 📝 License

MIT License - see LICENSE file for details

## 🤝 Contributing

Contributions welcome! Please feel free to submit a Pull Request.

## 📞 Support

For issues or questions, please open an issue on GitHub.
