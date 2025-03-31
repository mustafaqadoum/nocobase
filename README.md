2. Switch to the project directory
cd my-nocobase
3. Install dependencies
yarn install --frozen-lockfile
4. Set environment variables
The environment variables required by NocoBase are stored in the root .env file, modify the environment variables according to the actual situation, if you don't know how to change them, click here for environment variables description, or you can leave it as default.

TZ=UTC
APP_KEY=your-secret-key
DB_HOST=localhost
DB_PORT=5432
DB_DATABASE=postgres
DB_USER=nocobase
DB_PASSWORD=nocobase
NOCOBASE_PKG_USERNAME=your-username
NOCOBASE_PKG_PASSWORD=your-password
WARNING
Version 1.4 and above: By setting the environment variables NOCOBASE_PKG_USERNAME and NOCOBASE_PKG_PASSWORD, you can automatically download commercial plugins during application installation or upgrade;
TZ is used to set the application's time zone, with the default being the system's time zone;
APP_KEY is the application's secret key, used for generating user tokens and so on (if APP_KEY is changed, the old tokens will also become invalid). It can be any random string. Please change it to your own secret key and ensure it is not disclosed to the public.
DB_* is related to the database. If it is not the default database service in the example, please modify it according to the actual situation.
5. Install NocoBase
yarn nocobase install --lang=en-US
6. Start NocoBase
Development

yarn dev
Production

# Build (make sure you have executed `yarn install --frozen-lockfile`, note that it does not include `--production`)
yarn build
# Start
yarn start
7. Log in to NocoBase
Open http://localhost:13000 in a web browser. The initial account and password are admin@nocobase.com and admin123.

