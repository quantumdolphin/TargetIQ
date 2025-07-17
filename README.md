# TargetIQ

This repository hosts the complete source code, configuration files, and helper scripts to build and deploy a custom GPT Agent that takes a **UniProt ID** (e.g., `P00533`) as input and returns structured biological metadata — including the **protein name, gene name, synonyms, and related PubMed articles**.

It uses:

* 🦠 **UniProt API** for fetching protein metadata
* 📚 **PubMed E-Utilities** for literature search
* 🧠 **OpenAI GPT Actions** for natural language interaction
* ⚙️ **Pipedream Webhooks** as middleware
* 🧪 Built and maintained by [@quantumdolphin](https://github.com/quantumdolphin)

---

## 📁 Folder Structure

```
gpt-target-lookup-agent/
│
├── README.md                  # 📘 Main guide and walkthrough
├── LICENSE                    # 📜 MIT License (open-source)
│
├── .gpt/
│   └── action.json            # 🔧 Final GPT Action OpenAPI JSON
│
├── pipedream/
│   ├── uniprot-step.py        # 🦠 Fetches UniProt metadata
│   ├── pubmed-step.py         # 📚 Fetches PubMed articles
│   └── export-results-example.png # ✅ Successful Pipedream test-- to be added
│
├── screenshots/
│   ├── gpt-action-setup.png   # ⬆️ Action upload screenshot--to be added
│   ├── success-run-preview.png # ✅ GPT response screenshot--to be added
│   └── error-fixes.png        # ❌ Common errors + solutions--to be added
│
└── docs/
    └── privacy-policy-template.md # 🔐 Privacy policy for public GPT--to be added
```

---

## 🛠️ How It Works

1. **User types** a UniProt ID (e.g., `P00533`) into the custom GPT.
2. The GPT triggers a **webhook** hosted on Pipedream.
3. The webhook:

   * Calls the **UniProt API** to fetch metadata
   * Calls the **PubMed API** to find related publications
4. The data is returned and **rendered cleanly** by the GPT.

---

## 🚀 Quickstart

> You need: GitHub Desktop, a Pipedream account, and ChatGPT Builder access

1. **Clone this repo** using GitHub Desktop or Git:

   ```bash
   git clone https://github.com/quantumdolphin/gpt-target-lookup-agent.git
   ```

2. **Create a new Pipedream workflow**:

   * Upload `uniprot-step.py` and `pubmed-step.py`
   * Connect a trigger to them and deploy

3. **Set up your GPT**:

   * Go to ChatGPT → Explore GPTs → Build your own
   * Import `.gpt/action.json`
   * Use your Pipedream webhook URL
   * Copy `docs/privacy-policy-template.md` into the Privacy tab

4. ✅ Done! Share your GPT.

---


## 📀 APIs and Tools

* [UniProt API](https://www.uniprot.org/help/api_queries)
* [PubMed E-Utilities](https://www.ncbi.nlm.nih.gov/books/NBK25501/)
* [Pipedream](https://pipedream.com)
* [OpenAI Custom GPTs](https://platform.openai.com/docs/guides/gpt/custom-gpts)

---

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for more information.

---

## 🙌 Acknowledgements

Thanks to OpenAI, UniProt, and NCBI teams for building excellent public APIs. Special thanks to the bioinformatics and drug discovery communities for inspiration.

---

## 🌟 Contributions

Feel free to fork, open issues, or submit pull requests — for example, adding:

## 🌟 Future improvements :

* Support for ChEMBL, Reactome, or DrugBank
* Variant annotations from ClinVar
* Improved summary generation from papers

