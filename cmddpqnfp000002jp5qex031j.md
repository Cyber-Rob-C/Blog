---
title: "The Automation Habit That Changed How I Learn DevOps"
datePublished: Mon Jul 21 2025 23:04:34 GMT+0000 (Coordinated Universal Time)
cuid: cmddpqnfp000002jp5qex031j
slug: the-automation-habit-that-changed-how-i-learn-devops
tags: automation, devops, homelab

---

When I started learning DevOps, I kept hearing the same advice over and over:

> *“Get hands-on. Build a home lab. Automate everything.”*

So that’s what I did. But something unexpected happened along the way…

---

### Solving a Real Problem with a Simple Script

We work with a third-party vendor whose web portal occasionally changes without warning. These changes have caused connection issues and even unexpected service downtime.

They never notify us when changes happen.

So, I built a solution.

I wrote a small **Python script** that checks the vendor’s site for changes. It runs every 5 minutes using **systemd timers**, and if it detects something new, I get a **Discord notification** instantly.

That one project taught me more than any tutorial could have.

---

### What I Learned

This small real-world script became a crash course in DevOps fundamentals:

✅ How to use `requests` and `hashlib` in Python for web monitoring  
✅ How to configure `systemd` timers for scheduled tasks (better than cron in many cases)  
✅ How to send automated alerts to Discord using webhooks  
✅ How to write, test, and deploy scripts that actually *solve a problem*

Most importantly, I learned that **automation isn’t just about convenience**.  
It’s about understanding systems deeply enough to make them work for you.

---

### Your Home Lab Should Serve You

I used to build things in my home lab just to practice commands or spin up containers.  
Now I treat my lab like a proving ground for solving problems I face at work.

That one shift—automating real problems, not just running labs for their own sake—supercharged my DevOps journey.

---

### Final Thoughts

If you’re learning DevOps, here’s my advice:

**Don’t wait for the perfect project idea. Solve a problem in your world. Automate something that annoys you.**

Chances are, it’ll teach you more than a course ever could.

---

**Have you built something in your lab that solved a real-world issue? I’d love to hear about it.** Let’s learn from each other.