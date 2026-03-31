# RBAC LAB 3 – Role-Based Access Control

**Goal:** Implement Role-Based Access Control (RBAC) by creating users, groups, and assigning roles in Microsoft Entra ID / Azure AD.

## Step 1: Assign Roles to Groups

**Roles to assign:**

| Group     | Role                              |
|-----------|----------------------------------|
| IT Admin  | User Administrator / Global Admin |
| HR Team   | User Reader / HR limited role    

**Steps to assign roles:**  
1. Go to **Microsoft Entra ID → Roles and administrators**  
2. Select the desired role (e.g., **User administrator**)  
3. Click **+ Add assignments**  
4. Select the group (e.g., IT Admin)  
5. Click **Add**

## Step 2: Test RBAC

**Steps to test:**

### Log in as HR User
1. Open a **new incognito/private browser window**  
2. Go to **https://portal.azure.com/**  
3. Sign in with:  
   - Username: `hr.user@yourlab.onmicrosoft.com`  
   - Password: *(the password you set during user creation)*  

### Verify Permissions
- **Allowed:** View users, view groups  
- **Blocked:** Cannot create or delete users, cannot assign roles, cannot manage IT resources  

**Example Test:**  
1. Go to **Users → All Users** → HR User can **view users**  
2. Go to **Groups → IT Admin** → HR User cannot modify the group  
3. Try a restricted feature → Should see **“Access Denied”**

**Screenshot placeholders:**  
`![HR User login](screenshots/step5_hr_login.png)`  
`![HR User blocked action](screenshots/step5_hr_blocked.png)`

### Repeat for other users
- **IT Admin:** Full access  
- **John Doe:** Limited access / self-view only

---

## Step 6: Summary

- **Users:** HR User, IT Admin, John Doe  
- **Groups:** HR Team, IT Admin  
- **Role Assignments:** IT Admin → Admin role, HR Team → Reader/HR role  
- **RBAC Test:** Confirmed users inherit permissions through group membership

 Lab complete! RBAC is successfully implemented.

