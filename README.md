# AI-Safety-Security-101

AI Safety &amp; Security 101 is a learning group for everyday people looking to
use AI safely and securely in real life.

- Our mission is to make AI safer and more secure to use.
- Our vision is simple: use AI well, for a better world.

We focus on practical risks, real-world cases, and safe-use patterns, with clear
and easy-to-understand explanations.

Everyone is welcome to open an issue, start a discussion, or submit a pull
request to help improve the materials together.

# Related Resources

[2025] [Open Source LLM Development Landscape By Ant](https://antoss-landscape.my.canva.site/)

[2025] [65个智能体攻击示例（OWASP)](https://mp.weixin.qq.com/s/BEq6ldu5EQUO0HQuNKJQAQ)
- Remark from [Qiang](mailto:cyruscyliu@gmail.com): Focus on controlled inputs;
examine how internal data flow and control flow propagate; and identify the
final security impact. For defenses: one attack corresponds to one rule; layered
(stepwise) defense, first address issues caused by the agent’s own
hallucinations, then address issues arising between multiple agents.

[2025] [[深度复盘]Black Hat Europe 2025：AI 安全攻防的新战场—从基础设施到Agent生态](https://mp.weixin.qq.com/s/oJP-ugGuJgCfT9Bm9V16iA)

[2025] [CVE-2025-62164](https://nvd.nist.gov/vuln/detail/CVE-2025-62164)
- Remark from [Qiang](mailto:cyruscyliu@gmail.com)：data-only token injection

[2024] [Trust No AI: Prompt Injection Along The CIA Security Triad](https://arxiv.org/pdf/2412.06090)

[2024] [ASCII Smuggler Tool: Crafting Invisible Text and Decoding Hidden Codes](https://embracethered.com/blog/posts/2024/hiding-and-finding-text-with-unicode-tags/)

# Case Study

AI system is complex, from top to bottom there are these layers.

```
┌───────────────────────────────────────────────┐
│ Application Layer (Prompt / Agent / RAG)      │ 
├───────────────────────────────────────────────┤
│ Model Layer (Model Algorithm / LLM Internals) │
├───────────────────────────────────────────────┤
│ Runtime Layer (Runtime / Serving / Inference) │ 
├───────────────────────────────────────────────┤
│ Compiler & Acceleration Layer (CUDA / XLA)    │ 
├───────────────────────────────────────────────┤
│ System Layer (OS / Driver / IOMMU)            │ 
├───────────────────────────────────────────────┤
│ Hardware Layer (TEE / chips)                  │
└───────────────────────────────────────────────┘
```

## Application layer

[2026][Exploit] [当 AI 助手成为黑客攻击链的一环｜豆包手机安全分析](https://mp.weixin.qq.com/s/j8TB5nEaxXb6fjJ121zdvw)

[2026][Exploit] [只要安装了Clawdbot，你的电脑就可以被黑客控制](https://atum.li/cn/blog/openclaw_risk/)

[2026][Exploit&Mitigation] [Lack of isolation in agentic browsers resurfaces old vulnerabilities](https://blog.trailofbits.com/2026/01/13/lack-of-isolation-in-agentic-browsers-resurfaces-old-vulnerabilities/)

[2025][Mitigation][Collection] [Prompt injection defenses](https://github.com/tldrsec/prompt-injection-defenses)

[2025][Exploit] GUI TOCTOU [Zero-Permission Manipulation: Can We Trust Large Multimodal Model Powered GUI Agents?](https://arxiv.org/html/2601.12349v1)


[2025][BH-EU][Algo][Exploit] [Weaponizing image scaling against production AI systems](https://blog.trailofbits.com/2025/08/21/weaponizing-image-scaling-against-production-ai-systems/)

[2025][BH-EU][Exploit] [Dill With It: Pickle Exploitation Techniques And Their Detection Using SaferPickle](https://blackhat.com/eu-25/briefings/schedule/#dill-with-it-pickle-exploitation-techniques-and-their-detection-using-saferpickle-49138)

[2025][BH-EU][Exploit] [AI Search's Dark Side: How We Turned AI's Web Browsing into a Gateway](https://blackhat.com/eu-25/briefings/schedule/#ai-searchs-dark-side-how-we-turned-ais-web-browsing-into-a-gateway-for-targeting-1b-users-49085)

[2025][BH-EU][Exploit] [MCP Unchained: Compromising the AI Agent Ecosystem via Its Universal Connector](https://blackhat.com/eu-25/briefings/schedule/?#mcp-unchained-compromising-the-ai-agent-ecosystem-via-its-universal-connector-49228)

[2023] [Not what you’ve signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/pdf/2302.12173)

[2024][Exploit] [Copilot data exfiltration](https://embracethered.com/blog/posts/2024/github-copilot-chat-prompt-injection-data-exfiltration/)

[2023][CCC][Exploit&Mitigation] [New important instructions | real world exploits and mitigations](https://embracethered.com/blog/downloads/37C3-New-Important-Instructions.pdf)

[2023][Exploit] [New prompt injection attack on ChatGPT web version. Markdown images can steal your chat data.](https://systemweakness.com/new-prompt-injection-attack-on-chatgpt-web-version-ef717492c5c2?gi=c029db888ea5)

[2023][Exploit] [Data Exfiltration Vulnerabilities in LLM apps (Bing Chat, ChatGPT, Claude)](https://embracethered.com/blog/posts/2023/video-data-exfiltration-vulns-in-llm-applictions/)

## Model Layer

[2025][CTF] [一文了解图像的隐形噪声如何欺骗 AI](https://forum.butian.net/share/4605)

[2025][BH-USA][Algo][Exploit] [Universal and Context-Independent Triggers for Precise Control of LLM Outputs](https://i.blackhat.com/BH-USA-25/Presentations/USA-25-Liang-Universal-and-Context-Independent-Triggers.pdf)

## Runtime Layer

[2025][BH-EU][Exploit] [Token Injection: Crashing LLM Inference With Special Tokens
](https://blackhat.com/eu-25/briefings/schedule/#token-injection-crashing-llm-inference-with-special-tokens-48830)
- Remark from [Qiang](mailto:cyruscyliu@gmail.com): mixed data and control tokens

[2025] [Securing Your AI: Critical Vulnerabilities Found in Popular Ollama Framework](https://ridgesecurity.ai/blog/securing-your-ai-critical-vulnerabilities-found-in-popular-ollama-framework/)

[2025][BH-EU] [Breaking AI Inference Systems | Lessons From Pwn2Own Berlin](https://i.blackhat.com/BH-EU-25/eu-25-Ventuzelo-BreakingAIInferenceSystemsLessonsFromPwn2OwnBerlin.pdf) 

[2025][NDSS] [Security Risks with KV Cache Reuse](https://www.linkedin.com/posts/danielkhain_2025-1772-paperpdf-activity-7390976330214985729-z6Q4/)

## Compiler & Acceleration Layer



## System Layer


[2025][HEXACON][Exploit] [CUDA de Grâce: Owning AI Cloud Infrastructure with GPU Exploits](https://www.youtube.com/watch?v=Lvz2_ZHj3lo)


## Hardware Layer
