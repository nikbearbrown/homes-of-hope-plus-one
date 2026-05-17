# Research Note — Unit 2: AI as Work Tool

*Working pantry document for Homes of Hope +1, Course 2 — Unit 2 (AI as Work Tool). The chapter teaches Priya (19, Telugu first language, ~350 English words, smartphone fluency, basic ChatGPT exposure) to use ChatGPT/Gemini as a drafting assistant rather than a substitute thinker. Notes are for the chapter author. Compiled 2026-05-17.*

---

## Preliminary: the unit's thesis in one sentence

A girl who uses AI as a drafting assistant and catches its mistakes is more employable in Hyderabad's 2026 market than a girl with stronger English who uses AI as a replacement thinker — *because the second girl produces output she cannot defend in a phone screen*. The chapter has to teach the first behavior and inoculate against the second.

The architecture is identical to the Bastani GPT Tutor / GPT Base contrast from the medhavy pantry's `ask-ai-research.md`: same model, two prompt patterns, opposite learning outcomes. The unit here ports that finding from math practice to job-application drafting. The girl whose ChatGPT use builds her own English is the GPT Tutor case. The girl whose ChatGPT use offloads her English is the GPT Base case. The unit is the architecture that prevents her from becoming the second case.

---

## A. Conceptual foundations — 3–5 most important ideas

### A.1 The Bastani performance/learning split, ported to ESL

[Bastani et al. 2025, *PNAS*](https://www.pnas.org/doi/10.1073/pnas.2422633122) is the most important paper for this chapter. RCT in a Turkish high school, ~1,000 students, 9th–11th grade, math practice. Three conditions: no AI, GPT-4 with default chat ("GPT Base"), GPT-4 with a teacher-designed hint wrapper that refused to give answers ("GPT Tutor"). During practice: GPT Base students scored 48% higher than the no-AI control, GPT Tutor students scored 127% higher. On a subsequent exam *without AI*: GPT Base students scored 17 percentage points *lower* than the no-AI control. GPT Tutor students were statistically indistinguishable from the no-AI control.

The mechanism: GPT Base students were performing well during practice *because GPT-4 was doing the work*. The skill was not building. When the AI was withdrawn, the gap appeared. GPT Tutor students were forced to do the work themselves — slower during practice, but skill-equivalent to controls afterwards. The system prompt was the variable. Same GPT-4 underneath.

For Priya, the analogy is direct. If she pastes "write me a cover letter" into ChatGPT, copies the output, and sends it — she will get callbacks for jobs whose interviews she cannot pass, because her actual English has not moved. She will be the −17% case in spoken form. If she uses ChatGPT to draft, reviews it, edits the parts she can defend, asks the AI to explain anything she doesn't understand, and only then sends — her own English builds while she applies. That is the GPT Tutor case in self-directed form.

The chapter cannot literally enforce a GPT Tutor wrapper on her phone. ChatGPT is GPT Base by default. What the chapter can do is teach her to *act as her own wrapper*: prompt, then review, then correct, then explain-back. The two-step workflow in the TIKTOC (item 3 under core content) is the operational form of this.

### A.2 The cognitive-offloading risk is sharper for ESL learners than for L1 users

[Lee, Sarkar, Tankelevitch et al. 2025, *CHI 2025*](https://dl.acm.org/doi/full/10.1145/3706598.3713778) — Microsoft Research / CMU survey of 319 knowledge workers, 936 first-hand GenAI examples. Findings:

- 72–79% of users reported "less effort" or "much less effort" on Knowledge, Comprehension, Application, Analysis, and Synthesis tasks.
- *Higher confidence in GenAI was associated with less critical thinking; higher self-confidence was associated with more critical thinking.*
- Where critical thinking persisted, it shifted *away from generation* toward *verification, integration, and stewardship*.

The directional finding aligns with Bastani. For Priya, two things sharpen the risk:

- **Lower baseline self-confidence.** A learner with 350 English words who has been told her English isn't good enough has below-average self-confidence in English. Lee's correlation predicts she will defer harder to the AI than a confident L1 user would. The offloading risk is concentrated where she most needs the practice.
- **The vetting problem.** The AI's output is in fluent English she does not yet fully understand. She cannot reliably evaluate it ([Selwyn 2022, *European Journal of Education*](https://onlinelibrary.wiley.com/doi/10.1111/ejed.12532); [Stanford HAI 2024 on AI bias against diverse student populations](https://hai.stanford.edu/news/how-harmful-are-ais-biases-on-diverse-student-populations)). She is least equipped to vet the AI precisely where she most needs to. This is structural; the chapter cannot wave it away.

The chapter has to take this seriously without scaring her off the tool entirely. The honest framing: AI is a powerful drafting assistant *if she does three things* (review, correct, ask-back); it is a callback-generating trap *if she doesn't*.

### A.3 The Tutor CoPilot architecture — AI as scaffold for the weaker user

[Wang, Ribeiro, Robinson, Loeb & Demszky 2024, arXiv:2410.03017](https://arxiv.org/abs/2410.03017) — RCT with 900 tutors and 1,800 K–5 students. Tutor CoPilot is an AI assistant for live human tutors, not a direct student-facing chatbot. Mastery of learning objectives rose by 4 percentage points overall and 9 percentage points for students working with lower-quality tutors at baseline.

The mechanism this paper isolates: AI gives the biggest lift exactly where the human's baseline is thinnest. For Priya, this is the most encouraging single finding in the GenAI education literature. Her English is below the median Hyderabad job-applicant's English. AI as a drafting assistant gives her the largest possible lift — *if she uses it like the better tutors used Tutor CoPilot, as an instrument that improves her own output, not as a substitute*.

The chapter can lean on this evidence without overstating it. The Tutor CoPilot population was K–5 students with US tutors; the analogy to Priya is structural, not literal. But it makes the lower-baseline-larger-lift point honestly, with data.

### A.4 AI hallucinates differently in job-application contexts than in math contexts

The general-purpose finding ([Banerjee et al. 2024, arXiv:2409.05746](https://arxiv.org/html/2409.05746v1)) is that hallucination is a structural feature of LLM architecture, not a fixable bug. The specific failure modes for job-application writing — relevant to Priya — are distinct from the math-hallucination modes the trust-the-teacher and medhavy literatures cover:

- **Fabricated work history.** ChatGPT will fluently invent "internship at Apollo Hospitals, June–August 2023" because the prompt context suggested it would be helpful. Priya did not do this internship. The hiring manager calls Apollo, the internship does not exist, the application is dead and the candidate is flagged. This is the highest-stakes hallucination for this population.
- **Wrong company facts.** Ask ChatGPT for a cover letter to Genpact and it will confidently describe Genpact's services in language that may or may not match Genpact's 2026 reality. The hiring manager works at Genpact and knows. Generic-sounding cover letter signals to him *that the candidate did not bother to learn what we actually do*.
- **Generic-sounding language.** This is the most subtle failure. The AI produces *"I am a passionate and dedicated professional seeking opportunities to contribute meaningfully"* — grammatically perfect, register-appropriate, semantically empty. The hiring manager has read this sentence 4,000 times. It signals nothing about Priya. A clumsy specific sentence ("I want to work at Apollo because I helped at the sisters' clinic in Secunderabad for two years") beats a polished generic sentence every time, but Priya does not know this because the AI's polish reads to her as quality.
- **Wrong register for Indian corporate culture.** AI defaults toward US business English. Without prompting, ChatGPT will produce *"Hey [Name], Hope this finds you well! Just wanted to circle back..."* — a register that reads as slightly unprofessional in Hyderabad BPO contexts. Unit 1's register framework is what lets Priya catch this; without Unit 1, this is invisible.

The chapter has to name all four failure modes by example, not by abstraction. *"Find the thing the AI invented"* should be a recurring exercise pattern throughout the book.

### A.5 The two-step workflow — prompt → review → correct

The operational instruction the chapter teaches:

1. **Prompt** in simple English with the context the AI needs. Not *"write a cover letter"*. Instead: *"Write a short professional message in Indian business English to apply for this BPO customer service job at Concentrix. I am a 19-year-old fresher from Hyderabad. I have completed Anki-based English vocabulary training and I have community-living experience from a Homes of Hope residence for six years. Here is the job posting: [paste]."* The prompt gives the AI Priya's actual background and her actual target. This produces specific output, not generic output.
2. **Read every line.** Out loud if necessary. The rule: if she cannot say what a sentence means in Telugu in her head, she does not send it. This is the vetting move ported into something she can actually do.
3. **Mark the lines that are wrong or generic.** Wrong = fabricated facts about her, wrong register, factual error about the company. Generic = sentences a hiring manager has read 4,000 times.
4. **Correct each marked line.** Either rewrite it in her own words (preferred), or ask the AI to rewrite it with specific guidance (*"replace the passionate-and-dedicated line with one specific thing from my background"*). The bias should be toward her own words — even a clumsy sentence in her own voice beats a polished generic one.
5. **Ask the AI to explain anything she doesn't understand.** *"What does 'liaise with stakeholders' mean? Give me a one-sentence explanation in simple English with an example."* This is the GPT Tutor move — she is using the AI to teach her, not to think for her.

The chapter has to make this workflow concrete with three or four worked examples. Abstract instruction will not survive contact with Priya's actual practice on her actual phone.

---

### Worked example — the two-girl scenario from the TIKTOC, built out

The TIKTOC opening for Unit 2 sets up two girls applying for the same BPO customer service position at Concentrix Hyderabad.

**The job posting (illustrative, modeled on actual Naukri postings):**

> *Customer Service Associate — Voice Process — Concentrix Hyderabad*
> *Freshers welcome. 0–1 year experience. Excellent English communication skills mandatory. Night shifts available. Pickup and drop facility provided. Qualification: Intermediate (12th pass) or above. Walk-in interviews Mon–Fri, 11 AM–4 PM at our Madhapur office. Contact: [HR phone number].*

**Girl 1 — over-relies on AI.** She pastes the posting into ChatGPT and prompts: *"Write a cover letter for this job."* AI produces:

> *Dear Hiring Manager,*
>
> *I am writing to express my keen interest in the Customer Service Associate position at Concentrix Hyderabad. As a passionate and dedicated professional with a strong commitment to delivering exceptional customer experiences, I am confident that my skills align perfectly with the requirements of this role.*
>
> *Throughout my academic and professional journey, I have honed my communication skills and developed a customer-first mindset. I have successfully handled complex customer interactions during my internship at Apollo Hospitals (June–August 2023), where I gained valuable experience in resolving customer concerns with empathy and efficiency.*
>
> *I am particularly excited about the opportunity to leverage Concentrix's industry-leading platforms and contribute to your mission of transforming customer experiences. My fluency in English, Hindi, and Telugu would enable me to serve a diverse customer base effectively.*
>
> *I am available for an interview at your earliest convenience and look forward to discussing how I can contribute to your team.*
>
> *Best regards, [Name]*

She copies it, pastes her name, sends it. Two days later HR calls and asks her to come in for a walk-in. She comes in. The recruiter asks: *"Tell me about your internship at Apollo."* She has never done an internship at Apollo. She freezes. The interview ends in two minutes.

What went wrong: ChatGPT fabricated the Apollo internship because the prompt did not say "I am a fresher with no formal work history." The model defaulted to a successful-candidate template. The girl did not catch it because the fluent English looked like quality. Three other things are also wrong in less catastrophic ways: *passionate and dedicated professional* is generic; *industry-leading platforms* is filler; *fluency in English* is overstated for a girl with 350 English words.

**Girl 2 — uses AI as drafting assistant.** Same posting. She prompts: *"Write a short professional message in Indian business English to apply for this BPO customer service job at Concentrix Hyderabad. I am 19, a fresher with no work experience. I grew up in a Homes of Hope residence in Secunderabad for six years where I learned punctuality, professional conduct, and community living. I have completed an English vocabulary training program. I speak Telugu, Hindi, and basic English. I have not done any internships. Here is the posting: [paste]. Keep it under 150 words."*

AI produces:

> *Dear Hiring Manager,*
>
> *I am writing to apply for the Customer Service Associate position at Concentrix Hyderabad. I am a fresher who recently completed an English communication training program and I am eager to begin my career in the BPO industry.*
>
> *I grew up in a Homes of Hope residence in Secunderabad for six years, where I developed strong values of punctuality, discipline, and professional conduct. I am comfortable working in a team and committed to learning. I speak Telugu, Hindi, and English.*
>
> *I would like the opportunity to interview for this role and demonstrate my potential. I am available to attend the walk-in interview at your Madhapur office on any weekday.*
>
> *Thank you for considering my application.*
>
> *Best regards, Priya [last name] [phone number]*

She reads it line by line. Three things she catches:

- *"strong values of punctuality, discipline, and professional conduct"* — accurate but sounds like AI filler. She rewrites: *"living in a residence with daily routine and shared responsibility taught me to be on time and to take my work seriously."* Same idea, her voice.
- *"I would like the opportunity to interview"* — fine, but she adds the specific availability: *"I can attend the walk-in interview at your Madhapur office on Monday or Tuesday next week between 11 AM and 1 PM."* Specific signals professional.
- The closing line is missing a phone number. She adds it.

She also asks ChatGPT one clarification: *"What does BPO industry mean in simple English?"* — so that if HR asks "why BPO?" in the screen, she has a real answer, not a script.

She sends. HR calls. She comes in. The recruiter says *"Tell me about the residence."* Priya has actually lived this. The conversation goes for fifteen minutes. The interview ends in a verbal offer pending background check.

Same AI. Same posting. Same opening prompt structure. The variable was the review step.

**What Priya with her current profile would and would not catch:**

Likely to catch (with chapter scaffolding):
- The fabricated Apollo internship (because she knows her own history; this is the catch-the-invented-fact exercise pattern)
- Missing phone number in sign-off (because Unit 1 trained sign-off conventions)
- "Passionate and dedicated professional" sounding generic (with chapter exercises on the generic-AI-phrase pattern)

Likely to miss (without further scaffolding):
- "industry-leading platforms" — she doesn't know what platforms Concentrix uses; she can't tell if it's accurate or filler
- "fluency in English" overstated — fluency is a relative term; she may not flag this as overclaim
- US-business-English register slips (*Hey [Name], Hope this finds you well, circle back*) if they appear

The chapter has to teach the catchable ones explicitly and flag the missable ones for volunteer review in the Zoom session.

---

## B. Domain examples and cases

### B.1 ChatGPT's behavior with Indian English / Hyderabad contexts

Empirically, GPT-4 and GPT-4o handle Indian Business English well *when prompted explicitly* and revert to American business English by default. Unprompted output uses *"Hey,"* *"circle back,"* *"reach out,"* *"loop me in"* — all of which read as US tech-startup register, not Hyderabad BPO register. With the explicit instruction "*in Indian business English*" or "*for a Hyderabad-based role*" the register shifts measurably. Gemini behaves similarly. [verify with current 2026 model versions]

The chapter teaches one prompt-engineering move that is more important than any other: *include the register specification in the prompt*. Saying "for a Hyderabad BPO job" gets the model to produce Indian Business English. Not saying it gets the US default.

### B.2 What ChatGPT/Gemini reliably get right for this population

- **Spelling and basic grammar.** ESL learners over-correct their grammar and end up with stiff, over-controlled English; AI smooths it.
- **Register translation from casual to consultative** when asked. *"Make this sound more professional"* on a casual draft works reliably.
- **Vocabulary expansion.** *"Give me three professional ways to say 'I can do this work'"* — useful for breaking out of repeated 350-word loop.
- **Structure of standard documents.** CV section headers, cover letter paragraph order, thank-you-after-interview structure.

### B.3 What they reliably get wrong

- **Specific factual claims about Priya's history.** Even mild prompts produce confabulated specifics. (This is the central hallucination risk.)
- **Specific factual claims about companies.** Concentrix's 2026 service lines, Apollo's current units, CRY's current programs — AI knowledge is partial and confidently stated.
- **Numerical specifics.** Salary expectations, role responsibility percentages — usually invented when not in the prompt.
- **Local cultural specifics.** *Madhapur*, *Hi-Tech City*, the difference between Banjara Hills and Jubilee Hills, the local commute logic — AI knows these as locations but does not know which is closer to her residence or what *pickup and drop facility* actually means in the working life of a girl in Secunderabad.

### B.4 The Hyderabad ChatGPT user-base context

[verify — there is a Microsoft/OpenAI usage-share study cited in trade press; the specific Hyderabad / Telangana share is in low single digits but rising fast in the 18–24 segment]. The reality the chapter should acknowledge: ChatGPT use among Priya's peer group is already common but mostly recreational (translation, homework help). The chapter is not introducing the tool; it is reframing what she already uses.

---

## C. Connections and dependencies

- **Depends on:** Unit 1 (Professional Register). Priya cannot evaluate whether AI output is at the right register without Unit 1's framework.
- **Depends on:** smartphone fluency, basic ChatGPT exposure. Both safe to assume from the learner profile.
- **Does not depend on:** programming knowledge, prompt-engineering theory, model internals. The chapter is operational, not conceptual.
- **Unlocks:** Unit 3 (CV) — the CV is the first long-form AI-assisted document she will produce.
- **Unlocks:** Unit 4 (Job Search) — AI as posting interpreter is a Unit 2 capability deployed in Unit 4.
- **Unlocks:** Unit 5C (NGO report/proposal English) — entirely an AI-drafted output with human review.
- **Cross-references:** the medhavy `ask-ai-research.md` Bastani/Tutor CoPilot/Kestin evidence is the load-bearing literature here. Same architecture, different application. The chapter should not cite ask-ai-research.md directly; it should cite Bastani 2025 *PNAS* and Wang et al. 2024 in its own references.

---

## D. Current state of the field

### Settled

- AI use during practice without guardrails reduces durable learning, demonstrated in a large RCT ([Bastani et al. 2025, *PNAS*](https://www.pnas.org/doi/10.1073/pnas.2422633122)).
- AI use *with* guardrails (designed hint patterns, review steps, refusal-to-answer prompts) preserves and can enhance learning ([Bastani 2025, *PNAS*](https://www.pnas.org/doi/10.1073/pnas.2422633122); [Kestin et al. 2025, *Scientific Reports*](https://www.nature.com/articles/s41598-025-97652-6)).
- AI as scaffold for lower-baseline users produces larger lifts than for higher-baseline users ([Wang et al. 2024, arXiv:2410.03017](https://arxiv.org/abs/2410.03017); converging evidence in [Noy & Zhang 2023, *Science*](https://www.science.org/doi/10.1126/science.adh2586) on writing tasks).
- LLMs hallucinate as a structural property of the architecture ([Banerjee et al. 2024](https://arxiv.org/html/2409.05746v1)). RAG and prompting mitigate but do not eliminate.
- Self-reported critical thinking declines with AI confidence ([Lee et al. 2025, *CHI*](https://dl.acm.org/doi/full/10.1145/3706598.3713778)).

### Contested

- Whether the RCT findings from US college / Turkish high school populations generalize to South Asian ESL adults. The literature has not yet run this trial. The mechanism (offloading vs. scaffolding) is plausibly universal; the magnitudes are not yet measured for this population.
- Whether GPT-4o / Gemini 2 / Claude differ meaningfully in their hallucination patterns for personal-history prompts. Practitioner reports vary; published comparative benchmarks for this specific failure mode are thin.

### Unsettled

- The right "review intensity" for an ESL drafting workflow. Is line-by-line review necessary, or is paragraph-level review sufficient? No empirical answer. The chapter teaches line-by-line conservatively.
- How much of the offloading harm is reversible with one volunteer feedback session. The Tutor CoPilot result suggests substantial; not yet measured in self-directed AI use.

### Key references for this chapter

- Bastani, Hamsa, Osbert Bastani, Alp Sungu, Haosen Ge, Özge Kabakcı, and Rei Mariman. 2025. "Generative AI Without Guardrails Can Harm Learning: Evidence from High School Mathematics." *PNAS* 122(26): e2422633122. https://www.pnas.org/doi/10.1073/pnas.2422633122
- Wang, Rose E., Ana T. Ribeiro, Carly D. Robinson, Susanna Loeb, Dora Demszky. 2024. "Tutor CoPilot: A Human–AI Approach for Scaling Real-Time Expertise." arXiv:2410.03017. https://arxiv.org/abs/2410.03017
- Kestin, Greg, et al. 2025. "AI Tutoring Outperforms In-Class Active Learning." *Scientific Reports* 15. https://www.nature.com/articles/s41598-025-97652-6
- Lee, Hao-Ping (Hank), et al. 2025. "The Impact of Generative AI on Critical Thinking." *CHI 2025*. https://dl.acm.org/doi/full/10.1145/3706598.3713778
- Banerjee, Sourav, Ayushi Agarwal, Saloni Singla. 2024. "LLMs Will Always Hallucinate, and We Need to Live With This." arXiv:2409.05746. https://arxiv.org/html/2409.05746v1
- Noy, Shakked, and Whitney Zhang. 2023. "Experimental Evidence on the Productivity Effects of Generative Artificial Intelligence." *Science* 381(6654): 187–192. https://www.science.org/doi/10.1126/science.adh2586
- Selwyn, Neil. 2022. "The Future of AI and Education: Some Cautionary Notes." *European Journal of Education* 57(4): 620–631. https://onlinelibrary.wiley.com/doi/10.1111/ejed.12532
- Bjork, Elizabeth L., and Robert A. Bjork. 2011. "Making Things Hard on Yourself, But in a Good Way." https://bjorklab.psych.ucla.edu/wp-content/uploads/sites/13/2016/04/EBjork_RBjork_2011.pdf

---

## E. Teaching considerations — where ESL learners get stuck

### E.1 The "AI sounds better than I do, so AI is right" trap

This is the central pedagogical risk. Priya reads the AI output. It sounds smooth. Her draft sounds rougher. She concludes the AI is right and her version is wrong, even when her version is more accurate and the AI's version is fluent fabrication. The Lee et al. confidence finding predicts this exactly: deferring to AI when one's own confidence is low.

The chapter's countermove: name this trap explicitly. *"Fluent English is not the same as true English. If the AI writes a sentence about you that is not true, the smoothness does not make it true. The sentence has to be true first and smooth second."* Then reinforce with the find-what-the-AI-invented exercise pattern.

### E.2 The prompt-engineering shape Priya needs

She does not need to learn "prompt engineering" as a discipline. She needs three slot-filler templates:

- **Draft template:** *"Write [type of document] in Indian business English for [job/context]. I am [her background in simple sentences]. Keep it under [word count]. Here is [posting/context if any]."*
- **Explain template:** *"What does [word/phrase] mean in simple English? Give me one example."*
- **Critique template:** *"Read this and tell me what sounds generic or wrong: [her draft]."* — this is the AI helping her review, which is closer to the GPT Tutor case.

Three templates. Two pages of pattern exposure. Done. Anything more is over-engineering for this audience.

### E.3 The "I can't tell when AI is wrong" problem

The honest answer the chapter has to give: she can't always. That's why Unit 2 is not the last word — the Zoom volunteer is. The chapter's design move: do not ask Priya to be a sufficient vetter of AI output by herself. Ask her to be a *first-pass filter* (catch the obvious fabrications, the wrong register, the generic filler), and route the residual risk to the volunteer review.

This is exactly the Tutor CoPilot architecture inverted — instead of AI scaffolding a weaker human tutor, the human Zoom volunteer scaffolds an AI-assisted weaker learner. The human is doing the irreducible review that AI cannot reliably do for her own output.

### E.4 The Indian-context analogy that works

For Priya, the closest analogy is the rickshaw quote. She knows that when she asks an auto-rickshaw driver for a fare, the first number he gives her is high. She does not say *no, you're wrong, I'm not taking your auto*. She says *the meter price is 80, I will pay 90*. She negotiates. She *trusts the meter, not the driver's first number*.

AI is the same. The first output is a starting point. The meter — what is actually true about her, what register the job actually wants, what specific things the company actually does — is the thing she negotiates the output against. The chapter can use this analogy once, named clearly, then move on. It is one of the rare analogies that works without flattening.

### E.5 The Pekrun anxiety-quadrant risk specifically

The TIKTOC's Risk 3 names this for the mock-call session: low perceived control plus high stakes equals withdrawal. Unit 2 has its own version of this risk. A girl who tries AI, doesn't catch a hallucination, gets called for an interview, fails the interview, and concludes *AI made me fail* — withdraws from AI entirely and loses the most useful tool she has.

The mitigation is the same shape as the Zoom-session mitigation: the first AI-assisted output produced in this unit is explicitly framed as practice, reviewed by volunteer before sending. The first stakes-bearing AI output happens after at least one volunteer-reviewed practice cycle. The chapter has to make this scaffolding visible.

---

## F. Library files relevant to this chapter

- Heavy cross-reference: `/Users/bear/Documents/CoWork/bear-textbooks/books/medhavy/pantry/ask-ai-research.md` — the load-bearing Bastani / Tutor CoPilot / Kestin / Khanmigo literature is mapped there. The author should read it before drafting Unit 2; the medhavy chapter on Ask AI (`/books/medhavy/chapters/06-medhavy-conducting-ai.md` and adjacent) shows what the prose voice can look like.
- Light cross-reference: `/Users/bear/Documents/CoWork/bear-textbooks/books/trust-the-teacher/chapters/07-the-cognitive-offloading-problem.md` — the offloading argument in published-chapter form. Same evidence, different audience; useful as voice calibration.
- No direct MD-library hits for "AI as ESL drafting tool" specifically.

---

## G. Gaps and flags

- **Population-specific evidence gap.** No published RCT on AI-assisted writing for South Asian ESL adults in a job-application context. The Bastani / Tutor CoPilot / Kestin findings are imported by analogy. Strong analogy, but flag as not directly measured.
- **Model-specific behavior gap.** Whether ChatGPT (free tier vs. Plus tier), Gemini, or Claude differs meaningfully in Indian-business-register defaults — practitioner-level only, no formal benchmarks. The chapter should be model-agnostic where possible and prompt-explicit where not. `[verify with a quick comparison test before final draft]`
- **Free-tier vs. paid-tier flag.** Priya almost certainly uses free-tier ChatGPT and free-tier Gemini. Both have lower-quality output than paid tiers, particularly in regional-register tasks. The chapter should not assume Plus access. Where the chapter recommends a specific prompt, test it on free-tier first.
- **WhatsApp-Bing / Meta AI on WhatsApp flag.** Meta AI is now embedded in WhatsApp in India. Priya may not realize ChatGPT-equivalent capability is one tap away inside the app she uses most. The chapter should mention this explicitly.
- **What would change my mind:** A 2025+ study showing that for ESL job applicants, unguarded AI use (no review step) produces *better* callback-to-offer conversion than reviewed-AI use. I do not expect this; if it appears, the chapter's core architecture is wrong. The Bastani finding makes this very unlikely.

---

*End of pantry research note for Unit 2.*
