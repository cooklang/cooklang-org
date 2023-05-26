---
title: 'AI and the Evolution of Recipe Formats'
date: 2023-05-26T19:27:37+10:00
weight: 100
summary: This text discusses the challenges of translating traditional recipe formats into a structure understandable by computers. It highlights the issues faced by AI in comprehending the sequence of ingredients and cooking steps, and the steps taken to create a new, AI-friendly format. The piece delves into attempts to design a universal tool for recipe importation and conversion, and the issues encountered. It then outlines a new approach using AI to trace ingredients and cooking actions to create a comprehensive recipe graph, leading to an enhanced user experience and potentially revolutionizing the way we engage with recipes.
---

Recipes have been structured in a similar format for a long time; a list of ingredients followed by the steps necessary to create a dish. While this works for human readers, it's less convenient for computers. They struggle to understand when each ingredient is used and what happens in each step. This makes it challenging to design applications that provide step-by-step recipe instructions, let alone enhance the overall cooking process.

To combat this, a new format, Cooklang, was created, in which the text is organized in a straightforward structure and users could tag ingredients and tools as they were mentioned. This allowed the development of applications that could present recipes step by step, create shopping lists, and offer more benefits.

We attempted to create a [universal tool](https://github.com/cooklang/cook-import) that could import any recipe from the web and reformat it into this user-friendly layout. However, it was a difficult task due to the variety of ways people write recipes. For instance, a recipe might introduce a bunch of spices early on and later merely refer to them as "spices", complicating the process of tracking individual ingredients.

Consequently, we opted for a different approach. We proposed utilizing AI/ML assistance to trace the use of ingredients from start to finish. This could provide a clear understanding of when and how each component is used, ultimately leading to the construction of a recipe graph. This graph begins with the ingredients and cookware, following their interactions through the recipe, visualizing the process as it evolves.

Not long ago, people approached me to present their recipes in a more structured format and engage in [discussions](https://github.com/cooklang/spec/discussions/62) about them. The graph format is particularly useful for computers. Check out this informative Twitter thread about different recipe representations:

{{< tweet user="hydrosquall" id="1486157532968148996" >}}

Thus, I wanted to explore the possibility of using GPT-4 to create this graph.

GPT-4 works by responding to user prompts. For instance, you provide an example of the desired output, and it generates similar results. We decided to use this model for entity recognition and to identify relationships between ingredients and cookware.

We examined other projects for inspiration, like [GraphGPT](https://graphgpt.vercel.app), which utilizes direct instructions to prompt the model. Adapting this approach, we had our initial attempt at creating a graph. However, it was less successful in recognizing relationships.

After a few tweaks, we managed to achieve better results. Here's our improved attempt:

{{< gist dubadub 244d3ea113565cae3817d89ebe9101ec>}}

Further fine-tuning allowed us to generate Ruby-compatible syntax for creating a graph image. Here's the result: {{< gist dubadub 9da2fbe493a72e3090fefd9e5123dc45>}}

Notice how the AI smartly creates names for intermediate ingredients.

![](/blog/part-recipe-graph.png)

[Open full graph](/blog/full-recipe-graph.png)


What's next? If this system works effectively, it could revolutionize the way we approach recipe management. It isn't about creating a new language syntax, but rather focusing on improving tools and user experiences. This graph-based approach could easily be integrated into our CLI and mobile applications. This means users won't need to learn any syntax. They can continue writing recipes as they always have, and the computer will extract what it needs, making everyone's lives easier.

-Alexey
