# GenAI Knowledge Base (Vertex AI + Vector Search)

This project contains a working implementation of a Generative AI-powered knowledge base using **Google Cloud Vertex AI**, **Vector Search**, and **Firestore**. The workflow is based on the official Google GenAI notebook but adapted for live deployment and debugging.

---

## 🔧 Components Used

- Vertex AI Vector Search Index
- Vertex AI Index Endpoints (Deployed)
- Firestore (as document storage)
- Python Colab notebook (for querying and embedding)
- Google Generative AI SDK (`google.cloud.aiplatform`)
- Embedding model: `text-embedding-005`

---

## ✅ What’s Working

- [x] Project and region configuration
- [x] Vector Search index created and deployed
- [x] GenAI client initialization
- [x] Text embedding via Gecko model
- [x] Dummy document upload scaffold (Firestore integration)

---

## ⚠️ Issues Faced / To-Do

- [ ] Initial dummy upload to Firestore failed (`ValueError` from Firestore set call)
- [ ] Vector Search endpoint appears deployed, but `find_neighbors()` throws `IndexEndpoint not found` or `RPC` errors intermittently
- [ ] Need to confirm if Firestore database is correctly set up (`knowledge-base-database`)
- [ ] Missing visible upload cell in notebook → unclear where ingestion is intended

---

## 🧠 Next Steps

1. **Fix Firestore upload cell**
   - Confirm Firestore rules/database exist
   - Fix `doc.set({"pages": ...})` call if `doc` is not a valid document ref
2. **Re-test embedding + nearest neighbor match**
3. **Implement file ingestion flow**
   - Optionally support PDF/text drag-drop to Firestore & index
4. **Extend to structured document QA with prompt chaining**

---

## 🗂️ File Breakdown

| File | Purpose |
|------|---------|
| `genai_kb_workflow.ipynb` | Main notebook with end-to-end logic for Vector Search + Gemini integration |
| `README.md` | Project explanation and task tracking |

---

## 🤖 Author Notes

This project is in-progress and built via real-time debug tracing, screenshot-based validation, and zero-tolerance for code editing. Notebook snapshots reflect actual workflow states — no cleanup or hindsight polishing applied.

---

