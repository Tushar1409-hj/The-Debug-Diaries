---
title: "🔀 Routing and Navigation in Angular 20"
datePublished: Tue Jul 22 2025 16:57:24 GMT+0000 (Coordinated Universal Time)
cuid: cmdes2bj4000102jpdqheazqf
slug: routing-and-navigation-in-angular-20
tags: javascript, angularjs, web-development, typescript, hashnode, frontend-development, techblogs, angular20, thedebugdiaries, codewithtushar

---

In Angular, **Routing** allows you to navigate between different views or pages of your app — without reloading the whole page. This is what makes Angular apps feel fast and seamless.

---

### 📁 1. What is Routing?

Routing in Angular helps manage different **URL paths** in your application and load specific components based on the route.

For example:

```bash
/home → loads HomeComponent  
/about → loads AboutComponent  
/contact → loads ContactComponent
```

---

### 🧰 2. How to Set Up Routing in Angular 20

When creating a new Angular app, use this command **with routing enabled**:

```bash
bashCopyEditng new my-app --routing
```

> ✅ This will automatically create a `src/app/app-routing.module.ts` file.

---

### 🔌 3. Configuring Routes

Let’s say you have 3 components:

* `home.ts`
    
* `about.ts`
    
* `contact.ts`
    

Update your `app-routing.module.ts` like this:

```typescript
import { NgModule } from '@angular/core';
import { RouterModule, Routes } from '@angular/router';
import { Home } from './home';
import { About } from './about';
import { Contact } from './contact';

const routes: Routes = [
  { path: '', component: Home },
  { path: 'about', component: About },
  { path: 'contact', component: Contact }
];

@NgModule({
  imports: [RouterModule.forRoot(routes)],
  exports: [RouterModule]
})
export class AppRoutingModule {}
```

---

### 🧩 4. Use `<router-outlet>`

In your `app.html`, place this tag where routed components should appear:

```xml
<router-outlet></router-outlet>
```

This is a placeholder for dynamically loading views based on the current route.

---

### 🧭 5. Add Navigation Links

In your navbar or wherever you want routing links:

```xml
<nav>
  <a routerLink="">Home</a>
  <a routerLink="about">About</a>
  <a routerLink="contact">Contact</a>
</nav>
```

To highlight active links, use:

```xml
<a routerLink="about" routerLinkActive="active">About</a>
```

---

### 💡 6. Wildcard Route & Redirects

To handle unknown paths or redirects:

```typescript
const routes: Routes = [
  { path: '', redirectTo: '/home', pathMatch: 'full' },
  { path: '**', component: PageNotFound } // catch-all
];
```

---

### ✅ Summary

| Feature | Purpose |
| --- | --- |
| `RouterModule` | Enables routing in Angular |
| `Routes` array | Defines path → component mappings |
| `<router-outlet>` | Displays routed components |
| `routerLink` | Used for navigation links |
| `routerLinkActive` | Adds active CSS class on route match |

---

### 📌 What’s Next?

In the next blog on The Debug Diaries, we’ll cover:

🧱 **Understanding Angular Directives**  
You’ll learn about structural directives like `*ngIf`, `*ngFor`, and attribute directives to style or change behavior of elements.

Stay tuned and keep debugging with me!

---

### 🔗 Let's Connect and Explore More!

📖 **Read the full series**: [ngtushar.hashnode.dev/angular-series](https://ngtushar.hashnode.dev/angular-series)  
💻 **Source Code on GitHub**: [github.com/Tushar1409-hj](https://github.com/Tushar1409-hj)  
🔗 **Connect with me on LinkedIn**: [linkedin.com/in/tushar1409](https://www.linkedin.com/in/tushar-jadhav-0997ab265/)

If you found this post helpful, don’t forget to share it with your fellow developers and follow the series for more Angular insights! 🚀