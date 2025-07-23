---
title: "🧱 Understanding Angular Directives in Angular 20"
datePublished: Wed Jul 23 2025 10:37:27 GMT+0000 (Coordinated Universal Time)
cuid: cmdftxjwm000402l19cgs5jl4
slug: understanding-angular-directives-in-angular-20
tags: javascript, angularjs, web-development, typescript, hashnode, frontend-development, techblogs, angular20, thedebugdiaries, codewithtushar

---

Welcome back to **The Debug Diaries**! In this post, we’ll explore one of Angular’s most powerful features — **Directives**. If you want to build dynamic and responsive apps, you’ll use directives *everywhere*.

---

## 🚀 What Are Directives?

Directives in Angular are **instructions** in the DOM (Document Object Model). They let you modify the structure or behavior of elements dynamically.

There are mainly **two types** you’ll use most often:

1. **Structural Directives**: Change the layout by adding or removing elements (e.g. `*ngIf`, `*ngFor`)
    
2. **Attribute Directives**: Change the appearance or behavior of an element (e.g. `ngClass`, `ngStyle`)
    

---

## 1️⃣ Structural Directives

### ✅ `*ngIf`: Conditionally Display Elements

```xml
<p *ngIf="isLoggedIn">Welcome back, Tushar!</p>
```

**How it works:**  
If `isLoggedIn` is `true`, Angular renders the `<p>`. If false, it removes it from the DOM.

---

### 🔁 `*ngFor`: Loop Through Items

```xml
<ul>
  <li *ngFor="let tech of technologies">{{ tech }}</li>
</ul>
```

**Example Component:**

```typescript
export class AppComponent {
  technologies = ['Angular', 'React', 'Vue'];
}
```

---

## 2️⃣ Attribute Directives

### 🎨 `ngClass`: Apply Classes Dynamically

```xml
<p [ngClass]="{ 'highlight': isImportant }">
  This message might be important.
</p>
```

### 🖌 `ngStyle`: Apply Inline Styles

```xml
<p [ngStyle]="{ 'color': isError ? 'red' : 'green' }">
  Status Message
</p>
```

---

## 👨‍💻 Creating Your Own Directive (Optional for Beginners)

You can create custom directives to encapsulate reusable logic:

```bash
ng generate directive highlight
```

This will generate:

* `highlight.directive.ts`
    
* And automatically register it in `app.module.ts`
    

You can later apply your custom logic to any element.

---

## 🧠 Summary

| Directive | Type | Purpose |
| --- | --- | --- |
| `*ngIf` | Structural | Conditionally shows/hides content |
| `*ngFor` | Structural | Loops over lists |
| `ngClass` | Attribute | Applies/removes CSS classes |
| `ngStyle` | Attribute | Dynamically styles elements |

---

## 📌 **What’s Next?**  
In the next blog on **The Debug Diaries**, we’ll cover:

🧠 **Angular Services and Dependency Injection**  
You’ll learn how to create services, inject them into components, and share logic or data across your Angular app efficiently.

Stay tuned — the magic of Angular services is coming up next!

---

### **🔗 Let's Connect and Explore More!**

📖 **Read the full series**: [**ngtushar.hashnode.dev/angular-series**](https://ngtushar.hashnode.dev/angular-series)  
💻 **Source Code on GitHub**: [**github.com/Tushar1409-hj**](https://github.com/Tushar1409-hj)  
🔗 **Connect with me on LinkedIn**: [**linkedin.com/in/tushar1409**](https://www.linkedin.com/in/tushar-jadhav-0997ab265/)

If you found this post helpful, don’t forget to share it with your fellow developers and follow the series for more Angular insights! 🚀