
# 📘 Scope Document: Matrimonial Website – Functional-Level Breakdown

## 👤 USER REGISTRATION & PROFILE

| Functionality                            | Free User               | Paid User                | BuddyPress Feasibility    | Custom Development Needed |
|-----------------------------------------|-------------------------|--------------------------|---------------------------|---------------------------|
| Create profile                          | ✅                      | ✅                       | ✅ (BuddyPress core)       | ❌                        |
| Upload multiple photos                  | Limited (1-2)           | Unlimited                | ✅ (xProfile + Media plugin) | ❌                     |
| Profile photo privacy (blur/hide)       | ❌                      | ✅ (Premium feature)     | ❌                         | ✅                        |
| Profile approval / admin verification   | ✅ (by default)         | ✅                       | ✅ (via admin moderation)  | ❌                        |
| Profile verification badge              | ❌                      | ✅ (via KYC/doc upload)  | ❌                         | ✅                        |
| Partner preferences (Age, height, etc.) | ✅                      | ✅                       | ✅ (xProfile fields)       | ❌                        |
| View own profile completeness %         | ❌                      | ✅                       | ❌                         | ✅                        |

## 🔍 SEARCH & MATCHING ENGINE

| Functionality                              | Free User             | Paid User              | BuddyPress Feasibility    | Custom Development Needed |
|-------------------------------------------|-----------------------|------------------------|---------------------------|---------------------------|
| Basic search (Age, Religion, Caste)       | ✅                    | ✅                     | ✅ (BP Profile Search)     | ❌                        |
| Advanced filters (Education, Income)      | ❌                    | ✅                     | ✅ (custom filters)        | ❌                        |
| Horoscope matching                        | ❌                    | ✅                     | ❌                         | ✅ (custom algorithm)     |
| View mutual matches                       | ❌                    | ✅                     | ❌                         | ✅                        |
| Daily match recommendations               | ❌                    | ✅                     | ❌                         | ✅ (via scheduled cron)   |
| Search by profession, mother tongue, etc. | ✅                    | ✅                     | ✅                         | ❌                        |

## 📩 INTERACTION FEATURES

| Functionality                              | Free User             | Paid User              | BuddyPress Feasibility    | Custom Development Needed |
|-------------------------------------------|-----------------------|------------------------|---------------------------|---------------------------|
| Send Interest                              | ✅ (limited)          | ✅ (unlimited)         | ✅ (via friend request)    | ✅ (limit + logic change) |
| Cancel Interest                            | ❌                    | ❌                    | ❌ (not default behavior)  | ✅ (custom logic needed)  |
| Accept/Decline Interest                    | ✅                    | ✅                     | ✅ (friends system)        | ❌                        |
| Send Super Interest                        | ❌                    | ✅                     | ❌                         | ✅ (custom button + counter) |
| Shortlist Profiles                         | ✅                    | ✅                     | ✅ (Favorites plugin)      | ❌                        |
| View contact number                        | ❌                    | ✅                     | ❌                         | ✅                        |
| Message other users                        | ❌                    | ✅ (post interest match) | ✅ (BP Better Messages)  | ✅ (gate by match/plan)  |
| View who viewed your profile               | ❌                    | ✅                     | ✅ (with plugin)           | ❌                        |

## 📞 COMMUNICATION LOGS

| Functionality                              | Free User             | Paid User              | BuddyPress Feasibility    | Custom Development Needed |
|-------------------------------------------|-----------------------|------------------------|---------------------------|---------------------------|
| View accepted interests                    | ✅                    | ✅                     | ✅                         | ❌                        |
| View received interests                    | ✅                    | ✅                     | ✅                         | ❌                        |
| View sent interests                        | ✅                    | ✅                     | ✅                         | ❌                        |
| View declined/cancelled interests          | ❌                    | ✅                     | ❌                         | ✅                        |
| Chat categorized tabs (Interest, Accepted) | ❌                    | ✅                     | ❌                         | ✅ (extend chat plugin)   |
| View call logs                             | ❌                    | ✅                     | ❌                         | ✅ (via Twilio/WebRTC)    |

## 💼 MEMBERSHIP PLANS

| Feature                                   | Free User             | Paid Tiers            | BuddyPress Feasibility    | Custom Development Needed |
|------------------------------------------|------------------------|------------------------|---------------------------|---------------------------|
| Plan types (Gold, Diamond, Platinum)     | ❌                    | ✅                     | ✅ (Paid Memberships Pro)  | ❌                        |
| Feature-based limits (contacts, chat)    | ❌                    | ✅                     | ❌                         | ✅                        |
| Duration options (1mo, 3mo, Lifetime)    | ❌                    | ✅                     | ✅                         | ❌                        |
| Assisted plan (Relationship Manager)     | ❌                    | ✅                     | ❌                         | ✅                        |
| One-time and recurring billing           | ❌                    | ✅                     | ✅                         | ❌                        |
| Cancel membership anytime                | ❌                    | ✅                     | ✅                         | ❌                        |

## 📊 DASHBOARDS & REPORTING

| Functionality                              | Free User             | Paid User              | BuddyPress Feasibility    | Custom Development Needed |
|-------------------------------------------|-----------------------|------------------------|---------------------------|---------------------------|
| Profile view stats                        | ❌                    | ✅                     | ✅ (with plugin)           | ❌                        |
| Match engagement analytics                | ❌                    | ✅                     | ❌                         | ✅                        |
| Monthly performance reports               | ❌                    | ✅                     | ❌                         | ✅                        |
| Admin-level reports                       | N/A                   | N/A                    | ✅                         | ✅ (for custom metrics)   |

## 🛡️ SECURITY & MODERATION

| Functionality                              | Free User             | Paid User              | BuddyPress Feasibility    | Custom Development Needed |
|-------------------------------------------|-----------------------|------------------------|---------------------------|---------------------------|
| Report user/block profile                 | ✅                    | ✅                     | ✅ (report/block plugin)   | ❌                        |
| Admin moderation of new profiles          | ✅                    | ✅                     | ✅                         | ❌                        |
| Photo and data privacy control            | Limited               | Full                   | ❌                         | ✅                        |
| Hide/show phone numbers & photos          | ❌                    | ✅                     | ❌                         | ✅                        |

## 🔍 Summary: Feature Development Mapping

### 💡 Core Plugin-Supported Features
- User registration & profile (BuddyPress)
- Standard search & profile filters
- Basic member interactions (friendship, messaging)
- Paid plans and access levels (PMP integration)
- Basic analytics and activity tracking

### 🛠️ Custom Development Required
- Horoscope-based matching
- Sharpfinder (match percentage logic)
- Interest cancellation logic
- Super interest limits
- Relationship manager assignment
- Photo/contact privacy controls
- Categorized chat view (Interest, Accepted, Calls)
- Full call logging and video chat
- Enhanced dashboards & analytics
