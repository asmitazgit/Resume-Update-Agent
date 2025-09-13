# GOAL
# User–System Interaction: Resume Update Agent

## Actors
- **User**: Provides Job Description (JD) and existing Resume.
- **System (Agent)**: AI-powered service that tailors resume to JD.
- 
## Precondition

User has an existing resume.

User has a target job description (JD).

Main Interaction Flow

User → System: Uploads existing resume (PDF/Word/Text).

User → System: Provides job description (JD) of target role.

System → User: Acknowledges input and extracts keywords, skills, and role requirements from JD.

System → User: Shows key gaps (skills/keywords missing from resume).

User → System: Confirms which skills/achievements should be highlighted or added.

System → User: Generates an updated draft of the resume tailored to the JD.

System → User: Suggests optimized sections (Summary, Skills, Experience, Projects).

User → System: Reviews draft and provides feedback (e.g., “Make it shorter,” “Emphasize AWS experience”).

System → User: Updates the resume accordingly.

System → User: Provides final downloadable version in chosen format (PDF/Word).

Alternative Flows

Missing Resume: If user doesn’t have an existing resume, the system offers to generate a fresh one using profile details.

Multiple JDs: If user uploads multiple JDs, the system can create tailored resumes for each.
