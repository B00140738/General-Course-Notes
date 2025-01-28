
## The Most Important Step: Knowing What (Not) to Study

Have you had a wunderkind classmate back in school who doesn't seem to study very much but always aces the exams? I have. I was jealous of them. I thought they were just naturally smart. I was wrong. They were just better at studying than I was.

Years in the tech industry and entrepreneurship taught me the significance of prioritization. Success often hinges on discerning the essentials from the superfluous. It's not just about studying hard; it's about studying smart. I'd argue that identifying the right study areas is the pivotal step to conquering coding interviews.

Interestingly, knowing what **not** to study is also important. There are many things you can study, but not all of them are useful. For example, you can spend days studying how to implement a complex algorithm like [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform), but that's not going to help you in a coding interview either because it's too complex and academic and nobody expects you to use that during an interview. The pitfall here isn't just the misallocation of time but also the missed opportunities to focus on what truly matters. With a plethora of potential questions and topics expanding daily, it's a race you can't win by sheer volume.

The real interview questions condense to a small set of patterns and mastering these patterns should be the focus of your study.

Hopefully by this point you have read the [Top Pattern Stats](https://algo.monster/problems/stats) article to get an idea of what's useful and what's not. Now let's talk about what interviewers look for in real interviews and how to study the patterns.

## What Interviewers Look For

On the technical side, there are a couple of things interviewers look for:

1. Exceptional problem-solving abilities.
2. Producing bug-free code.

While qualities like communication and culture fit can be polished quickly, honing your technical skills requires dedicated preparation. The essence of problem-solving is to draw from familiar challenges when faced with unfamiliar ones. George Pólya, in his renowned book ["How to solve it"](https://en.wikipedia.org/wiki/How_to_Solve_It), provides valuable pointers like identifying patterns and breaking down complex problems. Meanwhile, the knack for writing flawless code is achieved through relentless practice. On some levels, producing bug-free code is even more important since coding to specs is what you will be expected to do on the job.

## Learn with the "PTS" System

At AlgoMonster, we love systems. We are big believers in [systems over goals](https://bit.ly/3uKFBUd).

Throughout this website, you will see systems for solving common interview patterns. The "PTS" system, short for Patterns-Templates-Speedrun, is our unique strategy:

1. Patterns: Master common patterns
2. Templates: Never make coding mistakes again using our templates for each pattern
3. Speedrun: Expanding your knowledge by going through many problems quickly

### 0. Grasp Elementary Data Structures

This means basic stuff like an array, stack, or linked list. Stuff you'd use in daily programming. If you have any real-life coding experience, you should know these already. Although depending on your understanding, you may have to brush up on how things work behind the scene. We have language-specific data structure overviews to get you started.

### 1. Patterns

There are literally thousands of problems out there on the internet you can practice, which can be overwhelming. The good news is that there are only a handful of common patterns you need to know. Once you master the patterns, you'll be able to apply the techniques to solve other problems.

#### Why mastering the pattern is important

Because we don't know what we don't know, humans can only infer from what we know. If a problem requires prior knowledge and we don't have that knowledge, then it's essentially intractable. This is especially true in a coding interview with limited time. When the pressure comes, we don't usually rise to the occasion. Instead, we fall to our highest preparation.

#### Can't I figure out these patterns myself?

You can. It takes time and experience to solve many problems and figure out patterns. To quote Issac Newton, "if I have seen further, it is by standing on the shoulders of Giants." We've done the leg work for you. And we are constantly updating the content to stay up to date with current interview trends.

![algorithm patterns](https://algo.monster/patterns.png)

Each pattern is broken down into progressive sub-sections that optimize your learning experience. We start with the most basic form of the pattern and gradually introduce more advanced techniques. This way, you can learn the pattern in a systematic way.

### 2. Templates

You need to understand the common patterns well and be able to **code them bug-free**, in 10-15 min during an interview. We distilled the pattern code into [templates](https://algo.monster/templates).

![algorithm templates](https://algo.monster/template.png)

Use the inline editors to practice coding using these templates against test cases. Do this as many times until you can code them bug-free quickly.

### 3. Speedrun

Once you've mastered the patterns and being able to code them correctly, you want to work through many problems and derive mental solutions. This might seem odd at first glance. Shouldn't you code every problem you see? In theory, yes. But we only have so much time in a day. We have our jobs, school work, or even kids to take care of. We don't have time to code every problem out there. And that's OK. After we have mastered step 2, we should be able to look at a problem, identify which pattern it belongs to, and derive a mental solution. By _going through_ as many problems as possible, you save much time and greatly expand your knowledge. This makes it easy for you to figure out the problem type during an actual interview quickly.

To help you with that, we have a [Speedrun](https://algo.monster/problems/speedrun) feature. Instead of coding each problem, you will be given a multiple choice question related to the techniques and templates used to solve the problem. This cuts down the time to go through many problems significantly.

![Speedrun](https://algo.monster/speedrun.png)

## Approach Problems Systematically with the Flowchart

Our newest resource, [the flowchart](https://algo.monster/flowchart), offers a structured method to discern the appropriate pattern from nuanced cues in problem statements. It comes enriched with comprehensive explanations and example problems. This is where all the patterns you have learned and mastered come together to help you solve problems systematically.

![Algorithm Selection Flowchart](https://algo.monster/flowchart-demo.png)

## Getting Your Questions Answered

Being an educator has taught me that education should be tailored to the individual. It's almost impossible to write an article that makes everyone likes it. If you write it too simple, the advanced students will get bored. If you write it too advanced, the beginners will get lost. You need a way to get individual user's questions answered. This is why we have multiple ways to get your questions answered:

- Ask our "Teaching Assistant", an AI-powered chatbot pre-trained with the content of each article that can answer most of your questions. Here's a contrived example of me using the chatbot to ask a question about this article you are reading:

![AI TA](https://algo.monster/ai-ta.png)

- Use the "👨‍🏫 Help Me!" button for coding help. The TA can answer anything related to debug your code. For example, you can ask it to debug your code, reason for time and space complexity or even rate your code.

![AI TA](https://algo.monster/ai-debug.png)

- Finally, you can always ask for human help in the [forum](https://discuss.algo.monster/) or [Discord](https://discord.gg/NzM4te47DT). If, even after completing these steps, you find yourself still struggling to grasp a concept, feel free to reach out to me directly via Discord private message. I'm quite confident in the quality of our material, so encountering such difficulties should be a rare occurrence.

### A Few Considerations:

- Our platform prioritizes understanding patterns quickly over exhaustive test cases. In actual interviews, you won't always have preset test cases. Instead, your analytical thinking and solution explanation play pivotal roles.
- We're more about acing interviews than competitive programming, which is why we don’t emphasize vanity metrics like % people you beat etc.
- Our editor boiler plate code setup is slightly different from other platforms you may have used. The driver code is provided so that you can copy paste into your favorite IDE and run it locally if you'd like to.
- While video content is in the pipeline, our current focus is on interactive illustrations and AI-assisted learning. Check out our written content and stay tuned on our [Youtube Channel](https://www.youtube.com/@algo.monster) for updates.

Doing coding interviews is no easy task. But with a sound system in place, all you need is the practice to conquer the coding interview. We hope you find this website helpful in your journey. If you have any questions, please don't hesitate to reach out to us.

## How to Stay Focused While Preparing for Coding Interviews

Today's digital world is full of distractions, especially when you're getting ready for software engineering interviews. This guide will help you prepare without getting distracted, so you can do your best.

### Optimizing Your Environment to Stay Focused

Focus isn't just about willpower. Your environment also matters. Changing what's around you can help you focus better.

#### Control Your Smartphone:

Your phone can be a big distraction. Here's how to handle it:

- Keep Your Phone Far Away: Put your phone in another room or out of reach. This is the best way to avoid distractions.
- Do Not Disturb Mode: If you really can't do without the phone, at least put it on DND mode to stops interruptions.
- Delete Your Social Media Apps: Apps like TikTok make us want quick rewards. Once you get used to easy dopamine, it becomes harder for you to focus with low dopamine-releasing tasks like studying. This can make it hard to focus on coding problems that help us in the long run. Understanding this can help you make better choices.

#### Block Distracting On Your Desktop

- [Focused YouTube Extension](https://chrome.google.com/webstore/detail/focused-youtube/nfghbmabdoakhobmimnjkamfdnpfammn): Blocks video recommendations. You can still search for videos. I have found this to be the most effective way to block YouTube distractions while still being able to use it for learning.
- Clean Computer Profile: Make a special user profile on your computer just for studying. Keep it simple, with no extra apps or websites in your browser history. Use this profile only when you study.

### Stay Motivated

#### "The Inner Game of Tennis"

In his book "[The Inner Game of Tennis](https://www.readthechapters.com/the-inner-game-of-tennis--the-classic-guide-to-the-mental-side-of-peak-performance-summary)", Timothy Gallwey emphasized the importance of mental skills in tennis. The key is to focus on the "game" itself and not worry about other things. This helps you play better. The same is true for coding interviews. Do not worry about things like whether you will get the job, why my friends are doing better than me, etc. Focus on the problem in front of you. Life is a single-player game. You are competing against only yourself. Focus on the game and you will do better.

### The Job Offer Takes Care of Itself: A Growth Mindset

Finally, I'd like to leave you with a growth mindset with this video:

Now that we've laid the groundwork for effective preparation, let's dive into the core of interview readiness. Are you ready to take your coding skills to the next level?