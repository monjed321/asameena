# Asameena

**Published iOS app · iPhone & iPad**

### [View Asameena on the App Store →](https://apps.apple.com/sa/app/asameena/id6752386204)

Explore the published app's screenshots, description, and release history on Apple's official listing. The app serves partner jewelry stores; its business features require a partner-store account.

**Asameena** is a B2B jewelry order and workshop management application built to digitize the relationship between a small gold/jewelry manufacturer and the jewelry stores that work with it.

The project was developed from a real business need. The manufacturer receives work from multiple jewelry stores, and each store needs a reliable way to send repair, engraving, custom name/photo, and other production requests together with all required images and specifications. Traditionally, this communication can become fragmented across phone calls, messaging applications, handwritten notes, and manual account records.

Asameena centralizes this entire B2B workflow into one application. Partner jewelry stores use the application to communicate directly with the manufacturer, submit and follow their work orders, browse models, and review their business account information. The manufacturer uses the administrative side of Asameena to receive, organize, update, and account for work coming from all partner stores.

The project began as a web application and was later converted into a mobile application using **Capacitor**.

**Asameena has been published on the Apple App Store under the name “Asameena”.**

---

## 🎯 Project Purpose

A small jewelry manufacturer working with multiple jewelry stores receives many specialized production and service requests every day.

Unlike a standard retail purchase, each B2B work order may include:

- Customer information
- Jewelry images
- Reference/design images
- Weight
- Karat
- Engraving text
- Custom names or photos
- Pricing
- Order status
- Additional notes

Managing this information through calls, chat messages, photos, and handwritten records becomes difficult when the manufacturer is simultaneously serving multiple jewelry stores.

**Asameena gives the manufacturer and its partner jewelry stores one dedicated B2B communication and order-management channel.**

---

## 👥 Who Is It For?

The application is designed around two sides of the same B2B relationship.

### Manufacturer / Workshop Administrator

The owner of the gold manufacturing workshop uses the administration interface to receive work from partner jewelry stores, manage their orders, update order details and statuses, enter weights and prices, and maintain the business account of each store.

### Partner Jewelry Stores

The users of the client-facing application are **jewelry stores that work with the manufacturer — not retail consumers**.

Each partner store receives its own account and can use Asameena to submit work directly to the workshop, attach images and specifications, browse available models, follow submitted orders, receive updates, and review its account information.

---

## ✨ Main Features

### 🔐 Authentication

Asameena includes a user authentication system built around **Firebase Authentication**.

The application distinguishes between administrative access and customer accounts so that each user sees the appropriate interface and functionality.

---

### 📦 Order Management

Partner jewelry stores can create and submit work orders directly to the manufacturer through the application.

Different order workflows were created for services such as:

- Repair
- Engraving
- Names / Photos

Depending on the order type, the system can store information such as:

- Images
- Weight
- Karat
- Notes
- Engraving information
- Print/reference images
- Price
- Order date
- Order status

The manufacturer receives and manages these requests from the administration interface.

---

## 🖼️ Image Uploads

Images are an important part of the jewelry ordering process.

Asameena allows partner jewelry stores to upload images associated with their work orders, including jewelry photos and reference/printing images for custom work.

This reduces the need for stores to send production details and images separately through messaging applications and ensures that every image remains associated with the correct work order received by the manufacturer.

---

## 💎 Product Catalog

The application includes a catalog through which the manufacturer can present jewelry models to partner stores.

Jewelry stores can browse available designs and use them when submitting work to the manufacturer instead of relying exclusively on external images or chat messages.

The catalog is integrated directly into the B2B ordering workflow.

---

## 👤 Partner Store Profile

Each partner jewelry store has a dedicated profile where its business/account information can be displayed and managed.

The profile system provides a simple mobile-friendly experience while keeping the store's information synchronized with the backend.

---

## 🧑‍💼 Partner Store Management

The manufacturer's administrative interface includes functionality for managing the jewelry stores that work with the workshop.

The manufacturer can access each store's information, review its orders, and maintain its account history, making long-term B2B relationships easier to organize.

---

## 💰 Store Accounts & Weight Calculations

Jewelry accounting often depends not only on monetary price but also on the weight of the material used.

Asameena includes functionality for managing:

- Order prices
- Original jewelry weight
- Adjusted weight
- Additional percentage calculations
- Monthly totals for each partner store

This allows the system to better reflect real jewelry-business accounting workflows rather than behaving like a generic e-commerce application.

---

## 📄 Monthly PDF Reports

One of the administrative features developed for Asameena is the ability to generate professional monthly account reports in **PDF** format for each partner jewelry store.

The reports were designed to include relevant business information such as:

- Order number
- Order date
- Order type
- Price
- Weight information
- Adjusted weight calculations
- Monthly totals

The PDF design was customized for Arabic content and provides the manufacturer with a professional way to summarize and share monthly B2B account statements with partner stores.

---

## 🔔 Order Updates & Notifications

The partner-store interface was designed to notify stores when information related to their submitted work changes.

The notification experience includes visual indicators and a recent-notifications interface so each jewelry store can quickly identify updates from the manufacturer regarding its orders.

---

## 🌐 Arabic & RTL Support

Asameena was designed primarily around an **Arabic user experience**.

This required special attention to:

- RTL layouts
- Arabic typography
- Form alignment
- Mobile input fields
- Arabic PDF generation
- Native mobile keyboard behavior

Arabic support was treated as a core application requirement rather than an afterthought.

---

# 🛠️ Technology Stack

The project uses a web-first architecture that was later adapted for native mobile distribution.

### Frontend

- HTML5
- CSS3
- JavaScript
- Tailwind CSS

### Backend & Services

- Firebase Authentication
- Firebase services for application data and storage

### Mobile

- Capacitor
- iOS
- Android
- Xcode

### Other Technologies

- PDF generation
- Image upload/storage
- Responsive Web Design
- RTL interface design

---

# 📱 From Web Application to Mobile App

Asameena originally ran as a browser-based application.

After the core system became functional, the project was converted into a mobile application using **Capacitor**.

This approach allowed the existing HTML, CSS, and JavaScript application to remain the core of the project while gaining access to native iOS and Android application packaging.

The Capacitor configuration uses:

```text
App ID: com.asameena.app
App Name: Asameena
```

Native iOS and Android projects were then generated from the web application.

---

## 🍎 iOS Integration

Preparing the application for iOS required more than simply wrapping the website.

The native iOS project was configured with the required permissions for features used by Asameena, including:

- Camera access
- Photo Library access
- Saving images to the Photo Library

The iOS configuration was also adapted for the application's Arabic-first experience.

Application icons and splash-screen assets were generated in the required native sizes using the Capacitor asset tooling.

---

# 🧩 Challenges & Solutions

Building Asameena involved several challenges, particularly when moving from a browser environment to native mobile WebViews.

## 1. Browser vs. Native WebView Behavior

### Challenge

Pages that worked correctly in a normal browser did not always behave the same way when executed inside the Android or iOS application.

### Solution

The application layout and JavaScript behavior were reviewed specifically for the native WebView environment instead of assuming that browser behavior would automatically transfer to the mobile application.

This became an important part of the testing process.

---

## 2. Mobile Scrolling

### Challenge

After converting the application with Capacitor, some pages contained more content than the screen height but could not be scrolled correctly inside the application.

The same pages could still scroll normally when opened directly in a browser.

### Solution

The page layout, viewport behavior, container heights, and CSS overflow rules were adjusted for the native application environment.

This ensured that scrolling was controlled by the application content rather than relying on browser-specific behavior.

---

## 3. Arabic Keyboard/Input Issues

### Challenge

Arabic text input behaved differently inside the native mobile application, even though it worked correctly in the browser.

Because Arabic is the primary language of Asameena, this was a critical issue.

### Solution

Input fields, document language configuration, RTL behavior, and mobile WebView handling were reviewed and adapted so Arabic input could work correctly throughout the application.

---

## 4. Firebase Authentication Inside the Mobile App

### Challenge

Authentication and page transitions that worked in the web version required additional attention when the same application was executed inside the native iOS environment.

### Solution

The authentication flow and application navigation were debugged specifically for Capacitor/iOS behavior, ensuring that Firebase authentication state and post-login navigation worked correctly inside the native application.

---

## 5. Complex Order Forms on Small Screens

### Challenge

Some jewelry orders require many fields, images, and controls.

As functionality increased, certain modal windows became too tall for mobile screens and could become difficult to use.

### Solution

The dialogs were redesigned around mobile constraints, including controlled scrolling inside modal content and better organization of form sections.

This allowed complex order forms to remain usable without filling the entire interface.

---

## 6. Image Upload Workflows

### Challenge

Different order types required different images, including jewelry photos and separate printing/reference images.

Keeping these uploads correctly connected to their corresponding orders required careful handling.

### Solution

Dedicated upload fields and storage logic were created for different image purposes so each image could be saved and displayed in the correct part of the order.

---

## 7. Arabic PDF Generation

### Challenge

Generating professional business reports in Arabic introduces additional difficulties compared with standard Latin-text PDFs, particularly with typography, text direction, alignment, and layout consistency.

### Solution

The PDF system was customized for Arabic output, including the use of an Arabic-compatible font and a layout designed specifically for customer account reports.

---

# 🎨 UI/UX Development

The interface evolved continuously during development based on real application usage.

Particular attention was given to:

- Mobile-first layouts
- Arabic RTL design
- Clear administrative controls
- Touch-friendly buttons
- Order-detail dialogs
- Customer-friendly forms
- Consistent visual feedback
- Responsive behavior across phones, tablets, and desktop browsers

The goal was not simply to create a management dashboard, but to make the system practical for daily use inside a real jewelry business.

---

# 🏗️ Development Approach

Asameena was developed iteratively.

Instead of defining every feature in advance, the application evolved as real business requirements appeared.

The development process included:

1. Building the initial partner-store and work-order workflows.
2. Adding authentication and individual accounts for partner jewelry stores.
3. Expanding order types and their specific fields.
4. Adding catalog functionality.
5. Developing administrative partner-store and account management.
6. Building monthly account PDF reports for partner stores.
7. Improving the mobile user experience.
8. Converting the web application to iOS and Android using Capacitor.
9. Testing and fixing WebView-specific behavior.
10. Preparing and publishing the iOS application.

This iterative process allowed the application to remain closely aligned with the actual workflow it was created to support.

---

# 🚀 App Store Release

A major milestone for the project was taking Asameena from a web application to a distributable iOS application.

The project went through the required native preparation, including:

- Capacitor iOS integration
- Xcode project preparation
- Application identifiers
- App icons
- Splash screens
- iOS permissions
- Native testing
- App Store preparation

The application was successfully published on the **Apple App Store** under the name:

## Asameena

**[Open the official App Store listing →](https://apps.apple.com/sa/app/asameena/id6752386204)**

Available for iPhone and iPad. The listing can be viewed without signing in to the business application; it presents the published product rather than an isolated portfolio demo.

This completed the transition from an internal web project into a real mobile application available through Apple's distribution platform.

---

# 📚 What I Learned

Asameena provided practical experience across the complete application-development lifecycle.

The project involved:

- Translating real business requirements into software features
- Designing B2B partner-store and manufacturer workflows
- Firebase authentication
- Data management
- File and image uploads
- Arabic and RTL application development
- Responsive/mobile-first UI design
- Complex form design
- PDF generation
- Debugging browser vs. WebView differences
- Capacitor
- Native iOS integration
- Android integration
- Xcode
- Mobile permissions
- Application assets
- Preparing a production application for the App Store

Most importantly, the project provided experience in continuously evolving a software system around real users and real operational requirements.

---

# 📌 Project Status

**Production / Published**

Asameena has progressed from an initial web-based jewelry management system to a mobile application and has been published on the **Apple App Store**.

Development continues as the system evolves and new improvements are introduced based on real-world usage.

---

# 👨‍💻 Author

Developed as a real-world software engineering project focused on digitizing communication, work orders, and account management between a small jewelry manufacturer and the jewelry stores it serves.

---

# 📄 License

This project was developed for a private business environment.

The source code, business logic, branding, and associated assets are not intended for redistribution without permission.
