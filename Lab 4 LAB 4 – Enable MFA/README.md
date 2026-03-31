# LAB 4 – Enable MFA (Multi-Factor Authentication)

**Goal:** Secure user accounts by enabling Multi-Factor Authentication (MFA) for selected users in Microsoft Entra ID / Azure AD.

---

## Step 1: Sign in to Azure Portal

1. Open **https://portal.azure.com/**  
2. Sign in with an **admin account** that has **Global Administrator** or **Privileged Authentication Administrator** role.  

**Screenshot placeholder:**  
`![Admin login](screenshots/step1_admin_login.png)`

---

## Step 2: Navigate to MFA Settings

1. Go to **Microsoft Entra ID / Azure Active Directory → Users**  
2. Click **Multi-Factor Authentication** (located at the top menu or under Security settings)  
3. This will open the **MFA management portal** in a new window.  

**Screenshot placeholder:**  
`![MFA portal](screenshots/step2_mfa_portal.png)`

---

## Step 3: Select Users for MFA

1. In the MFA portal, you will see a list of all users.  
2. Select the users you want to enable MFA for, e.g.:  
   - HR User  
   - IT Admin  
   - John Doe  
3. Click **Enable** from the right-hand menu.  
4. Confirm the action when prompted.  

**Screenshot placeholder:**  
`![Enable MFA users](screenshots/step3_enable_mfa.png)`

---

## Step 4: Enforce MFA

1. After enabling MFA, the status will be **Enabled** but users have not yet registered.  
2. To enforce registration:  
   - Select the user(s)  
   - Click **Enforce**  
3. Users will be required to set up MFA at next login.  

**Screenshot placeholder:**  
`![Enforce MFA](screenshots/step4_enforce_mfa.png)`

---

## Step 5: Test MFA Login

1. Open a **new incognito/private browser window**  
2. Log in as a user for whom MFA is enabled (e.g., HR User):  
   - **Username:** hr.user@yourlab.onmicrosoft.com  
   - **Password:** *(the one you set during user creation)*  
3. You should be prompted to **register an additional verification method**, such as:  
   - Microsoft Authenticator app  
   - Phone call  
   - Text message  

**Screenshot placeholder:**  
`![MFA prompt](screenshots/step5_mfa_prompt.png)`

---

## Step 6: Complete MFA Registration

1. Follow the on-screen instructions to set up the verification method.  
2. Once complete, the user will see a **confirmation message**.  
3. MFA is now active for the account.  

**Screenshot placeholder:**  
`![MFA complete](screenshots/step6_mfa_complete.png)`

---

## Step 7: Verify MFA Enforcement

1. Log out and log back in as the same user.  
2. The system should prompt for the **second factor** before access is granted.  
3. Repeat for other users as needed to ensure MFA is enforced.

**Screenshot placeholder:**  
`![MFA verified](screenshots/step7_mfa_verified.png)`

---

## Step 8: Summary

- **Users protected by MFA:** HR User, IT Admin, John Doe  
- **MFA method:** Authenticator app, SMS, or call  
- **Lab outcome:** All selected users are now required to use MFA for login, enhancing security.


- Replace all screenshot placeholders (`screenshots/*.png`) with your actual images.  
- Optional: Add GIFs showing the MFA login process for visual clarity.  
- Keep numbering consistent with lab steps.
