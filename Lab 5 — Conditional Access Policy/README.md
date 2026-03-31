# LAB 5 – Conditional Access Policy

**Goal:** Create and test a Conditional Access Policy to enforce security requirements like MFA, location restrictions, or device compliance for selected users.

---

## Step 1: Sign in to Azure Portal

1. Open **https://portal.azure.com/**  
2. Sign in with an **admin account** that has **Global Administrator** privileges.  

**Screenshot placeholder:**  
`![Admin login](screenshots/step1_admin_login.png)`

---

## Step 2: Navigate to Conditional Access

1. Go to **Microsoft Entra ID / Azure Active Directory → Security → Conditional Access**  
2. Click **+ New policy** to create a new Conditional Access policy.  

**Screenshot placeholder:**  
`![Navigate CA](screenshots/step2_ca_portal.png)`

---

## Step 3: Name the Policy

1. Enter a descriptive **Policy Name**, e.g.:  
   - `HR Users MFA Policy`  
2. Optional: Add a description for clarity.  

**Screenshot placeholder:**  
`![Policy name](screenshots/step3_policy_name.png)`

---

## Step 4: Assign Users or Groups

1. Under **Assignments → Users and groups**, select **Users and groups**  
2. Choose the target users or groups for this policy, e.g.:  
   - HR Team  
   - IT Admin group (if desired)  
3. Click **Select** to confirm  

**Screenshot placeholder:**  
`![Assign users](screenshots/step4_assign_users.png)`

---

## Step 5: Assign Cloud Apps

1. Under **Assignments → Cloud apps or actions**, select **Include → All cloud apps** or specific apps (e.g., Microsoft 365)  
2. Click **Select**  

**Screenshot placeholder:**  
`![Assign apps](screenshots/step5_assign_apps.png)`

---

## Step 6: Configure Conditions (Optional)

You can configure conditions like:  

- **Sign-in risk:** Medium or high risk users  
- **Locations:** Require MFA if login from untrusted locations  
- **Device platforms:** Apply only to Windows, iOS, Android, etc.  

**Example:** Require MFA for HR Team only when signing in outside corporate IP.  

**Screenshot placeholder:**  
`![Conditions](screenshots/step6_conditions.png)`

---

## Step 7: Configure Access Controls

1. Under **Access controls → Grant**, select:  
   - **Require multi-factor authentication**  
   - Optional: Require compliant device, require password change, etc.  
2. Click **Select**  

**Screenshot placeholder:**  
`![Access controls](screenshots/step7_access_controls.png)`

---

## Step 8: Enable Policy

1. Set **Enable policy → On**  
2. Click **Create** to save the policy  

**Screenshot placeholder:**  
`![Enable policy](screenshots/step8_enable_policy.png)`

---

## Step 9: Test Conditional Access Policy

1. Open a **new incognito/private browser window**  
2. Log in as a user in the targeted group (e.g., HR User)  
3. Verify the policy is applied:  
   - MFA is prompted if configured  
   - Access blocked or restricted if conditions are not met  

**Screenshot placeholder:**  
`![Test CA](screenshots/step9_test_policy.png)`

---

## Step 10: Summary

- **Policy created:** HR Users MFA Policy  
- **Users affected:** HR Team (and optional IT Admin)  
- **Cloud Apps:** All or selected apps  
- **Conditions:** Optional (location, device, risk)  
- **Enforcement:** MFA or other controls applied based on conditions  


- Replace all screenshot placeholders (`screenshots/*.png`) with your actual images.  
- Keep the folder structure consistent: e.g., `screenshots/stepX_description.png`  
- Optional: Add GIFs showing login and MFA prompts for clarity.
