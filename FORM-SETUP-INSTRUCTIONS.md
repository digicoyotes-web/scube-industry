# Form Setup Instructions - Formspree Integration

## Overview
The contact and careers forms have been updated to use **Formspree**, a free service that handles form submissions without requiring backend code.

## Forms Updated
1. **Contact Form** (`contact.html` & `scube1/contact.html`)
   - Endpoint: `https://formspree.io/f/xyzabc123`
   - Fields: First Name, Last Name, Email, Phone, Subject, Message

2. **Careers Form** (`careers.html` & `scube1/careers.html`)
   - Endpoint: `https://formspree.io/f/xyzabc456`
   - Fields: Full Name, Email, Phone, Location, Position, Resume

## Setup Steps

### Step 1: Create Formspree Account
1. Go to https://formspree.io
2. Sign up with your email (sales@scubeindustries.com)
3. Verify your email

### Step 2: Create Forms
1. **For Contact Form:**
   - Click "New Form"
   - Name it: "Contact Form"
   - Copy the form endpoint (e.g., `https://formspree.io/f/abc123def`)
   - Replace `xyzabc123` in `contact.html` with your actual endpoint

2. **For Careers Form:**
   - Click "New Form"
   - Name it: "Careers Application"
   - Copy the form endpoint
   - Replace `xyzabc456` in `careers.html` with your actual endpoint

### Step 3: Update HTML Files
Replace the placeholder endpoints in these files:
- `contact.html` - Line with `action="https://formspree.io/f/xyzabc123"`
- `scube1/contact.html` - Same endpoint
- `careers.html` - Line with `action="https://formspree.io/f/xyzabc456"`
- `scube1/careers.html` - Same endpoint

### Step 4: Test the Forms
1. Go to your website
2. Fill out the contact form and submit
3. Check your email for the submission
4. Confirm it works in Formspree dashboard

## Features
✅ **Free** - No cost for basic usage
✅ **No Backend Required** - Works on static hosting (Vercel)
✅ **Email Notifications** - Get emails for each submission
✅ **File Uploads** - Careers form can handle resume uploads
✅ **Spam Protection** - Built-in CAPTCHA available
✅ **Dashboard** - View all submissions in one place

## Pricing
- **Free Plan**: Up to 50 submissions/month
- **Pro Plan**: Unlimited submissions ($25/month)

## Alternative Solutions
If you need more features, consider:
1. **EmailJS** - Client-side email sending
2. **Vercel Functions** - Serverless backend on Vercel
3. **Firebase** - Google's backend service
4. **AWS Lambda** - Amazon's serverless functions

## Support
- Formspree Docs: https://formspree.io/help
- Email: support@formspree.io
