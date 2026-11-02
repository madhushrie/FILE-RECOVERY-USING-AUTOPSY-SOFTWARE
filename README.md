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
<img width="962" height="562" alt="Screenshot 2026-11-02 110013" src="https://github.com/user-attachments/assets/44e4caaa-b391-4400-8dd9-c7459cbcd454" />
<img width="958" height="562" alt="Screenshot 2026-11-02 110027" src="https://github.com/user-attachments/assets/877615fe-d9d9-4822-aeec-434e30d438f8" />

<img width="888" height="728" alt="Screenshot 2026-11-02 110049" src="https://github.com/user-attachments/assets/1ebd242c-57c8-4b13-a7a6-9e79d0814ea7" />
<img width="1075" height="641" alt="Screenshot 2026-11-02 110119" src="https://github.com/user-attachments/assets/e3977701-6e13-4d16-8015-512684a719b0" />
<img width="1104" height="1001" alt="Screenshot 2026-11-02 110615" src="https://github.com/user-attachments/assets/96db554a-3a14-4914-aae5-71a4992ec704" />
<img width="1102" height="1006" alt="Screenshot 2026-11-02 110806" src="https://github.com/user-attachments/assets/1b64f47c-901e-41a4-8acf-14a4da204072" />
<img width="832" height="523" alt="Screenshot 2026-11-02 110927" src="https://github.com/user-attachments/assets/6fffb20c-5011-4084-b3b1-d2acf851372c" />
<img width="799" height="911" alt="Screenshot 2026-11-02 110947" src="https://github.com/user-attachments/assets/5521561e-294c-44eb-a2d5-b59dadde9262" />
<img width="1682" height="1022" alt="Screenshot 2026-11-02 111048" src="https://github.com/user-attachments/assets/1514e817-a843-4afa-8682-2dc4d7f6ed7c" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
