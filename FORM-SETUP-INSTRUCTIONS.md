# Form Setup Instructions - EmailJS Integration (Unlimited & Free)

## Overview
The contact and careers forms have been updated to use **EmailJS**, a completely free service that handles unlimited form submissions without requiring backend code.

## Why EmailJS?
✅ **Completely Free** - No monthly limits or costs
✅ **Unlimited Submissions** - Send as many emails as you want
✅ **No Backend Required** - Works on static hosting (Vercel)
✅ **Easy Setup** - Just add your credentials
✅ **Professional** - Used by thousands of companies
✅ **Reliable** - 99.9% uptime

## Forms Updated
1. **Contact Form** (`contact.html` & `scube1/contact.html`)
   - Fields: First Name, Last Name, Email, Phone, Subject, Message
   - Sends to: sales@scubeindustries.com

2. **Careers Form** (`careers.html` & `scube1/careers.html`)
   - Fields: Full Name, Email, Position, Resume Link
   - Sends to: sales@scubeindustries.com

## Setup Steps

### Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Click "Sign Up Free"
3. Create account with your email (sales@scubeindustries.com)
4. Verify your email

### Step 2: Add Email Service
1. Go to **Email Services** in the dashboard
2. Click **Add New Service**
3. Select **Gmail** (or your email provider)
4. Follow the authentication steps
5. Copy your **Service ID** (e.g., `service_abc123def`)

### Step 3: Create Email Templates
1. Go to **Email Templates** in the dashboard
2. Click **Create New Template**

**For Contact Form Template:**
- Template Name: `contact_form`
- Subject: `New Contact Form Submission from {{from_name}}`
- Content:
```
Name: {{from_name}}
Email: {{from_email}}
Phone: {{phone}}
Subject: {{subject}}

Message:
{{message}}
```

**For Careers Form Template:**
- Template Name: `careers_form`
- Subject: `New Career Application from {{full_name}}`
- Content:
```
Name: {{full_name}}
Email: {{from_email}}
Position: {{position}}
Resume Link: {{resume_link}}
```

### Step 4: Get Your Credentials
1. Go to **Account** → **API Keys**
2. Copy your **Public Key** (starts with `key_`)
3. This is what you'll use in the HTML files

### Step 5: Update HTML Files
Replace `YOUR_PUBLIC_KEY_HERE` with your actual public key in these files:
- `contact.html` - Line with `emailjs.init("YOUR_PUBLIC_KEY_HERE")`
- `scube1/contact.html` - Same line
- `careers.html` - Same line
- `scube1/careers.html` - Same line

Also replace `YOUR_SERVICE_ID_HERE` and `YOUR_TEMPLATE_ID_HERE` with your actual IDs:
- Service ID: From Email Services
- Template ID: From Email Templates (e.g., `contact_form`, `careers_form`)

### Step 6: Test the Forms
1. Go to your website
2. Fill out the contact form and submit
3. Check your email for the submission
4. Confirm it works in EmailJS dashboard

## EmailJS Dashboard Features
- **View all submissions** - See every form submission
- **Email logs** - Track delivery status
- **Analytics** - Monitor form activity
- **Manage templates** - Edit email templates anytime
- **Rate limits** - Unlimited for free plan

## Troubleshooting

### Form not sending?
1. Check browser console for errors (F12)
2. Verify Public Key is correct
3. Verify Service ID and Template ID are correct
4. Check EmailJS dashboard for error logs

### Not receiving emails?
1. Check spam/junk folder
2. Verify email service is connected in EmailJS
3. Check template variables match form field names
4. Test with a different email address

### Need help?
- EmailJS Docs: https://www.emailjs.com/docs/
- EmailJS Support: https://www.emailjs.com/contact/

## Security Notes
- Public Key is safe to expose in frontend code
- Never expose your Private Key
- EmailJS handles all email delivery securely
- No sensitive data is stored on your server

## Pricing
- **Free Plan**: Unlimited emails, unlimited submissions
- **Premium Plans**: Available if you need advanced features

## Alternative Solutions (if needed)
1. **Basin** - Simple form backend (UNLIMITED & FREE)
2. **Vercel Functions** - Serverless backend on Vercel (UNLIMITED)
3. **Firebase** - Google's backend service
4. **AWS Lambda** - Amazon's serverless functions

---

**Status**: ✅ Ready to deploy
**Last Updated**: April 2026
