# Week Two: Email Security with Microsoft Defender for Office 365

As part of my [30-Day MyDFIR Microsoft Challenge](https://github.com/Kassimali/30-Day-MyDFIR-Microsoft-Challenge/tree/main), I focused on email security using Microsoft Defender for Office 365. This week, I explored the tools Microsoft provides to protect users against phishing, malicious links, impersonation, and other email-based threats.

I organized my hands-on activities into three main tasks: configuring Safe Links and Anti-Phishing policies, exploring email investigation tools, and simulating phishing attacks using Attack Simulation Training.

## Task 1: Configure and Test Safe Links Policy

### Lab Setup

1. Created two users, Hassan Abd and Sarah Ali, in the Microsoft 365 Admin Center and assigned them Microsoft 365 E5 Trial.
2. Activated their mailboxes by signing in to their accounts.
3. Explored the different email security tools available under Email & Collaboration in the Microsoft Defender portal.
4. Created a Safe Links policy named `Mydifir-Kassim-SafeLinksPolicy`.
5. Enabled URL protection settings, including URL scanning and click tracking, to help protect users from malicious links.
6. Sent a test email containing a suspicious link to Sarah's mailbox to assess how the Safe Links policy handled it.

### Observations

Sarah received the email with a security warning, and the link was rewriten in the message. This demonstrated how Safe Links can help protect users from potentially malicious URLs.

Safe Links protects users by checking URLs at the time of delivery and, when configured, checking them again when users click the links. It can rewrite URLs and block access to malicious destinations based on the applicable policy settings and security verdicts.

Safe Links can protect URLs in supported email messages and Microsoft Office applications, as well as Microsoft Teams when the relevant protection is configured.

**Key takeaway:** Configuring Safe Links is an important step in reducing the risk of users accessing malicious websites through phishing emails.

## Task 2: Configure Anti-Phishing Protection and Explore Email Investigation Tools

### 1. Configure an Anti-Phishing Policy

I created an Anti-Phishing policy named `Mydifir-Kassim-AntiPhishingPolicy` and explored the available protection settings.

The configuration included:

- Adding high-profile users, such as the CEO, to the protected users list.
- Enabling impersonation protection for selected users.
- Configuring spoof intelligence and spoofing protection.
- Exploring policy actions for handling suspicious messages.

Anti-phishing protection helps organizations detect and respond to emails that attempt to impersonate trusted users, domains, or organizations.

Some common phishing techniques include:

- **Display-name spoofing:** An attacker uses a familiar person's name to make an email appear legitimate.
- **Domain impersonation:** An attacker uses a lookalike domain, such as `micros0ft.com` instead of `microsoft.com`.
- **Email spoofing:** An attacker forges sender information to make an email appear to originate from a trusted source.
- **Reply-to manipulation:** An attacker uses a different reply-to address to direct responses to an account under their control.

Microsoft Defender uses machine-learning-based detection and configured policy settings to help identify phishing and impersonation attempts.

### 2. Explore Microsoft Defender Email Security Tools

During this task, I explored several tools in the Microsoft Defender portal and learned how they can support email threat investigation and response.

#### Threat Explorer

Threat Explorer is an investigation tool that helps security analysts investigate email-related threats and review message and threat information.

It helps analysts answer questions such as:

- Who received a particular email?
- Was the message delivered, blocked, quarantined, or otherwise remediated?
- Was the message detected as phishing or malicious?
- Which recipients were affected?
- What links or attachments were associated with the message?

Analysts can filter messages using fields such as sender address, recipient, sender domain, subject, and other available message attributes. They can also investigate individual messages and examine relevant details, including URLs, attachments, and email headers where available.

**From a SOC analyst's perspective, Threat Explorer is an important starting point for investigating suspicious emails, identifying affected users, and understanding the scope of an email-based attack.**

#### Quarantine

Quarantine is where messages identified as potentially harmful or otherwise subject to quarantine policies can be held for review.

I explored how quarantine supports email security operations, including:

- Reviewing suspicious or malicious messages.
- Investigating messages that users report as phishing.
- Checking why an expected email was not delivered.
- Reviewing available message details before taking further action.

Depending on the applicable policy and permissions, authorized administrators can release messages or take other permitted actions.

**Key takeaway:** Threat Explorer helps analysts investigate email threats, while Quarantine helps them review and manage messages that have been held by security policies.

### 3. Understanding Defender for Office 365 Protection Capabilities

I also explored the relationship between the different email security features available in Microsoft Defender for Office 365.

**Safe Links**
- Helps protect users from malicious URLs.
- Can rewrite URLs and check them at the time of click.
- Can block access to URLs identified as malicious.

**Safe Attachments**
- Analyzes potentially unsafe email attachments.
- Uses detonation in a protected environment for supported scenarios to help identify malicious files before they reach users or are opened.

**Anti-Phishing Protection**
- Helps detect phishing, spoofing, and impersonation attempts.
- Provides additional protection for configured high-profile users and domains.
- Supports policy-based handling of suspicious messages, including quarantine and other configured actions.

These capabilities work together to reduce the risk of email-based attacks and provide security analysts with tools to investigate suspicious activity.

## Task 3: Simulate a Phishing Attack Using Attack Simulation Training

For the third task, I explored Microsoft's built-in Attack Simulation Training feature to simulate a phishing attack in a controlled lab environment.

This tool is useful for assessing how users respond to phishing attempts, identifying users who may need additional awareness training, and measuring the effectiveness of phishing education.

### What I Did

1. Opened Attack Simulation Training in the Microsoft Defender portal.
2. Created a credential-harvesting simulation.
3. Used the Microsoft-provided payload and landing page for the simulation.
4. Configured the simulation for the lab users.
5. Explored how the simulation can track user interactions and support follow-up training.

### Please view the attached Investigation-Report.md for further details

**From a SOC perspective, this provides an opportunity to understand the human side of email security.** Technical controls such as Safe Links and Anti-Phishing policies are important, but user awareness and timely reporting also play a significant role in reducing phishing risk.

All simulations were intended for the controlled lab environment and its designated test users.

## Screenshots and Evidence

The following screenshots document the configurations and results of my hands-on activities:

Mydifir-Kassim-SafeLinksPolicy

![Safe Link Policy](./screenshots/Mydifir-Kassim-SafeLinksPolicy)


Mydifir-Kassim-AntiPhishingPolicy

![Mydifir-Kassim-AntiPhishingPolicy](./screenshots/Mydifir-Kassim-AntiPhishingPolicy)

Sample phishing email received by the test user


![phishingEmailReceivedExample](./screenshots/phishingEmailReceivedExample)

Hassan Abdi Clicks the simulated phishing link
![HassanAbdiClicksMaliciouslink](./screenshots/HassanAbdiClicksMaliciouslink)

## What I Learned

During Week Two, I gained hands-on experience with Microsoft Defender for Office 365 and explored how its email security capabilities can be used to prevent, investigate, and respond to phishing attacks.

My key takeaways were:

- How to configure Safe Links and Anti-Phishing policies.
- How URL protection helps reduce the risk of users accessing malicious websites.
- How impersonation and spoofing protection can help protect high-profile users.
- How to use Threat Explorer to investigate suspicious emails and identify affected recipients.
- How Quarantine supports the review and management of suspicious messages.
- How Attack Simulation Training can help assess user awareness and identify training needs.

Most importantly, I learned that email security is not only about preventing malicious messages from reaching users. It also involves investigating suspicious activity, understanding the scope of an incident, taking appropriate response actions, and improving user awareness.

This hands-on exercise helped me connect email security configurations with practical SOC analyst responsibilities, particularly phishing investigation, threat triage, and incident response.

**Week Two completed. I am continuing to build my practical cybersecurity skills through the 30-Day MyDFIR Microsoft Challenge.**