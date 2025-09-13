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

## Agents for Resume Update Flow

## Input & Parsing Agent

Accepts user’s resume (PDF/Word/Text).

Parses it into structured data (sections, experience, skills).

Cleans formatting & extracts metadata.

## Job Description Analyzer Agent

Takes the job description (JD).

Extracts required skills, tools, keywords, and responsibilities.

Identifies role-specific priorities.

## Gap Analysis Agent

Compares resume data vs. JD requirements.

Identifies missing keywords/skills.

Suggests areas to highlight or update.

## Resume Drafting Agent

Generates updated resume draft tailored to JD.

Rewrites sections (Summary, Experience, Skills) using AI.

Ensures ATS (Applicant Tracking System) compatibility.

## Optimization Agent

Improves readability and formatting.

Suggests action verbs, quantifiable achievements.

Ensures clarity, grammar, and structure.

## Feedback & Revision Agent

Interacts with user for approval/rejection of changes.

Applies revisions iteratively.

Supports “shorter version” or “highlight AWS experience” kind of requests.

## Export Agent

Converts final draft into chosen format (PDF, Word, Markdown).

Ensures consistent formatting and professional look.

Provides downloadable file.
---

## Future Enhancements
- Auto-commit changes in a dedicated Git branch.  
- Integration with GitHub Actions for CI/CD of resume updates.  
- Add version tagging (`resume_v1.0_JD123`).  
