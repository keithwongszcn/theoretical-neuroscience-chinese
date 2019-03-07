# Preface

为了研究神经系统**做了什么**，确认它的**如何**运作和理解它**为什么**以这样一种特殊的方式运作，理论分析和计算建模是非常重要的工具。从分子细胞的研究，到对人类精神物理学和心理学的探索，都是神经科学的研究手段。计算神经科学鼓励这些子学科的相互交流，期望从已有的知识中构建起简洁的体系，在不同的描述水平之间建立联系，确立统一的概念和原则。

做了什么，如何运作和为什么这样运作这三个问题分别对应于：描述模型(descriptive model)，机械模型(mechanistic model)和阐释模型(interpretive model)，本书会在接下来的章节中陆续讨论这几个概念。**描述模型**简洁且精准的总结了大量的实验数据，从而找出神经元和神经回路做了什么。这些模型可能对生物物理学、解剖学和生理物理学的发现的拟合度并不高，这是因为它主要的目的不是解释现象，而是描述现象。另一方面，**机械模型**基于解剖学、生理学和电路学对神经系统如何运作做出解释。它经常充当不同层次描述模型之间的桥梁。**阐释模型**使用计算和信息学理论原则，来探索神经系统功能的多种行为和认知的意义所在，针对的问题是神经系统为什么按照一定的模式运作。

针对特定的问题，一个常见的难题是如何将模型定位在相对应的层次，很容易犯提前假设模型需要过多的细节的错误。由于模型是作为不同理解层次之间的纽带，他们必须拥有足够多的细节，去与低层次产生关联，又要足够的简洁，以便与高层次构建出优雅的结果。

### Organization and Approach

根据大致的主题，本书分为三部分。第一部分—神经编码和解码（1-4章）主要讲述由动作电位（action potential）组成的信息编码，与由选择性反应的神经元群所表现出的信息。基于细胞（cell）和突触（synaptic）的生理物理知识，对神经元（neuron）和神经电路（neural circuit）的建模则在第二部分—神经元和神经电路（5-7章）中展示。可塑性（plasticity）在生长和学习中起到的作用在第三部分，适应和学习中（8-10章）予以讨论。第5章和第6章是例外，它们共同描述了神经元建模。这两章是相对独立的，无论是一学期课程还是两学期课程，无论面对的是本科生还是研究生，都可以选择灵活的编排在课程中。

虽然我们提供了一些背景知识，但没有神经科学背景的读者还是应该参考一本神经科学的书籍，如Kandel, Schwartz & Jessell (2000); Nicholls, Martin & Wallace (1992); Bear, Connors & Paradiso (1996); Shepherd (1997); Zigmond, Bloom, Landis & Squire (1998); Purves et al (2000).

计算神经科学建立在一种信念之上，它相信数学、物理和计算机科学方法可以用于解释神经系统的功能。不幸的是，有时数学更多的是阻碍而不是帮助。我们毫不犹豫的用精准和严格的方法来进行分析。有时这会降低一些人的忍耐程度。我们推荐这些读者去参阅数学相关的附录，那里简洁的提供了本书中会用到的多数数学方法，但即使某些步骤不甚清晰，也定要坚持尝试去理解一个复杂推导背后的意义和结论。

计算神经科学，像多数技巧一样，熟能生巧。基于这个目的，我们在网站上（http://mitpress.mit.edu/dayan-abbott）为本书提供了练习题，并希望读者能够物尽其用。最后，如果读者能对文中讨论的那些模型进行深挖，探索它们那些由于篇幅有限而无法在本书中讲述的特性，定是十分有益处的。

### Referencing

为了保持行文的流畅，我们将章节中的注释缩减到了最少。每个章节的末尾都附有作为课外阅读的注解书目(用粗体表示)、关于在文中引用的研究工作的信息和相关研究的参考读物。我们专注于介绍计算神经科学的基础工具，讨论我们认为最能帮助读者理解并赏识这些工具的应用案例。这意味着很多十分成功的应用计算方法的工具都不会在本文中引入。参考书目中的引用会向读者去介绍这些应用。在我们讨论的多数领域，许多人都提供了十分尖锐的见解。在提升阅读类别中的书和文章，会提供更多在本书中憾未引入的研究工作和参考文献。

### Acknowledgments

我们十分感谢大量在Brandeis, the Gatsby Computational Neuroscience Unit 和 MIT 的学生，以及在许多研究机构的同事们，他们对全部章节，难以计数的版本进行了刻苦的研读，提出意见和评价。我们特别感谢Bard Ermentrout, Mark Goldman, John Hertz, Mark Kvale, Zhaoping Li, Eve Marder 和 Read Montague对全书提供的大量的讨论和建议。许多人阅读了大部分文本并提供了宝贵的意见，批评和见解，他们是：Bill Bialek, Pat Churchland, Nathaniel Daw, Dawei Dong, Peter F¨oldi´ak, Fabrizio Gabbiani, Zoubin Ghahramani, Geoff Goodhill, David Heeger, Geoff Hinton, Ken Miller, Phil Nelson, Sacha Nelson, Bruno Olshausen, Mark Plumbley, Alex Pouget, Fred Rieke, John Rinzel, Emilio Salinas, Sebastian Seung, Mike Shadlen, Satinder Singh, Rich Sutton, Nick Swindale, Carl van Vreeswijk, Chris Williams, David Willshaw, Charlie Wilson, Angela Yu, and Rich Zemel。

我们从这些人中收到了大量额外的帮助和建议：Greg DeAngelis, Andy Barto, Matt Beal, Sue Becker, Tony Bell, Paul Bressloff, Emery Brown, Matteo Carandini, Frances Chance, Yang Dan, Kenji Doya, Ed Erwin, John Fitzpatrick, David Foster, Marcus Frean, Ralph Freeman, Enrique Garibay, Frederico Girosi, Charlie Gross, Andreas Herz, Mike Jordan, Sham Kakade, Szabolcs K´ali, Christof Koch, Simon Laughlin, John Lisman, Shawn Lockery, Guy Mayraz, Josh McDermott, Markus Meister, Earl Miller, Quaid Morris, Tony Movshon, Yuko Munakata, Randy O’Reilly, Simon Osindero, Tomaso Poggio, Clay Reid, Max Riesenhuber, Dario Ringach, Horacio Rotstein, Sam Roweis, Lana Rutherford, Ken Sugino, Alexei Samsonovich, Bob Shapley,WolframSchultz, Idan Segev, Terry Sejnowski, Jesper Sj ¨ostr ¨om, Haim Sompolinksy, Fiona Stevens, David Tank, Emo Todorov, Alessandro Treves, Gina Turrigiano, Davi Van Essen, Martin Wainwright, Xiao-Jing Wang, Chris Watkins, Max Welling, Jenny Whiting, MattWilson, LaurenzWiskott, Danny Young, and Kechen Zhang。同样感谢Quentin Huys, Philip Jonkers, Alexander Lerchner, Shih-Chii Liu,M´at´e Lengyel, Alex Loebel,HadiMurr, IainMurray, Jihwan Myung, John van Opstal, David Simon, Ed Snelson, and Rafael Yuste指出文中的错误。

我们感谢Maneesh Sahani

我们对于任何因疏忽而未包含在这份名单中的人致以歉意。Karen Abbott对图表提供了大量的帮助。对于MIT出版社，我们感谢Michael Rutter的耐心和持续的建议，也感谢Sara meirowitz和Larry Cohen在Michael离开后对工作的支持。