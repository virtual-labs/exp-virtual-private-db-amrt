<b>Step 1: Administrator Authentication</b>

1. On the "Admin Login" screen, enter the administrator credentials.
   - Username: `admin`
   - Password: `admin123`
   <br>
   <img src="images/adminLogin.png" alt="Admin Login">
   <br>
2. Click the <b>Login as Admin</b> button to proceed.

<br>
<img src="images/adminLogin2.png" alt="Admin Login">
<br>


<b>Step 2: Database Initialization</b>

1. Click the Create and Populate Employee Table button to populate the database with sample employee records across different departments (HR, Sales, Finance, and IT).
   <br>
   <img src="images/populateTable.png" alt="Populate Table">
   <br>
2. Click <b>Continue to add Row-Level Security (RLS) policies</b> to proceed to security configuration.
   <br>
   <img src="images/populateTable2.png" alt="Employee Records Table">
   <br>


<b>Step 3: Role-Level Security (RLS) Configuration</b>

1. Read the explanation of Row-Level Security.
2. Toggle the <b>RLS is DISABLED</b> switch to <b>RLS is ENABLED</b>.
   <br>
   <img src="images/RLSenable1.png" alt="RLS Disabled">
   <br>
   <br>
   <img src="images/RLSenable2.png" alt="RLS Enabled">
   <br>
3. Assign required security policies to different organizational roles by clicking Assign for the required policy:
   - <b>HR Manager</b>: Assign the <b>Full Employee Access</b> policy.
   - <b>HR Assistant</b>: Assign the <b>Basic Information Access</b> policy.
   - <b>Sales Representative</b>: Assign the <b>Personal Record Access</b> policy.
     <br>
     <img src="images/RLSenable3.png" alt="Policy Assigned">
     <br>
   - <b>IT Staff</b>: Assign the <b>Department Based Access</b> (or <b>Basic Information Access</b>).
   - <b>Finance Analyst</b>: Assign the <b>Department Based Access</b> policy.
4. Click <b>Confirm Policies & Logout</b> at the bottom of the page.


<b>Step 4: End-User Login Simulation</b>

1. On the "User Login" screen, select a regular user from the dropdown menu to simulate their permissions (e.g., `bob - sales_rep (Sales)`).
2. Enter the sample user password: `user123`.
3. Click <b>Login as User</b>.

<br>
<img src="images/UserLogin.png" alt="User Login">
<br>


<b>Step 5: Testing Data Access Restrictions</b>

1. On the "Test Data Access" screen, observe the Employee Records table.
2. Note how the Active Security Policies have modified the viewport:
   - For example, if you logged in as a Sales Representative, you will notice that you can only see your own record (`Personal Record Access` policy).
   - If logged in as an HR Assistant, you will see all records, but the salary information will be masked (`Basic Information Access` policy).
   <br>
   <img src="images/UserLogin2.png" alt="Test Data Access View">
   <br>

3. Review the "Active Security Policies" section below the table to confirm which policy is currently enforced.
4. Click the <b>Logout</b> button at the top right to return to Step 4 and test accessibility with a different user role.
5. To restart the entire database setup, click <b>↺ Restart Experiment</b> at the bottom of the page.
