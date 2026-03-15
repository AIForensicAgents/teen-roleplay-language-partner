# Clone the repository
git clone https://github.com/your-org/teen-roleplay-language-partner.git
cd teen-roleplay-language-partner

# Install frontend dependencies
cd client
pnpm install

# Install backend dependencies
cd ../server
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt

# Set up the database
cd ../
cp .env.example .env
python server/manage.py migrate
python server/manage.py seed_scenarios