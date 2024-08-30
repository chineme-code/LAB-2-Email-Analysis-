# LAB-2-Email-Analysis- Planet's Prestige

# Description
Analyzed a suspicious email using various tools like Thunderbird, CyberChef, and ExifTool. Identified hidden file types, decoded Base64 content, and extracted metadata to uncover potential threats, emphasizing key skills in email forensics and cybersecurity analysis.

# Scenario

CoCanDa, a planet known as 'The Heaven of the Universe' has been having a bad year. A series of riots have taken place across the planet due to the frequent abduction of citizens, known as CoCanDians, by a mysterious force. CoCanDa’s Planetary President arranged a war-room with the best brains and military leaders to work on a solution. After the meeting concluded the President was informed his daughter had disappeared. CoCanDa agents spread across multiple planets were working day and night to locate her. Two days later and there’s no update on the situation, no demand for ransom, not even a single clue regarding the whereabouts of the missing people. On the third day a CoCanDa representative, an Army Major on Earth, received an email.


### Lessons Learned from the BTLO Planet Email Lab

In this lab, I explored various techniques and tools to analyze a suspicious email received by a CoCanDa representative. Below are the key takeaways:

1. **Email Analysis with Thunderbird**:
   - Used Thunderbird to open and read the `.eml` file.
   - Noticed an attachment that required deeper analysis.

2. **Determining File Type**:
   - Checked the hex of the file from the encoded part by opening it in a text editor like Mousepad.
   - Identified the content transfer encoding as Base64 and used [CyberChef](https://gchq.github.io/CyberChef/) to decode it.

3. **Hex Analysis for File Identification**:
   - Analyzed another content transfer encoding, which was a PDF file, by converting it to hex.
   - Used the first four hex numbers (file signature/magic number) to determine the file type.

4. **Using Gary Kessler’s File Signature Database**:
   - Cross-referenced the hex numbers on Gary Kessler’s file signature database, revealing that the PDF file was actually a `.zip` file.

5. **Extracting and Verifying Files**:
   - Saved the Base64 output as a `.zip` file and extracted its contents.
   - Checked for hidden files and verified file signatures using [HxD](https://mh-nexus.de/en/hxd/), a hex editor.

6. **Identifying File Types**:
   - Discovered that the extracted files were a JPEG, a PDF, and an MS XML file.

7. **Excel File Analysis with SQRLX**:
   - Used SQRLX to analyze an XLSX file, uncovering hidden data in the second sheet.
   - Cleared all formatting to reveal a Base64-encoded file, which was decoded using CyberChef.

8. **Metadata Analysis with ExifTool**:
   - Used [ExifTool](https://exiftool.org/) to read the metadata of documents in the `popcoando` folder.

### Tools Used in This Challenge:
- **Thunderbird**: For reading `.eml` files.
- **Mousepad**: A text editor for inspecting file content.
- **CyberChef**: To decode Base64 content.
- **HxD**: Hex editor for checking file signatures.
- **Gary Kessler’s File Signature Database**: For identifying file types.
- **SQRLX**: Tool for analyzing XLSX files.
- **ExifTool**: For metadata extraction.

### Final Thoughts:
This lab emphasized the importance of email analysis in cybersecurity, particularly for SOC analysts. Understanding file signatures, metadata, and using the right tools are crucial skills for investigating potential threats.

https://blueteamlabs.online/achievement/share/challenge/60157/10
