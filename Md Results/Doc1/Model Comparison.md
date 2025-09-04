# Comparative LLM Assessment: PDF-to-Markdown Medical Document Conversion

## Summary Assessments

### 🔵 Claude Performance

**Content Accuracy: 100% (Perfect Match)**

**Correctly Captured:**

- ✅ Header Information: All 5 fields (Provider, Patient, Provider's Pt ID, Sex, Attachment Control Number)
- ✅ Hospital Discharge DX: 2/2 diagnoses with correct ICD codes
- ✅ Hospital Discharge Procedures: 1/1 procedure with correct CPT code
- ✅ All Clinical Sections: Complete text preservation across all 6 major sections
- ✅ Signature Block: Physician name and timestamp

---

### 🟢 Gemini Performance

**Content Accuracy: 100% (Perfect Match)**

**Correctly Captured:**

- ✅ Header Information: All 5 fields with identical inline formatting
- ✅ Hospital Discharge DX: 2/2 diagnoses with correct ICD codes
- ✅ Hospital Discharge Procedures: 1/1 procedure with correct CPT code
- ✅ All Clinical Sections: Complete text preservation across all 6 major sections
- ✅ Signature Block: Physician name and timestamp

**Perfect content match to ground truth.**

---

### 🟡 LlamaParse Performance

**Content Accuracy: 100% (Perfect Match)**

**Correctly Captured:**

- ✅ Header Information: All 5 fields present
- ✅ Hospital Discharge DX: 2/2 diagnoses with correct ICD codes
- ✅ Hospital Discharge Procedures: 1/1 procedure with correct CPT code
- ✅ All Clinical Sections: Complete text preservation across all 6 major sections
- ✅ Signature Block: Physician name and timestamp

---

### 🟠 Mistral OCR Performance

**Content Accuracy: 100% (Perfect Match)**

**Correctly Captured:**

- ✅ Header Information: All 5 fields present
- ✅ Hospital Discharge DX: 2/2 diagnoses with correct ICD codes
- ✅ Hospital Discharge Procedures: 1/1 procedure with correct CPT code
- ✅ All Clinical Sections: Complete text preservation across all 6 major sections
- ✅ Signature Block: Physician name and timestamp

---

### 🔴 ChatGPT Performance

**Content Accuracy: 85% (Significant Modifications)**

**Correctly Captured:**

- ✅ Header Information: All 5 fields present
- ⚠️ Hospital Discharge DX: 2/2 diagnoses but section title modified
- ⚠️ Hospital Discharge Procedures: 1/1 procedure but added "CPT" prefix and em-dash formatting
- ❌ Clinical Content: Extensively paraphrased and restructured throughout
- ⚠️ Signature Block: Present but reformatted with separate Date/Time field

**Major Content Modifications:**

- **Paraphrasing**: Extensive rewording of medical narrative (e.g., "originally diagnosed in the early 70's" → "originally diagnosed in the early 1970s")
- **Section Restructuring**: Changed "HOSPITAL DISCHARGE PHYSICAL FINDINGS" to "Physical Examination on Admission"
- **Content Reorganization**: Bullet-pointed physical exam vs. paragraph format
- **Added Information**: Included "CPT" prefix and procedure formatting not in original
- **Text Alterations**: Changed "TALC slurry" to "talc slurry", "Dr. Follow" formatting
- **Prognosis Addition**: Added separate "Prognosis" section not present in ground truth

---

## Detailed Content Analysis

### Header Information Accuracy

| Model            | Provider     | Patient          | Provider's Pt ID | Sex    | Attachment Control Number |
| ---------------- | ------------ | ---------------- | ---------------- | ------ | ------------------------- |
| **Ground Truth** | Ken Cure, MD | Patient H Sample | 6910828          | Female | XA728302                  |
| **Claude**       | ✅           | ✅               | ✅               | ✅     | ✅                        |
| **Gemini**       | ✅           | ✅               | ✅               | ✅     | ✅                        |
| **LlamaParse**   | ✅           | ✅               | ✅               | ✅     | ✅                        |
| **Mistral OCR**  | ✅           | ✅               | ✅               | ✅     | ✅                        |
| **ChatGPT**      | ✅           | ✅               | ✅               | ✅     | ✅                        |

### Clinical Content Preservation

**Models with 100% content accuracy:**

- Claude, Gemini, LlamaParse, Mistral OCR achieved perfect preservation for:
  - ICD diagnosis codes (174.8, 163.8)
  - CPT procedure code (32650)
  - Complete medical history narrative
  - Physical examination findings
  - Hospital course details
  - Discharge instructions and follow-up plans
  - Physician signature and date

**ChatGPT Content Modifications:**

- ❌ Extensive paraphrasing of clinical narrative
- ❌ Section title changes ("HOSPITAL DISCHARGE DX" → "Hospital Discharge Diagnoses")
- ❌ Format alterations (paragraph to bullet points in physical exam)
- ❌ Added interpretive elements not in original
- ❌ Character encoding issues with apostrophes and punctuation

### Critical Medical Information Accuracy

**Perfect preservation (Claude, Gemini, LlamaParse, Mistral OCR):**

- Patient demographics and identifiers
- Diagnosis codes and descriptions
- Procedure codes and descriptions
- Medication names (Tamoxifen, Megace, Arimidex, Tylenol with Codeine)
- Laboratory values (CA15-3: 44 → 600)
- Anatomical references and medical terminology
- Timeline information (early 70's, mid 70's, late 80's, mid 90's)
- Follow-up instructions (Dr. Follow, 3 weeks, chest x-ray)

**ChatGPT Medical Information Handling:**

- ✅ All critical medical codes and values preserved
- ⚠️ Medication names preserved but context altered
- ⚠️ Timeline information modernized ("70's" → "1970s")
- ❌ Clinical narrative extensively paraphrased
- ❌ Added clinical interpretations not in original document

---

## Overall Rankings

| Rank | Model           | Content Accuracy | Key Strengths                                    | Key Weaknesses         |
| ---- | --------------- | ---------------- | ------------------------------------------------ | ---------------------- |
| 1st  | **Claude**      | 100%             | Perfect content preservation, complete structure | None identified        |
| 1st  | **Gemini**      | 100%             | Perfect content preservation, complete structure | None identified        |
| 1st  | **LlamaParse**  | 100%             | Perfect content preservation, complete structure | None identified        |
| 1st  | **Mistral OCR** | 100%             | Perfect content preservation, complete structure | None identified        |
| 5th  | **ChatGPT**     | 85%              | Preserved critical medical codes                 | Extensive paraphrasing |

## Key Findings

**Perfect Content Preservation:** Claude, Gemini, LlamaParse, and Mistral OCR all achieved 100% content accuracy with no medical information lost or altered

**Most Problematic for Medical Documents:** ChatGPT extensively paraphrased and restructured content, making it unsuitable for exact document conversion tasks

**Critical Distinction:** While ChatGPT preserved essential medical codes and data, its interpretive approach altered the clinical narrative significantly

**Medical Document Reliability:** Four models demonstrated perfect reliability for medical document conversion, while ChatGPT's paraphrasing approach poses risks for clinical documentation

**Content vs. Interpretation Trade-off:** ChatGPT's approach may be beneficial for summarization but problematic for exact document conversion where fidelity is critical

## Recommendations

**For Exact Medical Document Conversion:** Claude, Gemini, LlamaParse, or Mistral OCR all provide perfect content accuracy

**For Content-Critical Applications:** Claude, Gemini, LlamaParse, or Mistral OCR recommended as all preserved 100% of medical content

**⚠️ Avoid ChatGPT for Document Conversion:** ChatGPT's interpretive approach makes it unsuitable for exact document conversion where fidelity is required

**For Medical Summarization vs. Conversion:** ChatGPT might be suitable for creating summaries but not for preserving original document content

**General Assessment:** This analysis reveals a clear distinction between models designed for exact conversion (Claude, Gemini, LlamaParse, Mistral OCR) versus those optimized for interpretation and paraphrasing (ChatGPT). For medical document conversion, content fidelity is paramount, making the first group strongly preferable.
