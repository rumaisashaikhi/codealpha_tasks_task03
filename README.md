# codealpha_tasks_task03
# Task3_SecureAudit
Author: Rumaisa Shaikh
Date: 27/10/2025

## Description
Secure code review and remediation of a simple Python login system. This project demonstrates detection of SQL injection and plaintext password issues and shows how to fix them.

## Files
- insecure_login.py    # Vulnerable version
- secure_login.py      # Fixed secure version (uses bcrypt, parameterized queries)
- users.db             # Sample SQLite database (created by secure script)
- bandit_report_before.txt
- bandit_report_after.txt
- screenshots/         # Put screenshots here (see names below)

## How to run
1. Install dependencies:
   `pip install bandit bcrypt`
2. Run Bandit (before fix):
   `bandit Task3_SecureAudit/insecure_login.py -f txt -o Task3_SecureAudit/bandit_report_before.txt`
3. Seed test user:
   `python -c "from Task3_SecureAudit.secure_login import create_user; create_user('testuser','Test@123')"`
4. Run secure login:
   `python Task3_SecureAudit/secure_login.py`
5. Run Bandit (after fix):
   `bandit -r Task3_SecureAudit -f txt -o Task3_SecureAudit/bandit_report_after.txt`

## Screenshots to include
- insecure_code_vscode.png
- bandit_report_before.png
- secure_code_vscode.png
- bandit_report_after.png
- db_seed.png
- login_success.png
- login_fail.png

## Notes
Keep `users.db` secure and do not commit real credentials. Use this demo only for learning.
