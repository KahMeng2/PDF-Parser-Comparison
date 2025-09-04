# Comprehensive LLM Performance Analysis: PDF-to-Markdown Medical Document Conversion

## Executive Summary

Based on analysis of 5 different medical document types, this comprehensive assessment reveals significant performance differences between large language models for medical document conversion tasks. The evaluation covered diverse document structures including ED observation charts, discharge summaries, hospital reports, clinical assessments, and psychiatric evaluations.

## Overall Model Rankings

| Rank | Model           | Average Accuracy | Best Performance | Consistency | Key Characteristics                              |
| ---- | --------------- | ---------------- | ---------------- | ----------- | ------------------------------------------------ |
| 1st  | **Claude**      | 99%              | 100% (4/5 docs)  | Excellent   | Perfect content fidelity with superior structure |
| 2nd  | **Gemini**      | 98.6%            | 100% (4/5 docs)  | Excellent   | Reliable accuracy with clean formatting          |
| 3rd  | **LlamaParse**  | 96.2%            | 100% (3/5 docs)  | Good        | Strong content capture, variable formatting      |
| 4th  | **Mistral OCR** | 79.8%            | 100% (3/5 docs)  | Variable    | Inconsistent performance across document types   |
| 5th  | **ChatGPT**     | 90.4%            | 100% (2/5 docs)  | Poor        | High accuracy but problematic modifications      |

## Performance by Document Type

### Simple Medical Documents (Discharge Summaries)

**Universal Excellence**: All models achieved 100% accuracy on well-structured, standardized medical summaries, indicating these document types are easily processed by modern LLMs.

### Complex Multi-Section Documents (ED Charts, Hospital Reports)

**Clear Differentiation**: Performance varied significantly:

- **Claude & Gemini**: Consistently high accuracy (95%+) with proper section management
- **LlamaParse**: Good content capture but structural challenges
- **Mistral OCR**: Highly variable (7%-100%) depending on document complexity
- **ChatGPT**: Strong content capture but concerning modifications

### Specialized Clinical Documents (Psychiatric Evaluations)

**Fidelity Requirements**: Documents requiring exact clinical language preservation:

- **Claude**: Perfect preservation (100%)
- **Gemini**: Near-perfect with minor formatting variations (98%)
- **ChatGPT**: Significant paraphrasing issues (70%)

## Critical Model Characteristics

### 🏆 Claude: The Gold Standard

**Strengths:**

- Highest overall consistency across all document types
- Perfect content fidelity in 4 out of 5 assessments
- Superior structural organization and markdown formatting
- Reliable preservation of medical terminology and codes
- Excellent handling of complex multi-section documents

**Best Use Cases:** Any medical document conversion requiring exact fidelity

### 🥈 Gemini: Reliable Performer

**Strengths:**

- Consistent high accuracy across all document types
- Clean, professional formatting
- Strong content preservation with minimal modifications
- Good handling of complex table structures

**Best Use Cases:** General medical document conversion with emphasis on readability

### 🥉 LlamaParse: Content-Focused

**Strengths:**

- Excellent content extraction capabilities
- Reliable preservation of critical medical information
- Handles complex documents well despite formatting issues

**Weaknesses:**

- Inconsistent structural formatting
- Table conversion challenges
- HTML formatting creates usability issues

**Best Use Cases:** When content accuracy is prioritized over formatting

### ⚠️ Mistral OCR: Highly Variable

**Strengths:**

- Can achieve perfect accuracy on simple documents
- Good content extraction when functioning properly

**Critical Weaknesses:**

- Extreme variability (7%-100% accuracy range)
- Complete failures on complex documents
- Unreliable performance makes it unsuitable for critical applications

**Best Use Cases:** Limited; backup option only for simple documents

### 🚫 ChatGPT: The Modifier

**Strengths:**

- Can achieve high content capture rates
- Professional presentation when successful

**Critical Weaknesses:**

- **Systematic paraphrasing**: Extensively modifies clinical language
- **Content interpretation**: Adds interpretive elements not in originals
- **Inconsistent accuracy**: Varies from 70%-100% across document types
- **Character encoding issues**: Persistent technical problems
- **Medical risk**: Alterations could impact clinical accuracy

**Best Use Cases:** Document summarization (NOT exact conversion)

## Key Clinical Considerations

### Medical Document Integrity

**Critical Finding**: Only Claude and Gemini consistently preserved exact clinical language, medication dosages, diagnostic codes, and assessment terminology without modification.

### Legal and Regulatory Compliance

**High-Risk Models**: ChatGPT's systematic paraphrasing and Mistral OCR's unreliability pose risks for documents requiring legal accuracy or regulatory compliance.

### Content vs. Interpretation Trade-off

**Clear Distinction**: Models fall into two categories:

- **Exact Conversion** (Claude, Gemini, LlamaParse): Preserve original content precisely
- **Interpretive Processing** (ChatGPT): Paraphrase and restructure content

## Recommendations by Use Case

### For Exact Medical Document Conversion

**Recommended**: Claude (first choice) or Gemini (excellent alternative)
**Acceptable**: LlamaParse (with format post-processing)
**Avoid**: ChatGPT, Mistral OCR

### For Clinical Documentation Requiring Legal Accuracy

**Recommended**: Claude only
**Acceptable**: Gemini with verification
**Avoid**: All others due to modification risks

### For General Document Processing

**Recommended**: Claude or Gemini based on formatting preferences
**Acceptable**: LlamaParse for content-focused applications
**Conditional**: Mistral OCR only after testing on specific document types

### For Document Summarization (Not Conversion)

**Acceptable**: ChatGPT's interpretive approach may be beneficial
**Preferred**: Still Claude/Gemini for accuracy with separate summarization step

## Final Assessment

This comprehensive analysis reveals that **Claude and Gemini represent the most reliable choices** for medical document conversion, with Claude showing slight advantages in consistency and structural organization. The critical finding is that medical document conversion requires specialized consideration of content fidelity, with models like ChatGPT being unsuitable for exact conversion tasks despite their general capabilities.

For healthcare organizations and medical professionals, the choice should prioritize accuracy and reliability over other factors, making Claude and Gemini the clear leaders in this specialized application domain.
