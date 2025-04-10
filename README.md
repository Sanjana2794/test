git config --global user.name "sanjana2709"         
git config --global user.email "sanjanamalhotra27000@gmail.com"
git init
git checkout -b main
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/Sanjana2794/test.git
git push -u origin main



name: Code Checkout Only

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  checkout-code:
    runs-on: ubuntu-latest

    steps:
      - name: ⬇ Checkout Repository Code
        uses: actions/checkout@v3

      - name: Print directory structure
        run: ls -R
