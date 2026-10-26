# Job Hunter — Claude Skill

A custom Claude Skill designed to find, verify and rank live job vacancies based on a candidate's actual experience, preferences and career goals.

## The Problem

Job searches often return vacancies that look relevant based on the job title but are not realistic applications.

Common problems include:

- Roles requiring more experience than the candidate has
- Expired or stale vacancies
- Unsuitable roles appearing because of broad search terms
- Job titles that sound relevant but contain unsuitable responsibilities
- Spending time applying for jobs where the candidate is unlikely to be competitive

Job Hunter aims to reduce this noise and identify vacancies that are genuinely worth applying for.

## The Solution

Job Hunter gives Claude a repeatable process for conducting a candidate-specific job search.

The Skill instructs Claude to:

1. Search across multiple relevant job families
2. Remove vacancies that violate the candidate's criteria
3. Open and inspect promising vacancies
4. Check whether the vacancy appears to still be accepting applications
5. Separate essential and desirable requirements
6. Compare the requirements against the candidate's actual experience
7. Estimate realistic interview competitiveness
8. Separately evaluate long-term career value
9. Assess the reliability of the vacancy source
10. Rank the strongest opportunities

Vacancies are classified as:

- APPLY
- STRETCH
- SKIP

## Project Structure

    job-hunter/
    ├── README.md
    ├── SKILL.md
    └── references/
        ├── candidate-profile.example.md
        └── search-criteria.example.md

### SKILL.md

Contains the main workflow and decision rules Claude follows when conducting a job search.

### candidate-profile.example.md

Contains factual information about the candidate, including education, professional experience, projects and skills.

### search-criteria.example.md

Contains the candidate's target roles, career direction, location preferences, exclusions and application priorities.

## How It Works

The Skill follows this workflow:

    Job Search Request
            ↓
    Load Candidate Profile
            ↓
    Load Search Criteria
            ↓
    Search Live Vacancies
            ↓
    Apply Hard Filters
            ↓
    Verify Vacancy
            ↓
    Assess Source Confidence
            ↓
    Analyse Requirements
            ↓
    Compare Candidate Fit
            ↓
    Interview Competitiveness + Career Value
            ↓
    APPLY / STRETCH / SKIP
            ↓
    Rank Final Shortlist

## Scoring Approach

Interview likelihood is used as a relative decision score rather than a statistical probability.

For example, 7/10 means the vacancy is considered a realistic application based on the available evidence. It does not mean the candidate has a 70% probability of receiving an interview.

Career value is assessed separately from interview competitiveness.

This prevents an attractive but unrealistic role from being ranked above a more achievable opportunity simply because it better matches the candidate's long-term career goal.

## Vacancy Verification

The Skill evaluates the reliability of vacancy information.

Source confidence is classified as:

- **High** — official employer careers pages and official application systems
- **Medium** — established job boards and recruitment agencies
- **Low** — unverified, anonymous, stale or aggregated listings

Where possible, vacancies discovered through third-party job boards are checked against official employer sources.

## Development and Testing

The Skill was developed iteratively using repeated live job-search tests.

### Version 1

The first version successfully searched and evaluated vacancies but exposed two problems:

- Hard exclusions were not always enforced
- Results became concentrated on one job board

### Version 2

The workflow was updated to strengthen exclusion rules and encourage broader searching.

Testing improved the filtering behaviour but revealed that vacancies from different sources were being treated as equally reliable.

### Version 3

Source-confidence rules and official-source verification were added.

This allowed the Skill to distinguish between employer career pages, established job boards and less-verifiable third-party listings.

## Design Decisions

### Separate Candidate Data From Workflow Logic

Candidate information is stored separately from the main Skill instructions.

This makes the workflow easier to maintain and means the Skill could be adapted to another candidate by replacing the reference files.

### Separate Interview Fit From Career Value

A vacancy can be excellent for someone's long-term career while still being an unrealistic immediate application.

The Skill therefore evaluates these independently.

### Quality Over Quantity

The Skill is instructed not to lower its standards simply to return a requested number of vacancies.

Five strong opportunities are preferable to twenty weak matches.

## Limitations

- Interview-likelihood scores are judgement-based rankings, not statistical probabilities
- Vacancy information may change after a search
- Some websites may prevent Claude from accessing full vacancy information
- Third-party listings can become stale
- AI judgement can still be inconsistent
- Important applications should still be reviewed by the user

## Future Improvements

Possible future versions could include:

- Tracking previously submitted applications
- Automatic duplicate detection
- Application deadline tracking
- CV-tailoring recommendations
- Tracking which types of applications lead to interviews

## Example

User:

> Find me 5 jobs to apply for today.

Job Hunter searches for live vacancies, evaluates them against the candidate profile and search criteria, and returns a ranked shortlist with the reasoning behind each recommendation.