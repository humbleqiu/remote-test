# ✅什么是Skill的自进化机制？

# 典型回答


Skill自进化机制是最近很火的Hermes Agent引入的一种Agent优化手段（也有人锤他说是抄袭了国产的EvoMap），他主要解决的是以下这个问题：





> 比如我在使用<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);">OpenClaw这种agent完成一个任务后，无论过程中走了多少弯路、犯了多少错误，这些宝贵的经验都不会沉淀下来，都是用后即焚的。即使下次再遇到相同的任务，他还会从头再来一遍，把踩过的坑再踩一遍。即使你让它记录Memory，他也只是会记录一些简要的重点事项和用户习惯，并不会记录太多执行细节。</font>
>





<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);">在</font>Hermes Agent中，<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);">每次完成复杂任务后，Hermes不会简单地丢弃对话历史，而是会启动一个“复盘”流程。它会回过头来审视整个执行轨迹，提取其中的关键步骤，特别是那些“踩过的坑”、有效的纠错手段以及人工验证过的最佳实践。</font>

<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);"></font>

<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);">随后，系统将这套经验总结、抽象为一个结构化的Skill技能文件包。这就带来了一个根本性的转变：Skill 从“静态调用”变成了“动态生成”。</font>

<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);"></font>

<font style="color:rgb(37, 39, 42);background-color:rgba(255, 255, 255, 0.2);">总结一下：</font>**Skill 自进化是指 AI Agent 能够在执行任务的过程中自动创建新的技能，并在后续使用中持续改进这些技能的能力。**

****

Skill的自进化有两种触发时机，一种是自动触发，一种是后台审查触发。



+ 自<font style="color:rgb(20, 20, 20);background-color:rgba(255, 255, 255, 0.2);">动触发完全依赖 </font>**LLM 的自主决策**<font style="color:rgb(20, 20, 20);background-color:rgba(255, 255, 255, 0.2);">。通过在系统提示中植入指导文本，让 LLM 自己判断何时应该创建或更新 Skill。</font>
+ <font style="color:rgb(20, 20, 20);background-color:rgba(255, 255, 255, 0.2);">后台审查机制的触发，即系统跟踪工具调用次数，达到阈值后自动启动后台审查，无需 LLM 主动决策。</font>



> 更新: 2026-04-18 13:58:17  
> 原文: <https://www.yuque.com/hollis666/aw7b67/xqpailrh56a9g9vo>