# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
<img width="821" height="377" alt="441038731-bcca4ee9-42f3-490e-ab65-e160c8ac0794" src="https://github.com/user-attachments/assets/a72a6930-cc5c-48c9-9af9-4a86ca92f4f5" />
<img width="997" height="155" alt="441038741-f4a36b69-b9ea-4319-b828-ae2123b19d6f" src="https://github.com/user-attachments/assets/ef803e2c-2f6f-4d64-b55e-4504f279f722" />
<img width="827" height="302" alt="441038749-6fedf058-d672-4bbd-ac2c-5899800cc897" src="https://github.com/user-attachments/assets/c4a17f80-6a9d-4724-9fec-3f19fb851f3b" />
<img width="1016" height="215" alt="441038772-e266a1e1-d4fe-4209-bf15-71ec359aac89" src="https://github.com/user-attachments/assets/88f9f964-bdee-44e3-96b7-c93903d31b7d" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
