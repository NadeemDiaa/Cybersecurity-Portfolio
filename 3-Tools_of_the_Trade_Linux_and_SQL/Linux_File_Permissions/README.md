# Linux File Permissions Audit

This project demonstrates a real-world file permissions audit and correction process for a research team's directory structure. As a security professional, you examine existing file permissions, identify discrepancies with security policies, and modify permissions to enforce proper authorization levels.

## Scenario

You are a security professional at a large organization working primarily with their research team. Part of your job is to ensure users have appropriate file and directory permissions to maintain system security.

During a routine audit, you discover several permission settings that don't comply with organizational security policies:
- Some files are writable by unauthorized users
- An archived file has incorrect read/write permissions
- A directory has overly permissive access settings

To address these issues, you:
- Examine current permissions using Linux command-line tools
- Identify specific permission violations
- Modify permissions to comply with security policies
- Verify all changes were applied correctly

## Permission Analysis

### Initial Permission Assessment

The audit revealed several permission violations in the `projects` directory:
- Multiple files had world-writable permissions (-rw-rw-rw-)
- The archived file `.project_x.txt` had incorrect write permissions
- The `drafts` directory allowed group execute access when it should be restricted to owner only

## Security Implementation

### Permission Corrections Applied

The following corrective actions were taken using Linux permission modification commands:

1. Removed world-writable permissions from project_k.txt
2. Restricted group read access on project_m.txt
3. Corrected permissions on archived file .project_x.txt to make it read-only
4. Removed group execute permission on drafts directory to restrict access

These changes ensured compliance with organizational security policies:
- No files are writable by "other" users
- Archived files are read-only for authorized users
- Directory access is properly restricted to authorized personnel only

## Provided Resources

The following file documents the complete permission audit and correction process:
- **File Permissions in Linux** - [View PDF](./File_permissions_in_Linux.pdf)

## Deliverables

- **File Permissions Audit Report** - [View PDF](./File_permissions_in_Linux.pdf)

Includes analysis of existing permissions, identification of security violations, and documentation of corrective actions taken.

## Skills Demonstrated

- Linux file system security analysis
- Permission string interpretation
- Security policy implementation
- Command-line proficiency
- Attention to detail in access control

## Tools Used

- Linux Command Line - Directory navigation and permission analysis
- ls command - Examining file permissions and attributes
- chmod command - Modifying file and directory permissions

---

*This project demonstrates practical application of Linux file permission management in a security context.*