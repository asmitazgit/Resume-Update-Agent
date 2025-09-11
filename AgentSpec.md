## Workflow

1. **User Action**  
   - Uploads resume (PDF/Docx).  
   - Provides target Job Description (JD).  

2. **System Action**  
   - Extracts key skills, responsibilities, and keywords from JD.  
   - Maps JD requirements against existing resume.  
   - Suggests edits:  
     - Highlight matching skills.  
     - Add missing but relevant keywords.  
     - Adjust summary/profile statement.  
     - Align experience bullets with JD.  

3. **User Action**  
   - Reviews system-suggested resume.  
   - Accepts or modifies changes.  

4. **System Action**  
   - Generates final tailored resume.  
   - Saves to `/output/resume_{job_role}.docx`.  
   - Commits update to Git repo (if automation enabled).  

---

## Example Use Case
- **Input**: JD for AWS Cloud Architect.  
- **System Output**: Updated resume emphasizing AWS, EC2, RDS, CloudFormation, Route53.  
- **File Saved**: `/output/resume_AWS_Cloud_Architect.docx`.  

---

## Future Enhancements
- Auto-commit changes in a dedicated Git branch.  
- Integration with GitHub Actions for CI/CD of resume updates.  
- Add version tagging (`resume_v1.0_JD123`).  
