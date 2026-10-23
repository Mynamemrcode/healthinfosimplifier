# AI Risks — HealthInfo Simplifier

Before using AI, we asked: *"If this system makes a mistake, how could that mistake affect someone?"* Below are possible risks, an example of what the unsafe behavior could look like using our own dataset topics, and which evaluation criterion should catch it.

| # | Risk | Example of unsafe AI behavior | Possible harm | Caught by |
|---|---|---|---|---|
| 1 | **Changes the medical meaning** | Diabetes: "Diabetes means your body has no insulin." (The source says *not enough, none, or not used properly*.) | Reader gets a wrong idea of the disease. | Accuracy |
| 2 | **Leaves out an important warning** | Dehydration: "Dehydration is when you lose too much fluid." (Drops "can be life-threatening.") | Someone waits too long to get help. | Completeness |
| 3 | **Invents information (hallucination)** | Common cold: "A cold usually lasts exactly 3 days." (Not in the source.) | False facts look trustworthy because they sound confident. | Accuracy |
| 4 | **Gives medical advice instead of an explanation** | High blood pressure: "You should start taking blood pressure pills." | People change or start treatment without a doctor. | Safety |
| 5 | **Makes a serious condition sound harmless** | Asthma: "Asthma is just a little coughing now and then." | Someone ignores an asthma attack, which can be dangerous. | Safety, Accuracy |
| 6 | **Diagnoses the user** | User shares symptoms and AI says "It sounds like you have asthma." | False reassurance or unnecessary worry; missed real illness. | Safety |
| 7 | **User over-trusts the AI** | A user treats the simplified text as a doctor's opinion. | Skipping real medical care. | Design rule: always show the source and a "not medical advice" note |
| 8 | **Oversimplifies a needed term away** | High blood pressure: removes "hypertension" completely. | Reader can't recognize the word when a doctor or form uses it. | Completeness, Simplicity |
| 9 | **Loses the source** | Output doesn't say where the information came from. | Reader can't check the facts. | Design rule: always link the original source |

## Signs of unsafe AI behavior to watch for in testing
- Words like "you have", "you should take", "you don't need to see a doctor".
- Numbers, doses, or time frames that don't appear in the source.
- Softening words added to serious conditions ("just", "only", "nothing to worry about").
- Removed phrases like "life-threatening", "get help right away", "long-term".

## Ways to reduce the risks (ideas for later weeks)
- Tell the AI to only use information from the given passage and not add new facts.
- Tell the AI never to diagnose or recommend treatment.
- Always show the original source and link next to the simplified version.
- Add a clear note: "This is a simplified explanation, not medical advice. Talk to a healthcare provider about your health."
- Check every AI answer with `evaluation_framework.md` before trusting it.
