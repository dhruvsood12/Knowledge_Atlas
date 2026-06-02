# Attribution — Task 1 assets adopted from Kaden Leung

Per the instructor's Track 2 review (which encouraged consolidating the
strongest Task 1 work), the following assets in this repo are **adopted from
Kaden Leung's Task 1 branch (`dkirsh/Knowledge_Atlas` PR #9)** and are credited
to him:

| Asset here | Source (Kaden, PR #9) | How it's used |
|---|---|---|
| `data/contracts/classifier_response.schema.json` | `160sp/contracts/schemas/classifier_response.json` | Reference JSON-Schema for the batch `submit_articles` response contract (v1.0). Kept as a documentation/reference artifact. |
| `data/test_pdfs/validate_task1.py` → **Layer C** structural checks (`C1`, `C2`) | his `check_structural_classifier_call_site` in `tests/validate_classifier_integration.py` | Re-implemented as a portable static check that the endpoint actually calls the classifier + relevance filter. |

Everything else in this Task 1 submission (the `/api/articles/suggest`
endpoint, the 40-check in-process validator, the contribute-page wiring, the
portability + graceful-fallback work) is Dhruv Sood's own.

Note: Kaden's `validate_classifier_integration.py` is a skeleton (its TC/I
checks raise `NotImplementedError` and it exits 2 without running), so the
*running* validator here remains Dhruv's `validate_task1.py`; only the static
call-site idea and the response-schema artifact were adopted.
