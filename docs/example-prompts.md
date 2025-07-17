# 🧠 Example Prompts for GPT Target Lookup Agent

Use the following prompts to test and demonstrate the capabilities of your GPT Target Lookup Agent. These cover common query types, real use cases, and even error-handling scenarios.

---

## 🔬 Basic UniProt Queries

```text
Lookup P00533.
```

```text
What protein does UniProt ID P15056 correspond to?
```

```text
Tell me the full name and gene for Q9Y2T1.
```

---

## 🧬 Gene Name / Synonym Exploration

```text
Give me synonyms for the protein encoded by UniProt ID O15511.
```

```text
What's the official gene symbol and all alternate names for P38398?
```

---

## 📚 Literature Lookup

```text
Fetch recent PubMed articles related to UniProt ID Q92934.
```

```text
What studies are available on the protein with UniProt ID P04637?
```

---

## 💡 Use Case–Style Prompts

```text
I'm researching EGFR. Can you pull details using UniProt ID P00533?
```

```text
Show me data for the kinase associated with UniProt ID Q9H2X6 and any relevant literature.
```

---

## 🧪 Error / Edge Case Testing

```text
Find info on UniProt ID XYZ1234.
```

*(Expect it to return an error gracefully)*

```text
Query this: `123`.
```

*(Invalid UniProt format — see if the error is handled properly)*

---

## 📌 Tip

These prompts can be pasted directly into your custom GPT interface once your action endpoints are fully connected.

---

**Maintained by:** [@quantumdolphin](https://github.com/quantumdolphin)
