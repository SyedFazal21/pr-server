# MongoDB Database Setup Guide

This guide helps you set up a MongoDB Atlas database, create a cluster, generate a connection string, and store it securely in a `.env` file. We will create a database named **PR-Solutions**.

---

## ✅ Step 1: Register on MongoDB Atlas

1. Go to: https://www.mongodb.com/cloud/atlas/register  
2. Sign up using your email, Google, or GitHub account  
3. Verify your email if required

---

## ✅ Step 2: Create a Free Cluster

1. Click **"Build a Database"**
2. Choose **Shared Cluster (Free Tier)**
3. Select a cloud provider (AWS recommended) and a region close to you (e.g., Mumbai)
4. Click **Create Cluster**

_Note: Cluster provisioning takes 1–3 minutes._

---

## ✅ Step 3: Create a Database User

1. Click **Database > Connect > Username & Password**
2. Create a username and password  
   ⚠️ Save them for your connection string
3. Click **Create Database User**

---

## ✅ Step 4: Add IP Address to Access List

1. In the Connect screen, click **Add IP Address**
2. Choose one of:
   - **Add Current IP Address**
   - **Allow Access from Anywhere (0.0.0.0/0)** (for development)
3. Click **Confirm**

---

## ✅ Step 5: Get Your MongoDB Connection String

1. Click **Connect > Connect your application**
2. Choose:
   - Driver: **Node.js**
   - Version: **Latest**
3. Copy the connection string. It looks like this:

mongodb+srv://<username>:<password>@cluster0.mongodb.net/PR-Solutions?retryWrites=true&w=majority

📌 Replace <username> and <password> with your Atlas credentials.

## ✅ Step 6: Add URI to .env File
1. Create a .env file in your project
2. Add your connection string like below
3. MONGODB_URI=mongodb+srv://yourUser:yourPassword@cluster0.mongodb.net/PR-Solutions?retryWrites=true&w=majority

