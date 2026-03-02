# Inventory App Portfolio Artifact

Project Overview

The primary objective of this project was to develop a mobile utility for Mobile2App Company to enable efficient tracking and monitoring of warehouse inventory. Designed to replace manual record-keeping with a reliable digital system, the app aims to reduce organizational chaos and prevent financial loss caused by stock shortages. It serves three professional roles: the Warehouse Worker for quick updates, the Small Business Owner for accurate records, and the Manager for monitoring trends and emergency alerts.

User-Centered Design

To produce a user-centered UI, the application features three primary screens:

- Login/Signup Screen: Utilizes TextInputLayout and obscuring password fields to ensure secure authentication for returning and new users.

- Main Inventory Grid: Employs a RecyclerView with a GridLayoutManager to display items as "Cards," providing a clear visual overview of stock levels.

- Notification Settings: Allows users to toggle and manage SMS permissions, which are required for automated zero-stock alerts.

My designs were successful because they prioritized Interaction Ergonomics; for example, I placed the primary "Add Item" action in a Floating Action Button (FAB) at the bottom-right for easy thumb reach. Adhering to Material Design 3 guidelines ensured the app felt like a native, intuitive Android experience.

Coding Approach and Techniques

I followed the Modern Android Architecture (MVVM) pattern to ensure a clean separation of concerns between the UI and the underlying data.

- Data Layer: I implemented a Room Database (SQLite) with two entities—Inventory and User—as the "Single Source of Truth".

- UI Layer: Activities and Fragments observe data exposed by the ViewModel, ensuring the UI remains responsive and synchronized with the database.

These strategies—specifically the use of persistent storage and decoupled architecture—are highly applicable to my future professional goals, such as developing a 2D Metroidvania game or a historical audio archive application.

Testing and Functionality

Testing was conducted using the Android Emulator to verify core CRUD (Create, Read, Update, Delete) operations and permission handling. This process was vital because it revealed a critical "App isn't installed" error; I discovered that for the Android launcher to recognize the app, the MainActivity must have the android:exported attribute set to true in the AndroidManifest.xml. Testing also ensured that the app degrades gracefully if a user denies SMS permissions, allowing the inventory grid to remain functional while disabling automated alerts.

Innovation and Challenges

significant challenge was ensuring the app was visible on the home screen while maintaining security. I had to innovate by carefully auditing the Intent Filters and activity attributes within the manifest to bridge the gap between internal code security and OS visibility. Additionally, implementing a TextWatcher to dynamically enable the "Say Hello" or "Login" buttons based on user input helped create a more responsive and "alive" feel to the interface.

Successful Demonstration of Skills

I was particularly successful in demonstrating my knowledge of database persistence and data flow. Successfully linking a RecyclerView to an active SQLite database through a custom Adapter allowed me to show I can handle the full lifecycle of a mobile application—from user input and secure storage to dynamic UI updates.
