```sh
# Create a new Vite project with React template
yarn create vite mini-e-commerce --template react
cd mini-e-commerce

# Initialize a new Git repository
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/mugabiBenjamin/mini-e-commerce.git

# Install Tailwind CSS and its Vite plugin
npm install tailwindcss @tailwindcss/vite

# Import Tailwind CSS in your project
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

// https://vite.dev/config/
export default defineConfig({
  plugins: [react(), tailwindcss()],
  server: {
    port: 5000
  }
})

# Install firebase
yarn add firebase

# Install all dependecies (optional)
yarn install

yarn lint       # For code linting
yarn format     # For code formatting


# Start the development server
yarn dev

git add.
git commit -m ""
git push -u origin main
```
