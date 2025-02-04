<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [Smart-AskLLM 提问LLM的智慧](#smart-askllm-%E6%8F%90%E9%97%AEllm%E7%9A%84%E6%99%BA%E6%85%A7)
  - [声明](#%E5%A3%B0%E6%98%8E)
  - [简介](#%E7%AE%80%E4%BB%8B)
  - [在提问之前](#%E5%9C%A8%E6%8F%90%E9%97%AE%E4%B9%8B%E5%89%8D)
  - [当你提问时](#%E5%BD%93%E4%BD%A0%E6%8F%90%E9%97%AE%E6%97%B6)
    - [谨慎选择提问的模型和场景](#%E8%B0%A8%E6%85%8E%E9%80%89%E6%8B%A9%E6%8F%90%E9%97%AE%E7%9A%84%E6%A8%A1%E5%9E%8B%E5%92%8C%E5%9C%BA%E6%99%AF)
    - [选择合适的AI助手和问题方向](#%E9%80%89%E6%8B%A9%E5%90%88%E9%80%82%E7%9A%84ai%E5%8A%A9%E6%89%8B%E5%92%8C%E9%97%AE%E9%A2%98%E6%96%B9%E5%90%91)
    - [专业模型和对话平台](#%E4%B8%93%E4%B8%9A%E6%A8%A1%E5%9E%8B%E5%92%8C%E5%AF%B9%E8%AF%9D%E5%B9%B3%E5%8F%B0)
    - [第二步，向多个模型交叉提问](#%E7%AC%AC%E4%BA%8C%E6%AD%A5%E5%90%91%E5%A4%9A%E4%B8%AA%E6%A8%A1%E5%9E%8B%E4%BA%A4%E5%8F%89%E6%8F%90%E9%97%AE)
    - [设定清晰的起手式：提示词与角色定位](#%E8%AE%BE%E5%AE%9A%E6%B8%85%E6%99%B0%E7%9A%84%E8%B5%B7%E6%89%8B%E5%BC%8F%E6%8F%90%E7%A4%BA%E8%AF%8D%E4%B8%8E%E8%A7%92%E8%89%B2%E5%AE%9A%E4%BD%8D)
    - [设定清晰的回复格式和中间过程要求](#%E8%AE%BE%E5%AE%9A%E6%B8%85%E6%99%B0%E7%9A%84%E5%9B%9E%E5%A4%8D%E6%A0%BC%E5%BC%8F%E5%92%8C%E4%B8%AD%E9%97%B4%E8%BF%87%E7%A8%8B%E8%A6%81%E6%B1%82)
    - [使用清晰、规范、精确的提示词表达](#%E4%BD%BF%E7%94%A8%E6%B8%85%E6%99%B0%E8%A7%84%E8%8C%83%E7%B2%BE%E7%A1%AE%E7%9A%84%E6%8F%90%E7%A4%BA%E8%AF%8D%E8%A1%A8%E8%BE%BE)
    - [为LLMs准备易于处理的输入格式](#%E4%B8%BAllms%E5%87%86%E5%A4%87%E6%98%93%E4%BA%8E%E5%A4%84%E7%90%86%E7%9A%84%E8%BE%93%E5%85%A5%E6%A0%BC%E5%BC%8F)
    - [精确地描述问题并言之有物](#%E7%B2%BE%E7%A1%AE%E5%9C%B0%E6%8F%8F%E8%BF%B0%E9%97%AE%E9%A2%98%E5%B9%B6%E8%A8%80%E4%B9%8B%E6%9C%89%E7%89%A9)
    - [话不在多而在精](#%E8%AF%9D%E4%B8%8D%E5%9C%A8%E5%A4%9A%E8%80%8C%E5%9C%A8%E7%B2%BE)
    - [描述问题症状而非你的猜测](#%E6%8F%8F%E8%BF%B0%E9%97%AE%E9%A2%98%E7%97%87%E7%8A%B6%E8%80%8C%E9%9D%9E%E4%BD%A0%E7%9A%84%E7%8C%9C%E6%B5%8B)
    - [别动辄声称找到Bug](#%E5%88%AB%E5%8A%A8%E8%BE%84%E5%A3%B0%E7%A7%B0%E6%89%BE%E5%88%B0bug)
    - [按逻辑顺序提供完整上下文](#%E6%8C%89%E9%80%BB%E8%BE%91%E9%A1%BA%E5%BA%8F%E6%8F%90%E4%BE%9B%E5%AE%8C%E6%95%B4%E4%B8%8A%E4%B8%8B%E6%96%87)
    - [描述目标而非固定方案](#%E6%8F%8F%E8%BF%B0%E7%9B%AE%E6%A0%87%E8%80%8C%E9%9D%9E%E5%9B%BA%E5%AE%9A%E6%96%B9%E6%A1%88)
    - [询问代码相关问题](#%E8%AF%A2%E9%97%AE%E4%BB%A3%E7%A0%81%E7%9B%B8%E5%85%B3%E9%97%AE%E9%A2%98)
    - [关于学习任务的问题](#%E5%85%B3%E4%BA%8E%E5%AD%A6%E4%B9%A0%E4%BB%BB%E5%8A%A1%E7%9A%84%E9%97%AE%E9%A2%98)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Smart-AskLLM 提问LLM的智慧

**How To Ask Questions The Smart Way**

Copyright © 2001, 2006, 2014 Eric S. Raymond, Rick Moen

本指南英文版版權為 Eric S. Raymond, Rick Moen 所有。

原文網址 (Translated from)：[http://www.catb.org/~esr/faqs/smart-questions.html](http://www.catb.org/~esr/faqs/smart-questions.html)

Copyleft 2001 by D.H.Grand(nOBODY/Ginux), 2010 by Gasolin, 2015-present by [Ryan Wu](https://github.com/ryanhanwu)

本中文指南是基于原文 3.10 版以及 2010 年由 [Gasolin](https://github.com/gasolin) 所翻译版本，配以 prompt.md 的提示词，由 Claude-3.5-Sonnet 改写后人工校对和优化的版本。

## 声明

**本指南仅教导如何更好地与LLM交互，而非解决具体专业问题的技术指南！**

我们已经看到太多人误解本指南的目的：有人认为掌握了提问技巧就等同于获得了专业知识，或者认为LLM可以解决所有问题。这种认知是错误的。

如果你阅读本指南后认为作者能直接解答你的专业问题，那你就误解了本指南的目的。本指南旨在教你如何有效地与LLM交互，从而更好地利用它来解决问题。但请记住：LLM只是一个工具，它有其固有的局限性。对于专业问题，你仍然需要咨询相关领域的专家。

LLM可能会产生幻觉，可能会给出错误信息，也可能对特定领域知识的理解存在偏差。本指南的目的是帮助你规避这些陷阱，更有效地利用LLM，而不是替代专业知识或专家建议。

## 简介

在与LLM的对话中,你所获得的答案质量很大程度上取决于你提问的方式。本指南将教你如何正确地向LLM提问以获得最有价值的答案。

现在LLM已经变得越来越强大和普及,任何人都可以通过它们获取知识和解决问题,这是件**好事**。不过要注意的是,尽管LLM被设计得很友好,但获得真正有价值的答案仍然需要恰当的提问方式。

首先你应该明白,LLM最擅长处理明确、结构化且富有挑战性的问题。如果你的问题模糊不清或过于简单,往往得不到理想的答案。好的问题能够帮助LLM更好地理解你的需求,从而提供更有针对性的解答。一个精心构思的问题往往能带来超出预期的洞见。

尽管LLM会尽力回答各种问题,但它们在面对含糊、重复或没有思考过的问题时,往往只能给出浅显或模糊的答案。这不是因为它们傲慢,而是受限于其回答问题的基本原理。

我们不建议那些不愿思考就随意提问的方式。这样不仅浪费了与LLM交互的机会,也无法获得真正有价值的答案。要知道,LLM虽然强大,但它需要清晰的输入才能给出有价值的输出。

我们理解很多人使用LLM只是想快速解决问题,对其技术细节并不感兴趣。对大多数人而言,LLM只是种工具,是达到目的的手段。这完全可以理解。但如果想获得真正有价值的帮助,你仍然需要学会正确地提问。

如果你想更好地使用LLM,就需要表现出积极思考、善于观察、乐于探索的特质。如果做不到这一点,那么与其反复尝试失败的对话,不如寻求其他更基础的帮助渠道。

提出一个好问题的最佳方式是:思路清晰、目标明确、结构合理,并展示出你对问题已经有了一定的思考。这样不仅能帮助LLM更好地理解你的需求,也能获得更有价值的答案。

## 在提问之前

在你准备向LLM提出问题前，请先做到以下事情：

1. 尝试将你的问题分解成更小的、明确的部分。
2. 检查问题是否在LLM的知识范围内（考虑知识截止日期）。
3. 尝试收集和整理相关的背景信息。
4. 思考如何清晰地表达你的需求和目标。
5. 准备必要的上下文信息。
6. 考虑是否需要提供具体的例子。
7. 检查你的问题是否可能涉及LLM的已知局限性。

当你提出问题时，最好能说明你已经做了哪些准备工作；这有助于获得更精准的回答。如果你能展示出对问题的初步理解和尝试过的方法会更好，因为这样可以帮助LLM更好地理解你的思维过程和需求。

在与LLM对话时，采用以下策略会很有帮助：
- 从简单明确的问题开始，逐步深入
- 提供清晰的上下文和具体例子
- 说明你期望的回答格式或详细程度
- 在需要时及时提供反馈和澄清

不要期望一次简单的提问就能解决复杂的问题。对于复杂问题，最好将其分解成多个步骤，并在每个步骤中与LLM进行有效互动。花时间组织你的思路和问题，因为问题的质量直接影响答案的质量。

准备问题时要注意避免：
- 含糊不清的表述
- 过于宽泛的问题
- 缺乏必要上下文
- 不合理的预设

记住，与LLM的对话质量取决于你提供的信息质量。通过提出有思考、结构清晰的问题，你更可能获得有价值的答案。好的问题应该：
- 目标明确
- 背景充分
- 逻辑清晰
- 便于理解和回答

如果你不确定如何改进问题，可以先请LLM帮你完善问题的表述。通过"这个问题如何表达更清楚？"或"还需要提供什么信息？"这样的引导，你可以逐步优化你的提问方式。

## 当你提问时

### 谨慎选择提问的模型和场景

小心选择你要提问的对象和场景。如果你做了下述的事情，你很可能得到无效或误导性的回答：向不具备相关知识的模型提问专业问题，向专注于特定领域的AI助手询问不相关的问题，在单次对话中反复提出同样的问题而不做改进，或者期待模型能够处理超出其能力范围的任务。

因此，第一步是选择合适的模型或AI助手。不同的模型有不同的专长和知识范围：有的擅长编程，有的专注于创意写作，还有的专门用于特定领域的分析。在提问之前，先了解你所使用的模型的特点和局限性。例如，如果你需要最新的市场数据，单纯依赖具有知识截止日期的语言模型可能无法满足你的需求。

向AI提问最重要的是构建有效的对话场景。这意味着你需要提供足够的上下文，使用清晰的表达，并且准确描述你的需求。不要假设模型能理解所有隐含的背景信息，即使是看似简单的问题，有时也需要你提供必要的补充说明。

在选择如何组织你的提问时，要考虑到AI模型的工作方式。它们更容易处理结构清晰、逻辑连贯的问题。如果你的问题很复杂，最好先确认模型是否理解你的问题要点，必要时进行拆分或重述。不要把所有问题一次性抛出，而是要循序渐进地推进对话。

谨记，AI模型虽然强大，但它们并非万能。它们不能替代专业顾问的建议，也不能处理需要实时信息或个人判断的问题。如果你不确定某个模型是否适合回答你的问题，最好先用一些简单的测试问题来了解它的能力范围。

一般来说，在通用对话中先进行初步探索，然后再根据需要转向更专业的模型或工具，这样的策略会更有成效。这不仅能帮助你更好地利用AI的能力，还能避免在错误的场景下浪费时间。

### 选择合适的AI助手和问题方向

在求助AI之前，先尽可能地在现有知识库和论坛中搜索。就像当年的Stack Exchange社区一样，现在已经有许多专门收集AI交互案例的平台，你的问题很可能已经有人问过并得到了不错的答案。

因为搜索引擎会索引这些平台的内容，在直接向AI提问之前先搜索往往能节省时间。有很大可能其他人已经遇到了类似的问题，而且已经总结出了有效的提问方式和解决方案。如果搜索无果，再考虑如何构建你的问题。

在选择和使用AI模型时要注意以下几点：

不同的AI模型有不同的特点和专长。选择合适的模型很重要 - 有的更擅长编程，有的更适合创意写作，有的专门用于特定领域分析。了解不同模型的能力边界，可以帮助你更快得到有效答案。

当你开始提问时，确保使用清晰的表述，并提供必要的上下文。尤其是在讨论技术问题时，示例代码和具体场景描述往往能帮助AI更好地理解你的需求。如果AI要求你提供更多信息，最好能完善你最初的问题描述，而不是零散地补充。

AI交互中一个重要的反馈机制是：如果一个回答对你有帮助，你可以明确指出这一点，这有助于改进后续对话。如果答案没有完全解决问题，也要说明具体哪些方面仍需要澄清或补充。

就像我们要根据问题类型选择合适的Stack Exchange子站一样，面对不同类型的问题，也需要采用不同的提问策略：

- 对于通用型问题，可以直接使用简单直接的表述
- 对于编程相关的问题，要注意提供完整的上下文和代码示例
- 对于专业领域的问题，最好先说明你的背景知识水平

### 专业模型和对话平台

为特定领域和任务准备的AI模型和平台正在不断涌现，它们往往对特定类型的问题有更好的理解和解答能力。特别是当你遇到相对基础或领域特定的问题时，选择合适的专业模型可能会比通用模型得到更好的答案。许多专业平台还提供了经过优化的提示词和最佳实践指南。

实际上，如果你遇到的问题与特定领域或工具有关（这很常见），最好先使用该领域的专业模型。比如编程问题使用经过代码训练的模型，创意写作使用专门的写作助手。这样往往能得到更准确和实用的回答，而不是通用模型可能给出的笼统建议。

在开始对话之前，先花点时间了解所选模型的特点和使用方式。了解它擅长什么，有什么限制，这些信息通常可以在模型的说明文档中找到。即使你之前使用过其他AI模型，不同模型之间可能存在显著差异，值得事先了解。

目前AI辅助交流正在快速发展，倾向于提供更即时和交互式的帮助。不过对于某些深度专业问题，可能还是需要寻求人类专家的帮助。所以要根据问题的性质选择合适的求助方式。

在进行AI对话时，建议从简短清晰的问题描述开始。不要一次性抛出太多信息，而是通过渐进式的对话来逐步深入。这样不仅能让AI更好地理解你的需求，也便于你及时调整提问方向。

### 第二步，向多个模型交叉提问

当你遇到重要问题时，最好向多个不同的AI模型提问，而不是仅依赖单一模型，即使你认为某个模型最擅长回答这类问题。查看每个模型的特点和局限性，合理利用它们的优势。这样做有几个重要理由：

任何值得深入探讨的问题，通常都能从不同模型的视角中获益。每个模型由于训练数据和方法的差异，往往会关注问题的不同方面。交叉验证这些答案，能帮助你获得更全面的认识。

向多个模型提问可以互补各自的不足。即使是最先进的模型也可能在某些方面有偏差或局限，通过对比不同答案，你能更好地识别这些局限性。

当你收集到不同模型的回答时，可以对比它们的异同。如果多个模型给出相似的答案，这往往说明这个答案更可靠；如果出现分歧，这些差异本身就很有研究价值。

通过对比不同模型的回答质量，你能逐渐建立起对各个模型特点的认识。这些经验将帮助你在未来更好地选择合适的工具。

如果你发现某个问题得到的答案差异很大，不妨将这种差异作为新的提问点。理解为什么会出现这些差异，往往能带来更深的洞察。

在实践中，你可以先向最熟悉的模型提问，然后用相同的问题去请教其他模型。记录和对比这些回答，关注它们的侧重点和表达方式的不同。这个过程虽然花费更多时间，但获得的收益往往超出预期。

不要局限于自己最喜欢的那个模型。每个模型都有其独特的训练背景和专长领域，多方印证不仅能得到更可靠的答案，也能帮助你建立对AI能力的更清晰认识。

### 设定清晰的起手式：提示词与角色定位

与AI交谈时，你的第一句话决定了整个对话的基调和效果。这个"起手式"应该包含两个关键要素：明确的问题描述和恰当的角色设定。这样的组合能帮助AI更准确地理解你的需求，并从最合适的专业视角来回应。

一个优秀的起手式应该遵循"场景-角色-目标"的结构：
- 场景：说明问题的具体环境和背景
- 角色：设定AI应该以什么样的专业身份回应
- 目标：描述你期望获得的具体帮助

> 低效提示：帮我看看这个机器学习的问题。

> 有效提示：以机器学习工程师的身份，分析这个图像分类模型在4GB显存环境下的性能问题。

> 更优提示：请以有5年计算机视觉经验的ML工程师视角，分析在RTX 3060（4GB显存）环境下，ResNet50模型处理1080p图像时的内存溢出问题 - 重点关注批处理大小和模型优化方案。

构建这样的起手式能帮助你：
1. 明确上下文：具体的技术环境和限制
2. 确定视角：需要什么样的专业知识
3. 界定范围：问题的具体边界在哪里
4. 指明方向：期望得到的解决方案类型

当你预计要讨论一系列相关问题时，好的角色设定尤其重要。例如：

```
请以一位精通微服务架构的高级后端工程师身份，帮我分析一个电商系统的设计方案。这个系统预计日订单量10万，需要考虑：
- 订单处理服务的分片策略
- 支付系统的高可用设计
- 库存系统的并发控制
```

在持续对话中，你可以：
- 保持角色一致性，深入专业讨论
- 在需要时请求切换视角（如从开发者转向架构师）
- 适时补充或调整场景信息

对于复杂问题，可以设计多轮交互：
1. 首轮以技术专家视角分析可行性
2. 再以性能工程师角度评估瓶颈
3. 最后用项目经理视角考虑实施计划

记住：好的起手式不仅是问题描述，更是一个专业对话的基础设定。它能帮助AI提供更有针对性和深度的回答，也让后续的交流更加顺畅和高效。

### 设定清晰的回复格式和中间过程要求

与AI对话时，明确指定你期望的回复格式和中间推理过程能显著提升回答质量。这就像给AI一个"思考模板"，帮助它更系统地分析和表达。

一个好的格式要求应该包含以下要素：
1. 输出格式（如Markdown、JSON、HTML等）
2. 推理过程的展示方式
3. 特定的结构要求

> 低效提示：分析一下这段代码的性能问题。

> 有效提示：请用Markdown格式分析这段代码，包含：
> - 时间复杂度分析
> - 空间使用评估
> - 具体的优化建议

> 更优提示：分析这段排序算法，要求：
> 1. 用JSON格式回复，包含"complexity"、"memory"、"bottleneck"、"suggestions"字段
> 2. 在分析过程中展示关键步骤的时间复杂度计算
> 3. 每个优化建议需包含预期改进效果
> ```json
> {
>   "complexity": {"best": "O(?)", "average": "O(?)", "worst": "O(?)"},
>   "memory": {"space": "O(?)", "auxiliary": "O(?)"},
>   "bottleneck": ["步骤1", "步骤2"],
>   "suggestions": [{"change": "", "impact": "", "tradeoff": ""}]
> }
> ```

要求展示中间过程的好处：
1. 帮助验证AI的推理逻辑是否正确
2. 发现潜在的思维盲点
3. 获得更多洞察和学习机会
4. 便于后续优化和调整

对于不同类型的问题，可以这样设计格式要求：

数学问题：
```
请展示完整推导过程：
1. 关键步骤和对应公式
2. 每步的简化说明
3. 最终结论
```

代码审查：
```
分析维度：
- 代码正确性（附带测试用例）
- 性能分析（含复杂度）
- 可维护性评分（1-5）
- 具体改进建议
```

系统设计：
```html
<analysis>
  <requirements>...具体要求...</requirements>
  <constraints>...限制条件...</constraints>
  <design>...设计方案...</design>
  <tradeoffs>...权衡分析...</tradeoffs>
</analysis>
```

在持续对话中，你可以：
- 根据AI的回复调整格式要求
- 要求保持一致的分析框架
- 针对特定环节要求更详细的展开

记住：
1. 格式要求要与问题复杂度匹配
2. 关键步骤的展示有助于理解和验证
3. 统一的格式便于比较和积累经验
4. 适当的结构化有助于后续引用和扩展

### 使用清晰、规范、精确的提示词表达

与LLM对话时，清晰且规范的表达不仅是礼貌，更能帮助LLM更准确地理解和回应你的需求。虽然LLM能处理各种输入，但高质量的提示词往往能得到更好的回答。

一个好的提示词表达应该：
1. 使用规范的语言和标点
2. 结构清晰有序
3. 术语准确无歧义
4. 适当提供上下文

> 不规范示例：帮我看看这段代码哪出问题了thx！！！

> 规范示例：此段代码在处理大量数据时出现性能瓶颈，请帮我分析可能的原因。

> 更优示例：以下Python代码在处理超过1GB CSV文件时CPU使用率异常高：
```python
[代码段]
```
期望：
1. 找出性能瓶颈
2. 提供优化建议
3. 分析优化后的预期效果

跨语言交流时的处理：

如果你使用非英语与AI交流，可以：
1. 明确说明你的语言偏好
2. 对专业术语提供双语参考
3. 要求AI用特定语言回复

```
偏好：请用中文回复
术语参考：
- 时间复杂度 / Time Complexity
- 内存泄漏 / Memory Leak
- 并发控制 / Concurrency Control
```

使用多语言时的最佳实践：
- 关键术语同时提供多语言版本
- 明确指定期望的回复语言
- 在需要时要求解释特定术语

代码相关问题的表达方式：
```
环境信息：
- 运行环境：Python 3.8
- 操作系统：Ubuntu 20.04
- 相关依赖：numpy 1.19.2

问题描述：
[清晰描述问题]

复现步骤：
1. [具体步骤]
2. [具体步骤]

期望结果：
[明确说明期望]

实际结果：
[实际情况]
```

系统设计问题的表达方式：
```
背景：[项目背景]
需求：[具体需求]
约束：
- 性能要求
- 可用资源
- 其他限制

期望输出：
1. 整体架构
2. 关键组件
3. 数据流设计
```

记住：
1. 使用正确的专业术语
2. 提供充分的上下文
3. 结构化组织信息
4. 明确表达期望

### 为LLMs准备易于处理的输入格式

当你向LLMs提问时，合适的输入格式不仅能提升回答质量，还能帮助它更准确理解上下文。以下是一些核心准则：

#### 1. 文本内容清理
* 使用纯文本格式而不是富文本或HTML
* 去除多余的格式标记和样式信息
* 保持段落结构清晰，使用一致的缩进
* 避免特殊字符和非标准编码

#### 2. 结构化信息组织
* 将长文档分割成合适的片段
* 保留原始的层级结构和关系
* 使用统一的标题和分隔符标记
* 突出重要的信息和关键词

如果要分享外部链接内容，应该：
```
# 选择性提取关键内容
原文：[长文档]
处理后：
- 移除导航栏、广告等干扰内容
- 提取核心段落和要点
- 保持原文的结构和逻辑
- 标记重要的引用和数据

# 提供清晰的引用格式
来源：[原始链接]
时间：[发布/更新时间]
作者：[如果有]
主题：[文档主题]
```

#### 3. 代码和技术内容
* 使用标准的代码块标记
* 保持代码的缩进和格式
* 提供必要的注释和说明
* 包含相关的环境信息和上下文

#### 4. 错误信息和日志
* 保持原始的时间戳和格式
* 突出关键的错误信息
* 包含必要的上下文信息
* 去除重复和无关的部分

记住：
- 输入的质量直接影响输出的质量
- 保持格式的一致性和标准化
- 提供充分但不冗余的上下文
- 突出问题的关键点和核心内容

这种预处理不仅有助于LLMs更好地理解和处理信息，也能帮助获得更准确和有用的回答。就像给LLMs提供一个整洁有序的工作环境，而不是杂乱的原始资料。

### 精确地描述问题并言之有物

当你在向LLMs提问时，问题的描述质量直接决定了回答的质量。一个好的问题应该包含以下要素：

* 仔细、清楚地描述问题或异常的具体表现，包括完整的错误信息。

* 提供足够的环境上下文，例如：
  - 系统配置和版本（如：Fedora Core 4、Slackware 9.1）
  - 相关软件的版本信息
  - 重要的配置项和设置
  - 最近的环境变更

* 说明你已经做过的研究和尝试：
  - 查阅过的文档或资料
  - 尝试过的解决方案
  - 为什么这些方案不能解决问题
  - 关键的排查步骤和结果

* 提供完整的问题复现方法：
  - 详细的操作步骤
  - 必要的测试数据
  - 最小化的测试用例
  - 触发问题的具体条件

尽量预想LLMs可能需要的补充信息，在提问时就主动提供。当你提供的是代码相关的问题时，一个可以稳定复现的环境尤其重要 - 这能显著提高获得有效回答的概率和速度。

最重要的是，在描述问题时要客观具体，避免主观臆测。好的问题描述应该让LLMs能清楚地理解：问题是什么，在什么条件下发生，以及你期望得到什么样的帮助。

### 话不在多而在精

你需要提供精确有内容的信息。这并不是要求你简单地把成堆的出错代码或资料完全转录到提问中。如果你有庞大而复杂的测试样例能重现问题，尽量将它剪裁得越小越好。

这样做的用处至少有三点。第一，表现出你为简化问题付出了努力，这可以使你得到回答的机会增加；第二，简化问题使你更有可能得到**有用**的答案；第三，在精炼问题的过程中，你很可能就自己找到了解决方法或权宜之计。

### 描述问题症状而非你的猜测

告诉LLMs你认为问题是怎样造成的并没什么帮助（如果你的推断如此有效，还用向别人求助吗？）。要确信你原原本本告诉了它们问题的症状，而不是你的解释和理论；让LLMs来推测和诊断。如果你认为陈述自己的猜测很重要，清楚地说明这只是你的猜测，并描述为什么它们不起作用。

**蠢问题**
> 我的程序一直报内存错误，我觉得可能是某个指针没有初始化，要怎么找出来？

**聪明问题**
> 我正在用C++开发一个图像处理程序（完整源码在此），在处理大于2MB的图片时会出现段错误。这个错误在以下三种情况下必现：
> 1. 图片大小超过2MB
> 2. 色彩深度为32位
> 3. 使用了双重循环处理像素
> 
> 错误日志如下...

所有的诊断专家都遵循"让我看看"的原则。这并不是一种怀疑，而是一种真实而有用的需求，以便让他们看到的是与你看到的原始证据尽可能一致的东西，而不是你的猜测与归纳的结论。所以，大方地展示给我们看吧！

### 别动辄声称找到Bug

当你在使用软件中遇到问题，除非你非常、**非常**的有根据，不要动辄声称找到了Bug。提示：除非你能提供解决问题的源代码补丁，或者提供回归测试来表明前一版本中行为不正确，否则你都多半不够完全确信。

编写软件的人总是非常辛苦地使它尽可能完美。如果你声称找到了Bug，也就是在质疑他们的能力，即使你是对的，也有可能会冒犯到其中某部分人。提问时，即使你私下非常确信已经发现一个真正的Bug，最好写得像是**你**做错了什么。如果真的有Bug，你会在回复中看到这点。

### 按逻辑顺序提供完整上下文

要获得最准确的回答，请提供完整的对话背景和尝试过程。包括：
- 之前的相关对话内容
- 您使用的具体提示词
- LLM的响应
- 问题出现的具体环境（如使用的模型、温度设置等）

在使用高级功能时（如配置详细程度、角色设定等），请说明您使用的具体设置。记住，`详尽`不等于`有效`。选择合适的细节层级，提供有价值的信息而不是无关细节。

如果您的问题背景较长（超过四个段落），建议先简要说明核心问题，再详细展开上下文。这样可以帮助LLM更好地理解需要关注的重点。

### 描述目标而非固定方案

当您寻求解决方案时，先说明最终目标，再描述当前受阻的具体步骤。很多使用者会固守某个特定方案，而没有意识到可能存在更好的解决途径。

**低效提问**
> 怎样让Claude在回答时使用表格格式？

**有效提问**
> 我需要将数据整理成易于比较的格式。我尝试让Claude使用表格输出，但不确定这是否是最佳方案。
> 我的数据包括产品名称、价格和评分，需要方便地进行横向对比。

第二种提问方式更可能得到更有价值的建议，比如使用其他数据可视化方式或更适合的数据组织形式。

### 询问代码相关问题

向LLM提出代码问题时，不必像对人类那样谨慎。实际上，直接提供完整的问题代码，然后说明"这段代码运行不了"往往也能得到有效回应。这是因为LLM能够快速分析整块代码，找出潜在问题。不过，提供更多上下文和细节仍然有助于获得更精准的答案。

比如，你可以这样描述："这是一个用Python写的网页爬虫程序，在运行时报错。这是完整代码和错误信息。我觉得可能是请求头设置有问题，但不确定。"这样的提问既保留了完整信息，又提供了你的初步判断。

当然，如果你能定位到具体的问题区域，提供最小复现代码仍然是更好的做法。这不仅能让LLM更专注于核心问题，也能帮助你自己更好地理解代码结构。例如："这段处理用户输入的函数在输入特殊字符时会崩溃，我简化后的测试代码如下..."

如果你想让LLM帮你审查代码，直接说明你的需求即可。像这样："请帮我检查这段代码的安全性，特别是用户输入验证部分。"LLM会根据你的要求进行针对性分析。

### 关于学习任务的问题

在处理学习任务时，LLM可以成为你的得力助手，但前提是要正确使用它。与传统的"不要问家庭作业"的建议不同，你完全可以向LLM请教学习相关的问题，因为这是个提升学习效果的好机会。

关键在于如何提问。不要简单地要求答案，而是展示你的思考过程："我在解这道微积分题，已经试过用分部积分法，但卡在这一步。我的推导过程是这样的..."这样不仅能得到针对性指导，还能加深你对问题的理解。

LLM特别适合解释概念和原理。当你遇到不懂的知识点时，可以要求它从不同角度解释，或者通过类比来帮助理解。它也可以提供额外的练习题，帮你巩固所学内容。

记住，LLM是学习的辅助工具，而不是答案机器。明智地使用它，让它帮助你建立更深入的理解，而不是简单地完成任务。
