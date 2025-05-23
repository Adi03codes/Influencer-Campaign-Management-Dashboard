# Influencer-Campaign-Management-Dashboard
An end-to-end SaaS dashboard for planning, executing, and analyzing influencer campaigns on Instagram.


## Tech Stack
| Layer        | Technology                                 |
|--------------|---------------------------------------------|
| Frontend     | Next.js, TypeScript, Tailwind CSS, ShadCN UI |
| State Mgmt   | Context API                                 |
| Backend      | Node.js, MongoDB                            |
| Auth         | OAuth2                                      |
| Deployment   | Vercel (Frontend), AWS EC2/S3               |

## Features
- 📊 Unified campaign dashboard
- 📨 DM Tracking by user, time & campaign
- 📁 Asset management with AWS S3
- 🔒 Secure login with OAuth2

## UI Pages
- **Campaign Manager**
- **Outreach Log**
- **Analytics & Reports**
- **Team Settings & Collaboration**

## Folder Structure
```
/influencer-dashboard
├── /frontend
│   ├── /pages
│   ├── /components
│   └── /ui
├── /backend
│   ├── /models
│   ├── /routes
└── /docs
```

## Core Backend Code (Campaign Routes)
```js
// backend/routes/campaignRoutes.js
const express = require('express');
const router = express.Router();
const { createCampaign, fetchCampaigns } = require('../controllers/campaignController');

router.post('/create', createCampaign);
router.get('/list', fetchCampaigns);

module.exports = router;
