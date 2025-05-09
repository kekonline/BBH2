### 🕵️‍♂️ Web Application Reconnaissance Checklist (Bug Bounty Hunting)

---

#### 1. 🔍 **Initial Research & Awareness**

* **Check for updates and new releases**

  * Visit the official website or GitHub repo for version history.
  * Example: Compare version 3.0 to 2.9 for newly introduced features.
* **Read release notes**

  * Understand what changed (new features, bug fixes, deprecations).
  * Focus on security-relevant changes.
* **Explore documentation**

  * Learn how the app works, especially admin or developer features.
  * Example: Look for hidden endpoints or debug modes.
* **Understand the frameworks used**

  * Identify the technologies and libraries.
  * Tools: Wappalyzer, BuiltWith.
  * Example: “Uses Laravel 10 and Vue 3” → check their known issues.

---

#### 2. 🧠 **Intelligence Gathering from the Community**

* **Read GitHub issues and discussions**

  * Look for open bugs, misconfigurations, or insecure patterns.
* **Check online issues**

  * Search platforms like Reddit, Stack Overflow, HackerOne, or Twitter (X) for reports or questions about the app.
  * Example: Search for “AppName XSS” or “AppName bug report”.

---

#### 3. 🧪 **Hands-on Familiarization**

* **Test the app**

  * Interact with it like a regular user.
  * Note all routes, inputs, and how the app behaves under stress.
* **Get familiar with app flows**

  * Understand user roles, login logic, how forms behave, etc.
  * Example: Can you register and reset passwords without email verification?

---

#### 4. ♻️ **Regression Testing**

* **Look into past vulnerabilities**

  * Find old CVEs or past bug bounty reports.
  * Try reproducing them in the current version.
  * Example: “SQLi in /api/search was fixed in 2022 – test again with bypasses.”
* **Regression issues**

  * See if fixes were poorly implemented or accidentally reintroduced.

---

#### 5. 🧰 **If Source Code is Publicly Available**

* **Download and inspect the source code**

  * Example: Clone the GitHub repository.
* **Install and run the app locally**

  * Enables dynamic testing and easier debugging.
* **Understand the app logic**

  * Look for:

    * Hardcoded secrets
    * Dangerous functions
    * Lack of sanitization
* **Check code changes between versions**

  * Use `git diff` to track what changed and if new features introduced risky logic.
  * Example: `git diff v2.0..v3.0`

---

### ✅ Summary Flow

1. **Research** – Know the app, its tech, and its updates.
2. **Community Intel** – Read what others discovered.
3. **Hands-on Testing** – Explore and break things ethically.
4. **Historical Review** – Old bugs are gold.
5. **Source Code Review** – If open, use it to your full advantage.

---

