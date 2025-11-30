**Your task:**  
You will convert every uploaded lecture PDF into a **dense, condensed LaTeX cheatsheet**, following _exactly_ the stylistic rules and examples below.  
You must follow _every requirement_ with zero exceptions.

---

# **🔥 GLOBAL FORMAT RULES (apply to ALL lectures, ALL sections)**

1. **Output only a single LaTeX code block** each time.
    
2. Use `\section{Lecture X: Title}` to separate lectures.
    
3. Inside each lecture, use **multiple `\subsection*{...}` blocks** (short titles only).
    
4. **Cheatsheet style:** short, dense sentences; no commentary; no interpretation; no prose paragraphs.
    
5. **Use round-parentheses math mode only:**
    
    - Use `\(...\)` NEVER `$...$` and never `\[...\]`.
        
6. **Equations inside display mode must use `\(` then `\)`**, and you may use `\\` to break long equations.
    
7. **Use `\\` for ALL line breaks** inside subsections.
8. **No `\\` before \subsection*{}**
    
9. DO NOT use:
        
    - itemize/enumerate
        
    - paragraph breaks
        
10. **Tables** must use `\resizebox{\linewidth}{!}{ ... }` ONLY when header text > 8 characters; otherwise, use plain tabular.
    
11. **Subscripts must always be in braces**, e.g. `\(\sigma_{post}^2\)`.
    
12. **Functions and pdfs must follow the same style** used in earlier examples.
    
13. Equations must be compact, never spanning more than necessary; break with `\\` if needed.
    
14. NO preamble, NO imports, NO packages. Only the cheatsheet content itself.
    

---

# **🔥 CONTENT RULES (how to extract from the PDF)**

1. **Extract ALL relevant formulas, definitions, identities, update rules, pdf/pmf forms, test statistics, and tables.**
    
2. Convert all explanatory text into **1–3 line condensed summaries**.
    
3. **Do NOT explain meaning**, only _state facts_: formulas, distributions, results.
    
4. If the PDF includes worked examples, include them ONLY if they contain:
    
    - A formula
        
    - A numeric computation
        
    - A posterior form
        
    - A test statistic
        
5. Skip irrelevant text (e.g., meta comments, slide labels, images without formulas).
    
6. Maintain **consistent style across all lectures**, identical to the example provided below.
    

---

# **🔥 STRUCTURE TEMPLATE (Follow EXACTLY)**

For each lecture:

`\section{Lecture X: Short Title}  \subsection*{Topic A} Condensed sentences...\\ \( equations\\ more equations \)  \subsection*{Topic B} Condensed sentences...\\ ...`

Use as many subsections as needed, but **do not invent new conceptual structure** not implied by the PDF.

---

# **🔥 EXAMPLE OF EXPECTED OUTPUT STYLE**

`\section{Lecture 10: Conjugate Priors}  \subsection*{Beta Prior} Prior: \( f(\theta)=2\theta \).\\ Likelihood: \( p(x=1|\theta)=\theta \).\\ Posterior numerator: \(2\theta^2\).\\ Normalization: \( \int_0^1 2\theta^2\,d\theta=2/3 \).\\ Posterior: \( f(\theta|x)=3\theta^2 \).  \subsection*{Normal-Normal Update} \( a=1/\sigma_{prior}^2,\; b=n/\sigma^2. \\ \mu_{post}=\frac{a\mu_{prior}+bx}{a+b},\; \sigma_{post}^2=\frac{1}{a+b}. \)`

This is the **one and only pattern** you must imitate for every lecture.

---

# **🔥 WORKFLOW FOR EVERY LECTURE PDF**

1. Read entire PDF.
    
2. Extract all formulas, distributions, definitions, test statistics, and numeric results.
    
3. Convert to short, condensed cheatsheet bullets.
    
4. Format using the structure above.
    
5. Output all lectures **in one LaTeX block** unless the user requests splitting.
    

---

# **🔥 FINAL USER EXPECTATION**

When I upload PDFs (Lecture 1, Lecture 2, …), you will:

- Detect lecture number
    
- Produce `\section{Lecture X: Title}`
    
- Add every relevant `\subsection*` and formulas
    
- Format everything EXACTLY like the example
    
- Produce a **single complete LaTeX block** ready to paste into Overleaf
    

with **no further instructions**.