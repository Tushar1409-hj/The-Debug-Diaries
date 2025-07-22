---
title: "🧩 Two-Way Data Binding and Angular Forms in Angular 20"
datePublished: Tue Jul 22 2025 15:25:47 GMT+0000 (Coordinated Universal Time)
cuid: cmdeosifk001102l0fcjy1usm
slug: two-way-data-binding-and-angular-forms-in-angular-20
tags: javascript, angularjs, web-development, typescript, hashnode, frontend-development, techblogs, angular20, thedebugdiaries, codewithtushar

---

*Sync your UI with your data — instantly!*

In this blog, we’ll explore how to **bind user input** to your component class and keep it updated in real-time using **two-way data binding**. We’ll also learn the basics of **Angular Forms**.

---

## 🔁 What is Two-Way Data Binding?

Two-way binding allows **synchronization between the input field in the UI** and the **component's variable**.

This means:

* When the user updates the input, the component gets updated.
    
* When the component value changes, the UI reflects it immediately.
    

To do this in Angular, we use the `[(ngModel)]` syntax — also called **banana in a box** 🐵📦.

---

## 🛠️ Setting Up `ngModel`

Before using `[(ngModel)]`, you must import the `FormsModule`.

### Step 1: Import FormsModule

```typescript
// app.config.ts (Angular 20+)
import { provideForms } from '@angular/forms';

export const appConfig = {
  providers: [provideForms()]
};
```

✅ This setup is specific to Angular 20 and **standalone components**.  
You no longer need to import FormsModule from `@angular/forms` in NgModules.

---

## 📝 Simple Two-Way Binding Example

Let’s create a simple input field where users can enter their name and see it update live.

### ✅ Component: `app.ts`

```typescript
export class App {
  username = '';
}
```

### ✅ Template: `app.html`

```xml
<input [(ngModel)]="username" placeholder="Enter your name" />
<p>Hello, {{ username }}!</p>
```

### 🔄 Output:

As you type, the `username` value updates in real time — both in the input box and in the greeting message.

---

## 🧪 Form Controls with ngModel

You can use `[(ngModel)]` for multiple fields:

```typescript
export class App {
  email = '';
  password = '';
}
```

```xml
<form>
  <input type="email" [(ngModel)]="email" name="email" placeholder="Email" />
  <input type="password" [(ngModel)]="password" name="password" placeholder="Password" />
  <button (click)="submitForm()">Submit</button>
</form>
```

> 💡 Don't forget the `name` attribute — it’s required for `ngModel` in forms!

---

## ✅ Simple Form Submission

```typescript
export class App {
  email = '';
  password = '';

  submitForm() {
    console.log('Email:', this.email);
    console.log('Password:', this.password);
  }
}
```

When you click the button, the current values of the form fields will be logged to the console.

---

## 🧾 Summary

| Concept | Description |
| --- | --- |
| `[(ngModel)]` | Two-way binding between UI and class |
| `FormsModule` | Required to use `ngModel` in Angular |
| `name` attribute | Required in form elements using `ngModel` |

---

## 📌 What’s Next?

In the next blog on **The Debug Diaries**, we’ll explore:

⚙️ **Understanding Angular Directives**  
You’ll learn how to use structural (`*ngIf`, `*ngFor`) and attribute directives to control how your app looks and behaves.

---

### 🔗 Let's Connect and Explore More!

📖 **Read the full series**: [ngtushar.hashnode.dev/angular-series](https://ngtushar.hashnode.dev/angular-series)  
💻 **Source Code on GitHub**: [github.com/Tushar1409-hj](https://github.com/Tushar1409-hj)  
🔗 **Connect with me on LinkedIn**: [linkedin.com/in/tushar1409](https://www.linkedin.com/in/tushar-jadhav-0997ab265/)

If you found this post helpful, don’t forget to share it with your fellow developers and follow the series for more Angular insights! 🚀