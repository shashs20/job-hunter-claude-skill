---
name: job-hunter
description: Searches for live job vacancies, verifies that they are still available, evaluates them against the candidate's profile and job-search criteria, and ranks the best opportunities by realistic likelihood of securing an interview. Use when the user asks to find jobs, search for vacancies, find roles to apply for, or identify suitable employment opportunities.
---

# Job Hunter

## Purpose

Find live job vacancies that are genuinely worth the candidate applying for.

The goal is not to find as many vaguely relevant jobs as possible.

The goal is to identify high-quality vacancies where the candidate has a realistic chance of receiving an interview, while also considering whether the role supports the candidate's longer-term career goals.

## Required Reference Files

Before performing a job search, read:

- `references/candidate-profile.md`
- `references/search-criteria.md`

Use the candidate profile to evaluate suitability.

Use the search criteria to determine which vacancies should and should not be recommended.

Do not assume experience or preferences that are not supported by these files or information provided by the user.

---

# Job Search Workflow

Follow this process whenever searching for jobs.

## Stage 1: Search

Search the live web for current vacancies matching the candidate's target roles and criteria.

Use multiple searches and job-title variations rather than relying on one search query.

Search broadly enough to discover related titles that may contain suitable responsibilities.

Prioritise:

1. Employer career pages
2. Reputable job boards
3. Recruitment platforms with accessible full job descriptions

Do not rely solely on search-result snippets.

---

## Stage 2: Initial Filter

Before performing a detailed analysis, remove vacancies that clearly violate the search criteria.

Immediately reject jobs that are:

- Closed or expired
- Apprenticeships
- Clearly too senior
- Primarily sales or cold calling
- Primarily call-centre work
- Traditional IT helpdesk roles
- Software development or coding-heavy roles
- Personal Assistant or Executive Assistant roles
- Primarily diary/calendar management
- Explicitly require a degree classification the candidate does not have

Do not spend significant analysis time on obvious rejects.

---

## Stage 3: Verify the Vacancy

For each potentially suitable vacancy, open the vacancy page and verify as much of the following as possible:

- Exact job title
- Employer
- Location
- Working arrangement
- Salary, if published
- Contract type
- Application deadline, if published
- Essential requirements
- Desirable requirements
- Main responsibilities
- Whether applications appear to still be open

Prefer information from the employer's official careers page when available.

Never claim a vacancy is live if this has not been verified.

If the vacancy status is uncertain, label it:

"Live status not fully verified"

---

## Stage 4: Requirement Analysis

Separate the vacancy requirements into:

### Essential requirements

Requirements that appear mandatory.

### Desirable requirements

Requirements that would strengthen an application but do not appear mandatory.

Then compare each important requirement with the candidate profile.

Classify each as:

- Strong Match
- Transferable Match
- Partial Match
- No Evidence
- Dealbreaker

A transferable match must have a clear explanation.

Do not convert unrelated experience into a match simply to improve the score.

---

## Stage 5: Interview Likelihood

Estimate how realistic the application is based on the candidate's actual profile.

Use the following scale:

### 9–10: Very Strong

The candidate meets almost all important requirements.

There are no major eligibility problems.

Existing professional or strongly transferable experience aligns well with the role.

This should be an application priority.

### 7–8: Realistic

The candidate meets most essential requirements.

Some gaps exist, but they are unlikely to automatically prevent an interview.

The candidate has credible transferable experience.

Recommend applying.

### 5–6: Stretch

The candidate has some relevant experience but meaningful gaps exist.

An interview is possible but should not be treated as likely.

Recommend only when the role offers particularly strong career value.

### 3–4: Weak

Important requirements are missing.

The candidate would probably be competing against substantially stronger applicants.

Normally do not recommend.

### 1–2: Very Weak

The candidate clearly lacks essential experience, qualifications or eligibility.

Do not recommend.

The score represents realistic competitiveness for an interview.

It is NOT simply a percentage of keywords matched.

---

## Stage 6: Career Value

Separately evaluate how useful the role would be for the candidate's longer-term Business Analyst direction.

Consider exposure to:

- Processes
- Systems
- Data
- Reporting
- Requirements
- Stakeholders
- Projects
- Documentation
- Process improvement
- Implementation
- Change
- KPIs
- Cross-functional work

Rate career value as:

- High
- Medium
- Low

Do not increase interview likelihood merely because career value is high.

Interview likelihood and career value are separate measurements.

---

## Stage 7: Recommendation

Classify each vacancy:

### APPLY

Use when the candidate has a realistic interview chance and the role satisfies the search criteria.

### STRETCH

Use when the role has worthwhile career value but the candidate has meaningful competitive gaps.

Use this category sparingly.

### SKIP

Use when the candidate is unlikely to be competitive, violates an exclusion, or has an important essential requirement missing.

Normally exclude SKIP vacancies from the final shortlist unless explaining why a particular vacancy was rejected would be useful.

---

# Final Output

Return the strongest vacancies first.

For each recommended vacancy provide:

## [Job Title] — [Employer]

**Location:**  
**Salary:**  
**Working arrangement:**  
**Interview likelihood:** X/10  
**Career value:** High / Medium / Low  
**Recommendation:** APPLY / STRETCH

**Why it fits:**
Briefly explain the strongest genuine matches.

**Main risk:**
State the biggest weakness or missing requirement honestly.

**Why it helps the candidate's career:**
Briefly explain the transferable value.

**Vacancy status:**
Confirmed open / Appears open / Status uncertain

**Source confidence:**
High / Medium / Low

**Application link:**
Provide the direct vacancy or application page when available.

---

# Final Ranking

After evaluating the vacancies, provide a final ranking:

| Rank | Vacancy | Interview Likelihood | Career Value | Recommendation |
|---|---|---:|---|---|

Rank primarily by realistic interview likelihood.

Use career value as a secondary factor.

Do not rank a highly desirable but unrealistic role above a strong realistic opportunity simply because it would be better for the candidate's long-term career.

---

# Quality Control

Before returning the results, check:

- Are the vacancies actually relevant?
- Have obvious exclusions been removed?
- Have live statuses been checked where possible?
- Did I distinguish professional experience from lab/project experience?
- Did I exaggerate any candidate experience?
- Are my interview scores genuinely differentiated?
- Would I actually advise this candidate to spend time applying for these jobs?
- Have I provided direct links where available?

If the answer to any of these is no, correct the results before responding.

# Hard Exclusion Enforcement

Hard exclusions are mandatory.

If a vacancy violates a hard exclusion in `search-criteria.md`, do not recommend it as APPLY or STRETCH.

Do not use labels such as:

- Borderline
- Your call
- Apply if willing to accept
- Consider anyway

Instead, reject the vacancy and continue searching for a replacement.

The final shortlist should contain vacancies that actually satisfy the candidate's criteria.

# Search Diversity

Do not stop searching after finding several vacancies from one website.

Search across multiple sources and employers.

Where possible, the final shortlist should not be dominated by a single job board.

Use job boards for discovery, but look for the employer's official careers page when possible.

Continue searching if the initial results are weak, repetitive, or concentrated on one source.

# Employment Preference

Prioritise permanent, full-time employment.

Use this preference order:

1. Permanent full-time
2. Long fixed-term full-time roles with strong career value
3. Short fixed-term full-time roles
4. Part-time roles

Part-time roles should normally not occupy a top recommendation position when suitable full-time vacancies are available.

A part-time vacancy may still be included when it is an unusually strong match, but clearly explain the trade-off.

# Recommendation Threshold

Aim to return 5 strong vacancies, not simply 5 vacancies.

If fewer than 5 suitable vacancies can be verified, return fewer than 5.

Never lower the candidate's standards merely to fill the requested number of results.

A result should normally require an interview likelihood of at least 7/10 to receive an APPLY recommendation.

Scores of 5-6 should normally be STRETCH.

Scores below 5 should normally be excluded from the final shortlist.

# Target Role Relevance

A vacancy must pass two tests:

1. Is the candidate realistically competitive?
2. Is this actually a sensible role for the candidate's stated career direction and preferences?

Do not recommend a job merely because transferable experience can be found.

Prioritise vacancies that fall within or are closely related to the target role families in `search-criteria.md`.

# Response Discipline

Do not end job-search results with generic offers to write a CV, cover letter, or application.

End with the ranked shortlist and the most important application priority or deadline.

# Vacancy Source Confidence

Evaluate the reliability of the vacancy source separately from candidate fit.

Use the following hierarchy.

## HIGH CONFIDENCE

Examples:

- Employer's official careers website
- Employer's official ATS/application page
- Official public-sector recruitment portal
- Official charity or organisation recruitment page

If an official page is accessible and still provides a functioning application route, the vacancy may normally be treated as live unless there is evidence that applications have closed.

## MEDIUM CONFIDENCE

Examples:

- Major established job board
- Recognised recruitment agency
- Job-board listing where the employer is clearly identified

Use these for discovery.

Where possible, search for the same vacancy on the employer's official website before recommending it.

## LOW CONFIDENCE

Examples:

- Employer is not identified
- Old agency advertisement with no closing date
- Aggregated or reposted vacancy
- Vacancy cannot be found anywhere except one third-party listing
- Application status cannot be established

Low-confidence vacancies should not normally outrank similarly suitable vacancies with high-confidence sources.

Clearly identify the uncertainty.

# Official Source Verification

When a promising vacancy is discovered on a job board:

1. Identify the employer.
2. Search for the employer's official careers website.
3. Search for the same job title there.
4. If found, use the official vacancy/application link in the final result.
5. If not found, retain the job-board link only when the vacancy still appears credible and current.

Do not spend excessive search time trying to locate an official page when none appears to exist.

# Search Coverage

Do not build the final shortlist primarily from one job board unless repeated searches genuinely fail to find suitable alternatives.

Search across combinations of:

- Employer career pages
- General job boards
- Specialist job boards
- Public-sector recruitment sites
- Charity/non-profit recruitment sites
- Recruitment agencies

Search multiple target role families rather than repeatedly searching one title.

At minimum, search across several of the candidate's priority role families before finalising the shortlist.

# Vacancy Freshness

Consider:

- Publication date
- Closing date
- Whether the application page functions
- Whether the employer still lists the vacancy
- Whether the advertisement appears stale
- Whether the same vacancy appears across current sources

Do not automatically assume that a vacancy without a published closing date is closed.

Likewise, do not automatically assume that an old third-party advertisement is still active.

Use the available evidence and state the confidence level.

# Source Confidence Output

For every final recommendation include:

**Source confidence:** High / Medium / Low

Prefer HIGH confidence vacancies when candidate fit is otherwise similar.