# Deployment Guide

This document explains how to develop, test, and deploy updates to the Lyteforce Labs site.

## Workflow Overview
1. **Local Development**
   - Set up a local WordPress environment (e.g., LocalWP, MAMP, XAMPP).
   - Install the Understrap parent theme.
   - Import the current database and uploads from staging to match content and layout.

2. **Version Control**
   - Store only the underscore theme files in GitHub (not WordPress core, plugins, or parent theme).
   - Commit with clear messages

3. **Testing**
   - Check:
     - Responsive navbar and logo scaling
     - Footer layout without bullet points
     - Partner logos and event listings formatting
     - Forms for events, sponsorship and contact form
     - Mobile menu and button functionality

4. **Deployment**
   - Push to GitHub main branch.
   - Verify all pages and event listings on staging.
   - Deploy to live using the same file upload process.

5. **Project Management**
   - Track development tasks in GitHub Issues or Trello.
   - Require approval before pushing to production.
