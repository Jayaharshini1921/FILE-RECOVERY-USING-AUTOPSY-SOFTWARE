# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1016" height="548" alt="Screenshot 2025-09-10 032958" src="https://github.com/user-attachments/assets/cd333fb6-da3b-40b3-84f2-ce44f1475e32" />


<img width="989" height="621" alt="Screenshot 2025-09-10 033037" src="https://github.com/user-attachments/assets/3ebcbdf3-6e2d-471c-bff0-d94fdb308f52" />



<img width="604" height="321" alt="Screenshot 2025-09-10 035930" src="https://github.com/user-attachments/assets/51228dde-dd8b-47b1-9c90-8e05e8aced33" />


<img width="1642" height="1102" alt="Screenshot 2025-09-10 040757" src="https://github.com/user-attachments/assets/a503aeab-6fa5-4e46-a411-ff99c6957811" />


<img width="1592" height="1009" alt="Screenshot 2025-09-10 040828" src="https://github.com/user-attachments/assets/4f923cc2-ddb4-4bcd-967a-88f1d73dd8a9" />





## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
