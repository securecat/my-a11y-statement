# The Web Was Always Accessible. What I Told Anthropic, and Why.
# Webはそもそもアクセシブルなものである。Anthropicへの提言、その手前にある想い

*Yu Morita / 森田雄 (Turucame ltd. / 株式会社ツルカメ, CEO, Information Architect, Principal UX Designer, Accessibility Expert)*

---

## Introduction

This document is adapted from a feedback email I sent to Anthropic on June 21, 2026. I have removed the parts of my profile that were specific to that audience (such as my affiliation with the original recipient) and reorganized the rest so it stands on its own, readable by anyone.

It was only after sending that technical feedback to Anthropic that I realized the *root* of why I'd written it hadn't actually been put into words. For the proposal to be understood correctly, I first needed the premise behind it to come through clearly. Having realized that, I wanted to write it down here, while it's still fresh.

## はじめに

以下は、2026年6月21日に私がAnthropic社へ送ったフィードバックメールをもとに公開する文書である。Anthropic社向けに開示した自身のプロフィール（所属組織の記載など）は割愛し、誰もがフラットに読める内容に再構成した。

Anthropic社へ技術的な提言を送った後になって、自分の中でこの提言の「根っこ」が言葉になっていないことに気づいた。提言を正しく理解してもらうためには、まず、これがきちんと伝わっているという前提が必要だったのだ。それに気づいたこの機会に、それをここに書いておく。

---

### Belief 1: The Web Was Always Accessible

Tim Berners-Lee, the inventor of the Web, said it plainly:

> "The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect."

The Web was born accessible — as a medium, as a resource, as a technology. Given that, steering it toward fully realizing that fundamental power is simply the natural, obvious thing to do. Doing the opposite — building systems and tools that push it *away* from accessibility — is, frankly, absurd. It's a profound failure of judgment.

## 想い、その1：「Web」はそもそもアクセシブルなものである。

Webの生みの親、Tim Berners-Leeはこう言っている。

> "The power of the Web is in its universality. Access by everyone regardless of disability is an essential aspect."
> （Webの力は、その普遍性にある。障害の有無にかかわらず誰もがアクセスできることは、その本質的な側面である。）

Webは、生まれながらにしてアクセシブルなメディアであり、リソースであり、技術だ。したがって、その根源的な力を最大限に発揮させるように仕向けるのは、当然だし自然なことだろう。逆に、わざわざそうならないように仕向ける——アクセシブルであることを妨げる方向に技術や仕組みを動かす——というのは、完全に馬鹿げている。極めて愚かなことだと思う。

---

### Belief 2: Everyone Is a Potential Person with a Disability

Here's the other thing, and it might be the more important one.

Whether or not we think of ourselves as able-bodied, everyone is, at every moment, a potential person with a disability. An accident or illness can happen at any time — to anyone. Hands and feet might stop working the way they used to. Eyesight might fail. None of this would be strange even if it happened right after you finish reading this sentence.

And regardless of how that turns out, I find myself always feeling this:

**"I want to keep using the Web, unchanged. I want to work on the Web, and enjoy the things made for it. I can't imagine a life without it. Whatever condition I'm in, I want to keep using the Web until the day I die."**

Accessibility is what makes that possible.

I don't think this is a feeling unique to me. If you're reading this, I'm certain you feel exactly the same way — that you, too, want to keep using the Web, unchanged, no matter what.

I want to keep using generative AI services like Claude, too, unchanged, for as long as I can. So — crushing that quiet but real human "wish," just to avoid guaranteeing something as small as a contrast ratio? I want to believe that can't possibly be true.

## 想い、その2：人は常に潜在的な障害者である

もう一つ、もっと大事なことがある。

人は誰しも、自分を健常者だと思っていようがいまいが、常に潜在的な障害者だ。いつ事故に遭うかも、いつ病気になるかもわからない。手足が思うように動かなくなるかもしれない。目が見えなくなるかもしれない。それは、今この文章を読んだ直後に起きても、何ら不思議ではないことだ。

そして私は、そのことがどうであるかに関わらず、常にこう思っている。

**「Webをずっと変わらず使いたい。Webで仕事もしたいし、Webのコンテンツを楽しみたい。Webのない人生など考えられない。自分がどんな状況にあっても、死ぬそのときまで、ずっとWebを使いたい」**

それを実現してくれるのが「アクセシビリティ」だ。

これは私だけの特殊な感情ではないはずだ。今これを読んでいるあなたも、きっと同じように、Webをずっと変わらず使いたいと思っているに違いない。

Claudeなどの生成AIサービスも、私はずっと変わらず使いたいと思っている。そのような、人間のささやかな、しかし切実な「願い」をつぶしてまで、コントラスト比ひとつ確保したくないなんて——そんなこと、あるわけがないと信じたい。

---

### What follows is the technical proposal built on these two beliefs

With these two beliefs as the foundation, I sent Anthropic the following feedback.

## ここから先は提言：技術的な背景

以上の2つの想いを土台として、私はAnthropic社へ以下の趣旨のフィードバックを送った。

---

## Feedback: WCAG 2.2 AA as Claude's Default Baseline

**Who I am**

My name is Yu Morita. I am an Information Architect, Principal UX Designer, and Accessibility Expert based in Japan, with over 30 years of experience in web design and digital work. I am the CEO of Turucame Ltd. (https://turucame.jp/).

I am sharing this feedback as a long-time Claude Pro and GitHub Pro subscriber who uses Claude (both claude.ai and Claude Code) daily in my professional accessibility and design work.

**The feedback**

I would like to formally request that Anthropic consider establishing WCAG 2.2 Level AA as Claude's default baseline quality standard for any code, UI, or design output — not as an opt-in feature, but as part of the model's default behavior, on par with how Claude already treats things like secure coding practices or meaningful variable naming as unprompted defaults.

**Why this matters**

1. **"Training data reflects a low-accessibility web" is not a sufficient explanation.** Most of the web's existing code is not WCAG-compliant, and this shapes what a language model considers "typical" output. But this is a description of the problem, not a justification for it. Claude already overrides "typical" patterns from training data in other domains — for example, defaulting toward secure coding practices even when insecure patterns are statistically more common in public code. The same kind of deliberate override is technically achievable for accessibility through RLHF and instruction-tuning priorities. The absence of this prioritization looks like a choice, not a limitation.

2. **Accessibility is now a global legal and business risk, not a regional nicety.** Many jurisdictions (the EU via the European Accessibility Act, the US via ADA litigation, and others) have legally enforceable accessibility requirements with real penalties. An AI system that generates inaccessible code by default is generating legal and reputational liability for every business that relies on it — including, indirectly, for Anthropic itself, given how central Claude has become to code generation workflows (Claude Code, Claude Design, etc.).

3. **Accessibility is now a global design standard, not an edge case.** In modern UX and product design practice internationally, WCAG AA compliance is treated as a baseline expectation, not a specialized add-on. A model whose default output requires manual correction to meet this bar is, in effect, behind the industry standard it is otherwise trying to lead in.

4. **This is a meaningful differentiation opportunity, not just a risk to mitigate.** With the recent investment in Claude Design and its design-system integration with Claude Code, Anthropic has a real opportunity to make "Claude-generated output meets WCAG AA by default" a competitive differentiator.

**What I am currently doing as a workaround, and why it isn't enough**

In my own workflow, I maintain a detailed accessibility instruction file (`A11Y.md`) as global configuration for Claude Code, paired with markuplint for automated linting. These layered workarounds genuinely help, but they share the same limitation: they are all external corrections layered on top of a model that does not, by default, treat WCAG AA as a baseline. Design systems and lint rules can catch missing attributes or out-of-range contrast values, but they cannot replicate the judgment-level instinct of building with accessibility in mind from the first line of code — the same way a well-trained model doesn't need to be told not to introduce a SQL injection vulnerability.

I recognize this is ultimately a training-and-prioritization decision that sits above what any user-side configuration can solve. I wanted to make sure this perspective reaches the team shaping that decision.

---

*I'm publishing this not just for the technical argument, but to share what's underneath it. If this resonates with you, please share it, in your own words, wherever you are.*

*この文書は、技術的な合理性の話だけでなく、その手前にある想いを共有するために公開しています。もし共感していただけたら、それぞれの場所で、それぞれの言葉で、是非共有してください。*

*If something here resonated with you — or even if you disagree — I'd love to hear it. Feel free to open an [Issue](../../issues) or send me a message on [X @securecat](https://x.com/securecat). Your own story about the Web counts too.*

*もし何か感じるものがあれば——あるいは違う意見があっても——ぜひ聞かせてください。[Issues](../../issues)でも、[X @securecat](https://x.com/securecat)でのメッセージでも構いません。あなた自身のWebにまつわる話も、聞かせてもらえたら嬉しいです。*

2026-06-21 Yu Morita

---

## License

This work is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
