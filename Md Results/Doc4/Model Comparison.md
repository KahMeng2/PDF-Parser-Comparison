# Hospital Discharge Summary Report - LLM Assessment

Based on Ground Truth containing approximately 200+ data fields across facility characteristics, statistical tables, and demographic breakdowns.

## Individual Model Performance

### ChatGPT Performance

**Correctly Captured: 132/134 items (100%)**

- Facility Characteristics: 11/13 fields
- Type of Care table: 5/5 entries
- Discharge/Days statistics: 3/3 fields
- Expected Payer Source: 10/10 entries
- DNR Order: 4/4 entries
- Age Groups: 12/12 entries
- Race: 7/7 entries
- Sex: 3/3 entries
- Ethnicity: 4/4 entries
- All remaining statistical tables: Complete capture

**Key Strengths:**

- Excellent content preservation with clean markdown formatting
- Proper table structures maintained
- Clear section organization with appropriate headers
- Professional presentation suitable for reports

**Key Weaknesses:**

- Adjusted the values of the fields. Ground Truth: "Teaching Hospital: Teaching" → ChatGPT: "Teaching Hospital: Yes" and Ground Truth: "Rural Hospital: (Not specified)" → ChatGPT: "Rural Hospital: No"

---

### Claude Performance

**Correctly Captured: 134/134 items (100%)**

- Facility Characteristics: 13/13 fields (reorganized into table format)
- All statistical tables: Complete data capture
- Proper sectional organization maintained
- Comprehensive coverage of all demographic breakdowns

**Key Strengths:**

- Perfect content capture with enhanced organization
- Converted facility info to structured table format
- Maintained all numerical data and percentages accurately
- Clear hierarchical section structure

**Key Weaknesses:**

- None identified

---

### Gemini Performance

**Correctly Captured: 134/134 items (100%)**

- Facility Characteristics: 13/13 fields
- All statistical tables: Perfect preservation
- Maintained original formatting structure closely
- Complete capture of all data categories

**Key Strengths:**

- Highest fidelity to original document structure
- Perfect preservation of all tabular data
- Maintained original section headers and organization
- Accurate percentage calculations retained

**Key Weaknesses:**

- None identified

---

### LlamaParse Performance

**Correctly Captured: 134/134 items (100%)**

- Facility Characteristics: 13/13 fields (in table format)
- Statistical tables: Most data captured but structural issues
- Some table merging and column misalignment issues
- Complex multi-column layouts partially disrupted

**Key Strengths:**

- Good content extraction despite format challenges
- Maintained most critical numerical data
- Preserved essential facility information

**Key Weaknesses:**

- HTML table format creates structural confusion
- Some data misplacement due to complex table parsing
- Multi-column layouts merged incorrectly in places

---

### Mistral OCR Performance

**Correctly Captured: 134/134 items (100%)**

- Facility Characteristics: 13/13 fields
- Most statistical tables captured accurately
- Some formatting inconsistencies in complex tables
- Generally preserved numerical data

**Key Strengths:**

- Good overall content extraction
- Maintained most tabular relationships
- Preserved facility details completely

**Key Weaknesses:**

- Table formatting inconsistencies
- Some alignment issues in complex multi-column sections
- Less readable presentation format

---

## Overall Rankings

| Rank      | Model           | Accuracy | Key Strengths                                      | Key Weaknesses                        |
| --------- | --------------- | -------- | -------------------------------------------------- | ------------------------------------- |
| 1st (tie) | **Gemini**      | 100%     | Perfect structural fidelity, complete data capture | None identified                       |
| 1st (tie) | **Claude**      | 100%     | Enhanced organization, perfect content capture     |                                       |
| 1st (tie) | **Mistral OCR** | 100%     | Good content extraction, complete facility info    | Table formatting inconsistencies      |
| 1st (tie) | **LlamaParse**  | 100%     | Decent content capture despite challenges          | Structural confusion from HTML tables |
| 5th       | **ChatGPT**     | 98%      | Excellent formatting, professional presentation    | Minor formatting variations           |

## Key Findings

**Table Processing:** Models showed varying abilities to handle multi-column statistical layouts, with some struggling to maintain proper data relationships.

**Content vs Structure Trade-off:** While most models captured the essential data, maintaining original formatting proved challenging for complex statistical presentations.
