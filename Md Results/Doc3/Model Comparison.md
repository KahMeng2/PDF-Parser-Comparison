# Comparative LLM Assessment: Claude vs Gemini vs LlamaParse vs Mistral OCR

## Summary Assessments

### 🔵 Claude Performance

**Correctly Captured: 72/76 items (95%)**

- ✅ Patient Information: 8/8 fields
- ✅ Medical Admission: 10/10 fields
- ✅ ED to Ward Departure - Nursing: 19/19 fields
- ✅ ED to Ward Departure - Medical: 9/9 fields
- ⚠️ Authorization for Departure - Nursing: 5/9 fields (4 misplaced to Medical)
- ✅ Authorization for Departure - Medical: 4/4 fields
- ✅ Authorization for Discharge - Nursing: 8/8 fields
- ✅ Authorization for Discharge - Elderly: 4/4 fields
- ✅ Authorization for Discharge - Medical: 4/4 fields

**Misplaced Items (4):**

- Facility field (Patient Info instead of separate section)
- NUM/Senior ED Nurse authorization fields (Medical instead of Nursing section)

---

### 🟢 Gemini Performance

**Correctly Captured: 71/76 items (93%)**

- ⚠️ Patient Information: 7/8 fields (missing "Facility" as separate section)
- ✅ Medical Admission: 10/10 fields
- ✅ ED to Ward Departure - Nursing: 19/19 fields
- ✅ ED to Ward Departure - Medical: 9/9 fields
- ⚠️ Authorization for Departure - Nursing: 3/9 fields (6 misplaced to Medical)
- ✅ Authorization for Departure - Medical: 4/4 fields
- ✅ Authorization for Discharge - Nursing: 8/8 fields
- ✅ Authorization for Discharge - Elderly: 4/4 fields
- ✅ Authorization for Discharge - Medical: 4/4 fields

**Misplaced Items (5):**

- Facility field (embedded in header, not as separate section)
- NUM/Senior ED Nurse authorization fields (Medical instead of Nursing)
- "Alterations to calling criteria" and "Altered frequency" fields (Medical instead of Nursing)

---

### 🟡 LlamaParse Performance

**Correctly Captured: 65/76 items (86%)**

- ⚠️ Patient Information: 7/8 fields (missing separate Facility section)
- ✅ Medical Admission: 10/10 fields
- ✅ ED to Ward Departure - Nursing: 19/19 fields
- ✅ ED to Ward Departure - Medical: 9/9 fields
- ✅ Authorization for Departure - Nursing: 9/9 fields
- ✅ Authorization for Departure - Medical: 4/4 fields
- ✅ Authorization for Discharge - Nursing: 5/8 fields
- ⚠️ Authorization for Discharge - Elderly: 4/4 fields (positioned as column header)
- ✅ Authorization for Discharge - Medical: 4/4 fields

**Key Issues:**

- Converted to HTML table format instead of markdown sections
- Some structural organization lost in table conversion
- Authorization sections merged into table cells rather than distinct sections

---

### 🔴 Mistral OCR Performance

**Correctly Captured: ~5/76 items (7%)**

- ❌ Critical Failure: Document converted to embedded image
- ❌ No structured text extraction
- ❌ No field recognition
- ❌ No sectional organization
- ❌ Only header text "Attachment 1: Adult ED Observation Chart..." extracted
- ❌ Large unreadable table structure

**Complete Assessment Impossible:** Document rendered as image with minimal text extraction.

---

### 🟡 ChatGPT Performance

**Correctly Captured: 75/76 items (99%)**

- ⚠️ Patient Information: 7/8 fields (Facility merged into demographics, not separate section)
- ✅ Medical Admission: 10/10 fields
- ✅ ED to Ward Departure - Nursing: 19/19 fields
- ✅ ED to Ward Departure - Medical: 9/9 fields
- ✅ Authorization for Departure - Nursing: 9/9 fields
- ✅ Authorization for Departure - Medical: 4/4 fields
- ✅ Authorization for Discharge - Nursing: 8/8 fields
- ✅ Authorization for Discharge - Elderly: 4/4 fields
- ✅ Authorization for Discharge - Medical: 4/4 fields

**Misplaced Items (1):**

- Facility field (integrated into "Patient & Demographics" instead of separate "Facility Information" section)

**Key Strengths:**

- Excellent content capture rate
- Clean markdown formatting
- Proper field structure and organization
- Complete functional content preserved

---

## Overall Rankings

| Rank | Model           | Accuracy | Key Strengths                                       | Key Weaknesses                          |
| ---- | --------------- | -------- | --------------------------------------------------- | --------------------------------------- |
| 1st  | **ChatGPT**     | 99%      | Highest content capture, clean formatting           | Minor section naming variation          |
| 2nd  | **Claude**      | 95%      | Good sectional organization, complete field capture | Authorization field misplacement        |
| 3rd  | **Gemini**      | 93%      | Good field capture, readable format                 | Authorization field misplacement issues |
| 4th  | **LlamaParse**  | 86%      | Maintained tabular relationships                    | Lost markdown sectional structure       |
| 5th  | **Mistral OCR** | 7%       | Failed extraction but recognizable attempt          | Failed to extract structured content    |

## Key Findings

**Best for Structure:** Claude maintained the closest resemblance to original document hierarchy

**Best for Content:** Claude and Gemini both captured nearly all factual content

**Most Problematic Area:** Authorization sections - both Claude and Gemini struggled with nursing vs medical field placement

**Critical Missing Content:** None - top three models captured functional content effectively

**Most Severe Failure:** Mistral OCR failed by embedding document as image

**Key Finding:** ChatGPT achieved the highest accuracy (99%) with only one structural misplacement

**Recommendation:** ChatGPT for highest content fidelity, Claude for best structural organization. Both significantly outperform other options. Avoid Mistral OCR for document conversion tasks.
