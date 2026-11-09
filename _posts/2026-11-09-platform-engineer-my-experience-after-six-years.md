---
title: Platform Engineer my experience after six years
---

Hi!

This is my first, and maybe the last, blog post I'll write to share my experience and tips as a platform engineer.

## Why did I wait until now?

First, because I never really considered myself experienced enough to have much to share. Second, it has been a year since many of us started using AI agents at work, and seeing how fast things are progressing, I wonder how much longer people will bother reading things by themselves. And lastly, LLMs are still really bad at writing somehow, so let me try writing something myself once!

## Who am I?

I am Lim Kevin Chao (Lim Kevin is my first name, in case you were wondering), a French guy who discovered DevOps shortly after graduation and quickly became interested in the field. I was always curious about how the big guys managed to ship software at that scale. Since then, I’ve spent the last six years working in platform teams at several fintech companies in Sweden.

## So what’s a platform engineer in the first place?

That’s a tricky question, as the responsibilities can vary from one company to another. So let me share my own definition based on my experience.

I am a software developer (I am probably bad at that part…) working on one product: the platform that all developers use to ship their products. Think of it like an internal SaaS but without the shiny dashboard.

The goal is to deliver a reliable platform where developers can ship without having to think about everything else (e.g. how to deploy their services or how collect metrics). And just like any SaaS, you need to guarantee the security of the platform, provide proper access management, and continuously deliver new features.

## How to communicate with developers

I think we all agree that communication is key in most jobs, and ours is no exception. But lucky you, you have the best customers in the world!

Why? Because your customers are developers from your own company. You can ping them on Slack anytime, have a quick chat at their desks. And even better, they know what it takes to build and maintain software.

If there’s one thing I’m proud of, it’s the good relationships I’ve built with developers at every company I’ve worked for. And I’m not talking about socializing (I’m actually quite shy…), but rather the everyday interactions on Slack, discussions about features, and most importantly, making them trust my team. I think two things have helped me achieve this:

- Have a dedicated Slack channel for developers. Use it for support, feedback, and any platform discussions. Treat that channel as a top priority. Avoid private support requests whenever possible. Knowledge sharing is important, and that's why you have that channel, so others can find answers or participate.

- Get to know the technical leaders of each team. Find out who makes architectural decisions and defines development standards. You want to be involved in architecture discussions early, not just when they need something from your team.

## Share knowledge, don’t become a bottleneck

There’s a good chance your team is understaffed, and you will lead most of your projects on your own. In theory you don’t really need to interact with your teammates especially now that you can discuss things with your AI agent for as long as you want. But that doesn't mean you shouldn’t discuss your work with the rest of your team.

So make sure to discuss architecture decisions with your teammates. First it will make your work easier to review but more importantly thats one of the most interesting parts of the job! Sorry talking with an AI is still not as satisfying…

Share what you've investigated and why you think your approach is the best way forward.
Let your peers challenge your ideas, you might realize your initial idea was a bit naive. And make sure to do the same for their projects. Be proactive and stay curious about what everyone else is working on.

You should absolutely avoid the situation where dev A is the telemetry expert because he is the one who worked on it, and dev B is the go-to person for CI/CD because he recently revamped it. Everyone on the team should be able to provide support for any part of the platform and work on future features.

First, you'll realize it's boring to work on only one part of the platform. And second, you don't want to be called during your vacation because you're the only one who knows how something works. Yes you may not feel irreplaceable anymore, but there are plenty of other ways to show your value.

## Some tips to finish…

I wanted to end the post here, but it felt a bit silly after saying communication is only half the job so here are a few technical decisions that have made my work easier.

### Infrastracture code in a single repository

Having a single repository for all of our infrastructure code has been the best decision we’ve made, especially now with AI agents. “Ask Claude” just works with all the context in one place.

### Have metrics on your logging pipeline

How many times have I heard dev say, “Something is wrong with the logs I can’t see them” only to find out something broke. So stop letting services sending directly logs to your logging platform. Use a collector, monitor it. Now I have a dog barking at me instead.

### One base image for for everyone

Use the same base image for all services running the same language. If you are also in charge of the security, you will appreciate being able to fix vulnerabilities across multiple services by updating a single image.

### Migration away from legacy system you will not regret

You know what’s fun? Thinking about systems and design. And what better opportunity to do that than sunsetting old legacy systems that are a pain to maintain? Yes, it can be scary and painful, but in my experience, it is always worth it in the long term. That’s why it’s so important to build relationships with the devs who will help you through the migration. It’s also a great opportunity for new joiners to get familiar with the platform, as it forces them to explore parts of the system they might otherwise avoid touching.

---

Thanks for making it all the way to the end! I hope I didn’t waste too much of your time.
If you have any questions or just want to have a casual chat, feel free to reach out to me on LinkedIn.
