
# ✅ Developer Task List for Matrimonial Website (Shaadi.com / Jeevansathi Style)

This document outlines all functional and technical requirements for building a full-featured matrimonial website using **WordPress + BuddyPress**. Tasks are categorized into plugin-supported items (out-of-the-box or minor customization) and custom development work.

---

## 🔹 Plugin-Supported Tasks (BuddyPress / Paid Memberships Pro)

### 👤 User Profile & Registration
- [ ] Enable BuddyPress core features: user registration, profile creation, activity stream.
- [ ] Add xProfile groups and fields for:
  - Basic Info: Name, Age, Gender, Marital Status
  - Partner Preferences: Age range, Height, Religion, Caste, etc.
  - Education, Profession, Salary
  - Lifestyle Habits: Drinking, Smoking, Food Habits
- [ ] Enable profile moderation by admin before display (using BuddyPress moderation plugin or custom approval hooks).
- [ ] Add "Verified" and "Just Joined" badges using BuddyPress Member Types or user meta.

### 🔍 Search & Filters
- [ ] Use **BP Profile Search** plugin to add filters for Member Directory.
- [ ] Add filters for religion, caste, profession, location, and education.
- [ ] Support filter presets (e.g., “Recommended Matches”, “New Profiles”).

### 📩 Interest & Communication
- [ ] Use **BP Friends** to implement "Send Interest" and "Accept Interest" features.
- [ ] Use **Favorites plugin** for "Shortlist Profile".
- [ ] Use **BP Better Messages** for 1-on-1 chat after mutual interest.
- [ ] Use PMP conditionals to restrict chat access to paid users.

### 💼 Membership Plans
- [ ] Install **Paid Memberships Pro**.
- [ ] Create plans: Free, Pro, Pro Max, Pro Supreme, Assisted.
- [ ] Configure plan features: contact views, messaging access, super interest limits.
- [ ] Enable recurring billing and one-click cancellation for users.

### 📊 Activity Logs
- [ ] Track and display Interests Sent, Received, Accepted, Declined using BuddyPress notifications and custom post types.
- [ ] Show logged-in user dashboard with a summary of activity (e.g., Interests Sent, Views, Chats).

### 🛡 Privacy & Moderation
- [ ] Add a report/block user plugin to enable safe user experience.
- [ ] Restrict visibility of profile photos and contact information for free users using PMP shortcodes.
- [ ] Set up moderation workflow for photo and profile content.

---

## 🔸 Custom Development Tasks

### 🔁 Matching Engine
- [ ] Implement horoscope compatibility matching based on xProfile fields.
- [ ] Develop **Sharpfinder** algorithm: calculates profile match score based on user preferences.
- [ ] Match score should be used to highlight profiles in search results.

### 🛠 Enhanced Interest System
- [ ] Override BuddyPress Friend system to prevent cancellation of interests.
- [ ] Track interest states: Sent, Accepted, Declined, Cancelled (by recipient only).
- [ ] Create “Super Interest” functionality:
  - Limit super interests per plan (stored in user meta).
  - Reset counters daily or monthly via cron.

### 💬 Messenger Enhancements
- [ ] Modify BP Better Messages UI to show tabs: Interest, Acceptance, Calls.
- [ ] Filter conversations by interest state.
- [ ] Add notification badges for each tab.

### 📞 Call System
- [ ] Integrate WebRTC/Twilio for voice/video calls between matched users.
- [ ] Log all calls: store date/time, participants, duration, and status.
- [ ] Show call log in user dashboard and Messenger Call tab.

### 📈 Reports & Dashboards
- [ ] Create a user dashboard that includes:
  - Monthly summary: Profile Views, Interests, Messages.
  - Engagement charts.
- [ ] Admin Dashboard:
  - Sitewide metrics: new signups, matches made, plans sold.
  - Top performing users and categories.

### 🤝 Assisted Matrimony
- [ ] Assign relationship manager to Assisted plan members.
- [ ] Provide manager profile view for assigned users.
- [ ] Allow callback or meeting scheduling (integrate Calendly or similar).

---

## 🧩 Plugin & Code Structure Recommendations

- `/wp-content/plugins/matrimony-core/`: All custom logic (match score, interest system, call logs).
- `/wp-content/plugins/matrimony-assist/`: Admin-user relationship module, callback requests.
- `/wp-content/themes/matrimony-theme/`: UI/UX templates for profile view, search, Messenger tabs, dashboards.

---

## 🧠 Summary

This task list ensures the full scope of a feature-rich matrimonial website is covered. Custom development focuses on matchmaking algorithms, tier-based limits, communication enhancements, and assisted workflows. Plugins are leveraged where feasible to optimize time and reduce complexity.
