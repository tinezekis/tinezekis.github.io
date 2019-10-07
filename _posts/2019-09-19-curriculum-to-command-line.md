---
layout: post
title: Curriculum to Command Line
subtitle: Why teachers make great coders, and what your team can learn from them
date: 2019-09-19
categories: blog
---

<p>
  <em>This article is adapted from a talk I gave at <a target="blank" href="https://www.javascriptandfriends.com/">JavaScript & Friends</a> and <a target="blank" href="https://www.musiccitytech.com/">Music City Code</a>. You can find the slides from that talk <a target="blank" href="https://speakerdeck.com/tinezekis/curriculum-to-command-line-why-teachers-make-great-coders-and-what-your-team-can-learn-from-them">here</a>. You can also read this article on <a target="blank" href="https://medium.com/@tinezekis/curriculum-to-command-line-why-teachers-make-great-coders-and-what-your-team-can-learn-from-them-2079c533a01a">Medium</a>.</em>
</p>

<hr>

<img width="100%" src="/imgs/20190919-curriculum-to-command-line/01-title-page.png">

<p>
  Hello! My name is Christine Zekis, but I go by ‘Tine Zekis, which also happens to be my Twitter handle (<a target="blank" href="https://twitter.com/tinezekis">tinezekis</a>). My pronouns are she, her, hers. I’m a Software Engineer and a former High School Math Teacher.
</p>

<p>
  Before we dig in, I’d like you to take a moment to consider this question: <em>Who was your favorite teacher and why?</em> This could be anyone from your preschool teacher to a college professor, or anything in between. And it doesn’t need to be from a traditional education setting…maybe it’s your Sunday school teacher, or a dance instructor, or a soccer coach.
</p>

<p>
  Here’s what I came up with when I did this exercise:
</p>

<p>
  My favorite teacher was my high school geometry teacher, Ms. Hardin.
  <ul>
    <li>She had a great sense of humor</li>
    <li>She was able to break down logic and explain her reasoning</li>
    <li>She related the content to our lives</li>
    <li>She was deeply committed to her students</li>
  </ul>
</p>

<p>
  Now that you’ve thought a bit about what makes an awesome teacher, I’d like to spend a few minutes convincing you of my premise…that awesome teachers make awesome coders.
</p>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/02-argument.png">

<h3>(Awesome) Teachers Make Awesome Coders</h3>

<p>
  While planning any lesson, most teachers will start with the learning objectives. What will students be able to do as a result of this lesson? A learning objective might be something like, “As a student in Ms. Zekis’s Algebra class, I can apply the quadratic formula to solve word problems involving trajectory.” Perhaps you’ve seen something similar in your work, only developers would call this a <em><strong>user story</strong></em>. A user story could be, “As a user with admin access, I can edit the names and email addresses of other users.”
</p>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/03-user-stories.png">

<h4>Learning Objectives => User Stories</h4>

<p>
  So let’s talk about the learning objectives, or user stories, for this article:
  <ol>
    <li>As a <strong>programmer</strong>, I can improve my comprehension and hone my problem-solving skills by creating and taking opportunities to teach others.</li>
    <li>As a <strong>team member</strong>, I can improve my communication skills by breaking down concepts for a variety of audiences.</li>
    <li>As a <strong>leader</strong>, I can help my team to become better collaborators by creating a culture of teaching and learning.</li>
    <li>As a <strong>hiring manager</strong>, I can appreciate the skills that former educators and other career changers may bring to the table.</li>
  </ol>
</p>

<p>
  Consider these various roles and decide what your goals will be for the remainder of your reading here. Try to focus on one or two of these objectives as we continue on.
</p>

<hr>

<p>
  After establishing the learning objectives, teachers will typically move on to the assessment. How do we know we met our objectives? Translating this to the world of coding isn’t too much of a stretch: this is when we would write our tests or specs. How do we know the code does what we say it does?
</p>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/04-write-the-tests.png">

<h4>Write the Assessment => Write the Tests</h4>

<p>
  When I used to write math exams, I would start by making sure the students can solve a particular type of problem with an intuitive solution. For instance, the answer is a positive, whole number. Developers might call this the <em><strong>happy path</strong></em>. But I also want to make sure the students can solve problems with harder solutions. Maybe the answer is negative, or zero. Maybe it’s a very large number or a decimal. These are our <em><strong>edge cases</strong></em>.
</p>

<p>
  And not until the assessment is done do I start to figure out what the students must do to get from where they are to where they will need to be to meet the objectives. In education, we call this Backward Planning, or Outcome-Based Education. In the tech industry, we might call this <em><strong>test-driven development (TDD)</strong></em>.
</p>

<hr>

<p>
  Then, after all the planning, it’s time to actually teach the lesson. This is usually around the time that 90% of the plan gets thrown out the window. I’m going to call this part <em><strong>deployment</strong></em>. Throw it out there and wait for something to go wrong.
</p>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/05-deployment.png">

<h4>Teaching the Lesson => Deployment</h4>

<p>
  Various studies have estimated that teachers make anywhere from 1,000 to 3,000 decisions per day in their classrooms. I’ve seen <a target="blank" href="http://info.csp.edu/globalassets/academic-resources/academic-departments/teacher-education/teacher-education-conceptual-framework.pdf">1,500</a> cited most often, so we’ll stick with that for the sake of argument. If we assume a day from 8:00am to 3:00pm with a 30-minute lunch break, that’s more than 230 decisions per hour, which is almost 4 per minute. So that’s a decision just about every 15 seconds. Teachers are constantly adjusting to the changing situations in their classrooms — moving closer to the student who seems distracted, pausing to assess understanding, switching gears if the class isn’t getting it or just seems restless.
</p>

<p>
  I’m not sure about you, but that’s the kind of person I want troubleshooting support issues on my team. Plus, who better to have on an Agile team doing CI/CD? Our teams need to be nimble, able to pivot when we get new requirements or feedback from our users. And teachers are trained in that kind of flexibility and willingness to change directions.
</p>

<hr>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/06-lifelong-learners.png">

<h4>Lifelong Learners => Lifelong Learners</h4>

<p>
  One more transferable skill teachers can bring to development is their commitment to lifelong learning. Teachers are constantly growing, adjusting, and learning new things. I’m not going to change this one. This applies to coders without any updates. Technology is always changing, and to do well in this field, coders need to be constantly growing, adjusting, and learning new things.
</p>

<hr>

<p>
  Okay, let’s bring it back to our initial conversation. Think about that favorite teacher you remembered earlier, and consider this: <em>Would your favorite teacher make a great coder? Why or why not?</em>
</p>

<p>
  Here are some things I came up with when I did this. Reasons a teacher might make a great coder:
  <ul>
    <li>Adjusts well to changing situations</li>
    <li>Good at predicting what might go wrong</li>
    <li>Enjoys solving interesting problems</li>
    <li>Can break down problems into smaller steps</li>
    <li>Thinks outside the box</li>
    <li>Cares deeply about students — Could this translate to caring for users or teammates?</li>
  </ul>
</p>

<p>
  Maybe your favorite teacher just gave really good hugs. Is that something that could translate to being an empathetic programmer? Or maybe they were really good at calling you out on your bullshit. How could that be useful on an engineering team?
</p>

<p>
  And now we’ve come to the most important part of this article…
</p>

<h3>So What?</h3>

<p>
  What does any of this have to do with you? Well, let’s revisit that last point about teachers and coders: they are both lifelong learners.
</p>

<p>
  I hope we can all agree that, in order to excel in this field, we need to be willing and able to continue learning. Now, there are countless studies on how people learn, but I’m going to go way back to some early thinking on the topic. Aristotle once said, “Teaching is the highest form of understanding.” (<a target="blank" href="https://www.teachthought.com/pedagogy/great-best-quotes-about-teaching/">Source</a>) Since then, people have done tons of research on the matter, and this seems to actually be the case.
</p>

<img width="80%" src="/imgs/20190919-curriculum-to-command-line/07-protege-effect.png">

<p>
  Psychologists call it the <strong>Protégé Effect</strong>. The Protégé Effect is the improved short-term and long-term comprehension one gets from preparing to teach and carrying out a lesson on a new concept. In other words, if you want to learn something, the best thing you can do is teach it.
</p>

<p>
  Some of the statistically significant <a target="blank" href="https://effectiviology.com/protege-effect-learn-by-teaching/">results of the effect</a> include:
  <ul>
    <li><em>Increased metacognitive processing</em> — awareness of your learning process</li>
    <li><em>Increased use of effective learning strategies</em> — things like organizing the material in a logical way, seeking out key pieces of information or major takeaways, etc.</li>
    <li><em>Increased motivation to learn</em> — people often take their learning more seriously when they’re responsible for educating others, rather than just themselves</li>
    <li><em>Increased feelings of competence and autonomy</em></li>
    <li><em>Improved communication skills, confidence, and leadership ability</em></li>
  </ul>
</p>

<p>
  So with all of these benefits, it’s pretty compelling as an advantageous and effective way to learn new things.
</p>

<h4>Ways to Benefit from the Effect</h4>

<p>
  There are multiple ways to experience these benefits. First, you can simply <em><strong>prepare</strong></em> to teach the concept. Organize the information, consider the answers to potential questions your audience might ask, etc. Planning the lesson alone has been shown to produce some form of the Protégé Effect.
</p>

<p>
  You can also <em><strong>pretend</strong></em> to teach the topic. Go through the content out loud, as if you are teaching.
</p>

<p>
  However, the strongest benefits of the Protégé effect will come if you actually <em><strong>teach</strong></em> a lesson on the topic.
</p>

<h4>Ways to Teach</h4>

<p>
  There are also lots of ways to teach. One is to <em><strong>give a talk</strong></em>. You can give a lightning talk, host a lunch & learn, lead a meeting, or put together some other form of group presentation.
</p>

<p>
  Not a fan of public speaking? No problem! <em><strong>Write it down</strong></em> instead. You can break down concepts in writing through a blog tutorial, or maybe some detailed documentation.
</p>

<p>
  You can also teach in a one-on-one setting by taking on the role of <em><strong>mentor</strong></em>.
</p>

<p>
  And I’m sure you can think of other ways to start teaching. Get creative…maybe you want to do a code demo and post it on YouTube. Just as long as you’re communicating information to an audience of some sort.
</p>

<h3>So, What Next?</h3>

<p>
  So, what can you do differently this coming Monday? Well, old habits die hard, so I’m going to give you some homework.
</p>

<h4>What can I teach?</h4>

<p>
  Over the next couple of days, try to think about what kinds of things you can teach. Maybe you want to talk about a fun side project you’re working on, or a new technology you’re considering for your team. Or you could talk about the problem you figured out most recently. I’ve found a good rule of thumb to be that if any problem ends up being more than a quick Google search or visit to StackOverflow to solve, write it down. It’s probably a good candidate for a lightning talk or a blog post.
</p>

<h4>What else can I do in my current role to engender a culture of teaching and learning?</h4>

<p>
  Additionally, I’d like you to think about what else you can do in your current role to help create a culture of teaching and learning on your team. For instance, my team has a designated time for weekly 5-minute lightning talks, and people can just sign up. We also have bi-weekly tech demos where teams show off something they’ve been working on. Last month, our summer interns got the chance to present a feature they built, which was a great opportunity to showcase their work and answer questions about it.
</p>

<h4>What Would Teacher Do?</h4>

<p>
  And finally, I want you to think about what your favorite teacher would do. What’s something that made that teacher awesome? Could you do something similar in your own role?
</p>

<p>
  My favorite teacher, Ms. Hardin, could always lighten the mood and create a positive environment by telling silly jokes. And I was the person on my team who helped keep up a tradition of starting every day with a Dad joke on Slack.
</p>

<p>
  So what’s something you can do that your awesome teacher did?
</p>

<h3>Resources</h3>

<p>
  Special thanks to all the people who made and released these awesome resources for free:
  <ul>
    <li>Teacher statistics from <a target="blank" href="http://info.csp.edu/globalassets/academic-resources/academic-departments/teacher-education/teacher-education-conceptual-framework.pdf">Concordia University, St. Paul</a></li>
    <li>Aristotle quote from <a target="blank" href="https://www.teachthought.com/pedagogy/great-best-quotes-about-teaching/">TeachThought</a></li>
    <li>Protégé Effect summary by <a target="blank" href="https://effectiviology.com/protege-effect-learn-by-teaching/">Effectiviology</a></li>
    <li>Presentation template by <a target="blank" href="https://www.slidescarnival.com/">SlidesCarnival</a></li>
  </ul>
</p>
