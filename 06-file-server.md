# File Server and Shared Folder

The File Server role was installed on DC001. A folder was created at `C:\Shares\StaffShare` and shared through Server Manager under File and Storage Services.

| Setting | Configuration |
|---|---|
| Share name | `StaffShare` |
| Network path | `\\192.168.56.10\StaffShare` |
| Share permission | Domain Users — Full Control (lab configuration) |
| NTFS permission | Domain Users — Modify |

Share permissions and NTFS permissions both affect effective network access. This lab uses broad share permissions and more limited NTFS permissions for practice. Review permissions carefully before using a similar configuration in production.

## Accessing the share from PC001

Enter this UNC path in File Explorer's address bar or the Run dialog, not in the search box:

```text
\\192.168.56.10\StaffShare
```

## Verification

A test file named `lwandle-test.txt` was created from PC001 inside the shared folder. The file was then visible on DC001 at `C:\Shares\StaffShare\lwandle-test.txt`.
