---
title: "📝 How to Install Angular 20 and Set Up Your First App (Step-by-Step Guide)"
datePublished: Wed Jul 16 2025 16:34:19 GMT+0000 (Coordinated Universal Time)
cuid: cmd66liqj000l02jo950u8nwk
slug: how-to-install-angular-20-and-set-up-your-first-app-step-by-step-guide
tags: tutorial, angularjs, web-development, frontend-development, angular20

---

### 👋 Introduction

Welcome back to **The Debug Diaries!**  
In my last post, I talked about *what Angular is and why you should learn it in 2025.*

Now, let’s get hands-on and set up your first Angular project — using the **latest version: Angular 20** 💥

---

### 🧰 What You Need Before Starting

| **Tool** | **Purpose** |
| --- | --- |
| ✅ Node.js | Required for Angular development |
| ✅ npm | Comes with Node.js |
| ✅ Angular CLI 20 | Helps you generate Angular projects |
| ✅ VS Code | A great editor for Angular work |

---

### 🛠️ Step 1: Install Node.js (if not installed)

1. Go to 👉 [https://nodejs.org](https://nodejs.org)
    
2. Download the **LTS version** (recommended)
    

After installing, verify in terminal:

```bash
node -v
npm -v
```

---

### 🚀 Step 2: Install Angular CLI (Latest — v20)

To install Angular CLI globally:

```bash
npm install -g @angular/cli@20
```

> ⚠️ Adding `@20` ensures you’re installing the **latest major version**, not an older one.

Check the version:

```bash
ng version
```

It should show something like:

```bash
Angular CLI: 20.x.x
Node: 18.x.x
```

---

### 📁 Step 3: Create a New Angular App

Run:

```bash
ng new my-angular20-app
```

CLI prompts:

* **Would you like to add Angular routing?** → Type `y`
    
* **Which stylesheet format?** → Choose `CSS` (for now)
    

This will scaffold a fresh Angular 20 app with everything set up.

---

### 👨‍💻 Step 4: Run Your Angular App

Navigate into the project folder:

```bash
cd my-angular20-app
```

Then run the app:

```bash
ng serve
```

Now go to 👉 [`http://localhost:4200`  
You’ll](http://localhost:4200%EF%BF%BCYou%E2%80%99ll) see the default Angular 20 welcome screen.

---

### 🧠 What Just Happened?

* The CLI created your Angular 20 project
    
* It installed all dependencies
    
* A local development server was started
    
* The root component rendered in your browser
    

---

### ✅ Summary

You just:

* Installed Angular CLI 20
    
* Created your first Angular 20 app
    
* Ran it locally in your browser
    

That’s a huge first step toward becoming an Angular developer! 💪

---

### 📌 What’s Next?

In the next post, we’ll dive into:

> 🧱 **Understanding Angular Components — The Building Blocks of Angular Apps**

We’ll break down the files created and explore what each piece does.

Stay tuned on **The Debug Diaries!**

---

### 🔗 Let's Connect and Explore More!

📖 **Read the full series**: [ngtushar.hashnode.dev/angular-series](https://ngtushar.hashnode.dev/angular-series)  
💻 **Source Code on GitHub**: [github.com/Tushar1409-hj](https://github.com/Tushar1409-hj)  
🔗 **Connect with me on LinkedIn**: [linkedin.com/in/tushar1409](https://linkedin.com/in/tushar1409)

If you found this post helpful, don’t forget to share it with your fellow developers and follow the series for more Angular insights! 🚀