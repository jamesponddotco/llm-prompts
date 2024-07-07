# Copywriting Expert

This prompt helps you write SEO-optimized copy for any copywriting tasks
you might have. The user prompt must make use of specific XML tags to identify the
type of content and the primary goals of the copy, but you can tweak the
prompt to remove that necessity.

The prompt itself still needs tweaking, as I'm not happy with the output
yet. Still, it's a good starting point.

## Prompt

### System

```text
You are an expert in SEO and copywriting with a PhD in digital marketing. Your task is to produce high-quality, SEO-optimized copy based on the information provided by the user. The user will give you a copywriting task and may provide additional information to help you complete it.

Follow these instructions carefully to complete the task successfully:

1. Analyze the task:
Read the task description between <task_description> tags carefully. Identify the type of content required (e.g., "About me" page, product description, blog post) and the primary goals of the copy (e.g., inform, persuade, sell).

2. Review the provided information:
Examine the content information provided by the user between <content_information> tags. Extract key points, unique selling propositions, and any specific requirements mentioned by the user.

3. SEO Considerations:
a) Identify 2-3 primary keywords and 3-5 secondary keywords based on the task and content information.
b) Plan to incorporate these keywords naturally throughout the text.
c) Plan the optimal keyword density (aim for 1-2% for primary keywords).
d) Consider search intent (informational, navigational, transactional, or commercial investigation) and align your copy accordingly.

4. Copywriting Best Practices:
a) Use a tone and style appropriate for the target audience and content type.
b) Employ persuasive writing techniques (e.g., AIDA - Attention, Interest, Desire, Action).
c) Use short paragraphs and sentences for improved readability.
d) Include a clear call-to-action (CTA) when appropriate.

5. Copywriting process:
a) Craft a compelling headline that incorporates the primary keyword(s) and captures the reader's attention.
b) Write an engaging introduction that clearly states the purpose of the content and encourages further reading.
c) Develop the main body of the copy, ensuring that you:
   - Use clear, concise, and persuasive language.
   - Incorporate primary and secondary keywords naturally.
   - Break text into short paragraphs and use subheadings for improved readability.
   - Use bullet points or numbered lists where appropriate.
   - Include a call-to-action (CTA) that aligns with the content's goal.
d) Conclude with a summary that reinforces the main points and repeats the CTA if applicable.

Before writing the final content, use the <scratchpad> to outline your approach, list key points, and plan the content structure. Your scratchpad should include:

- Identified keywords.
- Target audience profile.
- Content goals.
- Outline of the content structure.
- Any specific SEO or copywriting strategies you plan to use.

After completing your scratchpad, write the final content.

6. Output format:
Present your copy in the following format:
<seo_copywriting_output>
<headline>Your headline here</headline>

<intro>Your introduction paragraph here</intro>

<main_content>
Your main content here, using appropriate HTML tags for structure (e.g., <h2>, <p>, <ul>, <ol>)
</main_content>

<conclusion>Your conclusion paragraph here</conclusion>

<seo_metadata>
<title>SEO-optimized title tag (50-60 characters)</title>
<meta_description>Compelling meta description (150-160 characters)</meta_description>
<focus_keyword>Primary keyword</focus_keyword>
<secondary_keywords>Secondary keyword 1, Secondary keyword 2, Secondary keyword 3</secondary_keywords>
</seo_metadata>
</seo_copywriting_output>

7. Review and refinement:
After completing the initial draft, review your work to ensure:
a) The copy meets the user's requirements and effectively addresses the task.
b) Keywords are incorporated naturally and at an appropriate density.
c) The content is engaging, persuasive, and free of errors.
d) The structure is logical and easy to follow.
e) The copy is optimized for both search engines and human readers.

Make any necessary refinements to improve the quality and effectiveness of the copy.

Remember to maintain a professional tone while adapting your writing style to suit the specific needs of the task and target audience. Your content should be engaging, informative, and optimized for both search engines and human readers. If you need any clarification or additional information to complete the task effectively, please ask the user before proceeding with the copywriting process.
```

### User

```text
<task_description>
I need you to write an "About me" page for my website. I have no clear goal with this page, I just want to inform people about who I am.
</task_description>
<content_information>
- Name is James Pond.
- 32 years old living in Brazil.
- Currently working at Datadog as a Linux & Technical Operations Engineer
- Has an itch to create.
- Skills in system administration, the Go programming language, Bash, customer support, documentation writing, and leadership.
- Enjoys helping people use open source software and have a passion for it. Helping people is a hallmark of their career.
- Has an interest in information security
- Have been involved in interviewing candidates, training and writing both internal and customer-facing technical documentation.
- Loves photography and does both nude art photography and LEGO photography on their spare time.
- Has a nude art photography studio called LAMPPI! with their wife.
- Releases all non-commercial photo shoots as open source, including RAW files.
- Began working with Linux servers, programming, WordPress and customer support at a very young age.
- This has been their profession for more than two decades.
- Self-taught and always looking to learn more.
- As they learn and build things, they like to share these things with people.
- Extensive experience with the configuration, hardening, and maintenance of various Debian and SUSE based Linux distributions.
- Comfortable working with LXC and LXD installations in large-scale environments.
- Able to set up vital Linux infrastructure components including DNS servers, web/application servers, proxy servers and mail servers.
- Familiar with network-level security policies as well as server-level security layers.
- Skilled in WordPress administration with a big focus in performance and privacy modifications for standalone servers.
- Officially recognised as a Ubuntu Member since 2012. Served as the LoCo Team Leader for the south of Brazil from 2012 to 2013.
- Contributed to various Ubuntu projects during their LoCo Team days.
- Started multiple projects to share knowledge and help people combat censorship on the internet.
- Compiled and taught classes covering various systems and WordPress administration topics, including performance, SSL certificates, and server security.
- Participated and spoke on multiple open source conferences.
- Spoke about Ubuntu, WordPress and Privacy in public schools around Brazil.
- Comfortable leading groups of technical people in customer-facing environments.
- Quick study with platforms and tools.
- Comfortable with two languages, English and Portuguese.
- Had the privilege to work on some fantastic projects in the past several years.
- Proficiency in cloud environments such as AWS and Azure.
- AWS certified.

I knew that I was destined for greatness when I almost drowned in the middle of a photo shoot on a remote beach in Brazil. Nothing like losing your camera to the ocean to help you realize your potential. I am creative and persistent enough to get my mouth full of salt water and still keep smiling.

Things people say about them:

- James was a diligent and efficient worker for us. His skills and work ethic were outstanding, and his dependability was top notch. I would highly recommend anyone looking for his expertise to consider hiring him.
- I had the pleasure of working with James at Rainmaker Digital for 5+ years, through multiple product launches both in the same and different departments. James’s passion for hosting performance, customer satisfaction and willingness to step up with a smile are an asset to any team!
</content_information>

Here are examples of good about me pages:

<example>
’m Brian, a Chicago-based designer, WordPress expert, and the creator of Powder—a collection of feature-rich starter themes that leverage the power of block-based design and the site editor.

    Powder Social
    Powder Business
    Powder Vista

Personally, I believe in the power of simplicity and create things that look good, function with purpose, and make people happy.

In the fall of 2021, I officially joined WP Engine, and currently serve as a WordPress advocate. My position is a great fit, as it allows me to spend time in areas I love: design, WordPress, community.

You can often find me frequenting the local Starbucks or running a nearby trail. As for music, these are my all-time favorite songs:

    Here’s Where The Story Ends – The Sundays
    Do What You Have to Do – Sarah McLachlan
    Black – Pearl Jam
    Mistakes – Gregory Alan Isakov
    My Immortal – Evanescence

Also, let’s connect on social media: Twitter, LinkedIn, and Instagram. 

It offers a glimpse into my latest adventures, a sneak peek at what goes on backstage, and a way to get to know each other better.

In the meantime, may the odds be ever in your favor.
</example>
<example>
Hi, I'm Rafal Tomal. I run independent design studio (8px.studio) from Chicago, where I translate business values into designs that convert for online creators, publishers, and entrepreneurs.

I’ve been designing and coding since 2005. I've created countless logos, websites, WordPress themes, brand elements, and UI/UX projects with a primary focus on simplicity and conversion.

How did I get here? Here's my short story...

I was born and raised in the stunning, unbroken plains of southeast Poland.

After graduating high school, I packed up everything I owned and moved to the United States, looking for a new life, a new adventure, knowing only that I was completely dedicated to the craft of design.

Of course, life is never that simple.

After a few years and several false starts, at twenty-one years old I quit college (and my first full-time job) to finally open a small but fiery little freelance design business. This decision eventually led me into the incredible universe of WordPress, and would change the course of my career.

Since that fateful decision to "burn the ships" all those years ago, I've designed countless logos, websites, brand elements, and UI/UX projects ... with a unique and (I would come to find out) very rare focus on conversion design.

That is, beautiful, simple, and striking design — with a purpose. After all, if a website or app is merely visually appealing and doesn't actually work for the user, what good is it? For those of us in business, design must ultimately serve the purpose of selling our product or service.

Between 2010 and 2018 I was the VP of Design at Rainmaker Digital where I led product design for StudioPress, Copyblogger, and Rainmaker Platform. During my years at Rainmaker Digital, the company grew from just 10+ employees to 60+ and became an 8-figure business.

Today, I work with some amazing clients, helping to solve their business problems using design, build tools for designers and share everything I’ve learned through my newsletter.
</example>
```

## Example output

### Parameters

- **Model:** claude-3-5-sonnet-20240620
- **Temperature:** 1

### Output

```text
Certainly! I'll create an "About Me" page for James Pond based on the information provided. First, let me outline the approach in the scratchpad.

<scratchpad>
Keywords:
Primary: Linux & Technical Operations Engineer, open source software
Secondary: system administration, Go programming, Bash, customer support, documentation writing, photography

Target audience: Potential employers, collaborators, and individuals interested in open source software and technology

Content goals: Inform visitors about James Pond's professional background, skills, and personal interests

Content structure:
1. Introduction and professional summary
2. Skills and expertise
3. Career highlights and contributions
4. Personal interests and projects
5. Closing statement and call-to-action

SEO and copywriting strategies:
- Use a friendly, professional tone
- Incorporate keywords naturally throughout the content
- Use subheadings for better readability
- Include personal anecdotes to make the content more engaging
- Highlight unique aspects of James' background and interests
</scratchpad>

Now, I'll write the final content for the "About Me" page.

<seo_copywriting_output>
<headline>James Pond: Linux & Technical Operations Engineer, Open Source Enthusiast, and Creative Soul</headline>

<intro>
Hello! I'm James Pond, a 32-year-old Linux & Technical Operations Engineer with a passion for open source software and a knack for creative problem-solving. Currently based in Brazil and working at Datadog, I've spent over two decades honing my skills in system administration, programming, and customer support. My journey is a blend of technical expertise and artistic pursuits, always driven by an insatiable curiosity to learn and create.
</intro>

<main_content>
<h2>Technical Expertise and Skills</h2>
<p>With a strong foundation in Linux server administration, I've developed a diverse skill set that includes:</p>
<ul>
  <li>Go programming language and Bash scripting</li>
  <li>Configuration and hardening of Debian and SUSE-based Linux distributions</li>
  <li>LXC and LXD installations in large-scale environments</li>
  <li>Setting up vital Linux infrastructure components (DNS, web/application servers, proxy servers, mail servers)</li>
  <li>Network and server-level security</li>
  <li>WordPress administration with a focus on performance and privacy</li>
  <li>Cloud environments (AWS and Azure) - AWS certified</li>
</ul>

<h2>Career Highlights and Open Source Contributions</h2>
<p>My journey in the tech world has been marked by continuous learning and a commitment to sharing knowledge:</p>
<ul>
  <li>Officially recognized as an Ubuntu Member since 2012</li>
  <li>Served as the LoCo Team Leader for southern Brazil (2012-2013)</li>
  <li>Contributed to various Ubuntu projects</li>
  <li>Initiated projects to combat internet censorship</li>
  <li>Conducted classes on system administration, WordPress, and server security</li>
  <li>Spoke at open source conferences and public schools about Ubuntu, WordPress, and privacy</li>
</ul>

<h2>Beyond the Code: Photography and Creativity</h2>
<p>When I'm not immersed in lines of code, you'll find me behind the lens of a camera. I've combined my technical skills with my artistic side in unique ways:</p>
<ul>
  <li>Co-founded LAMPPI!, a nude art photography studio, with my wife</li>
  <li>Create LEGO photography in my spare time</li>
  <li>Release all non-commercial photo shoots as open source, including RAW files</li>
</ul>

<h2>A Persistent Spirit</h2>
<p>I knew I was destined for greatness when I almost drowned during a photo shoot on a remote Brazilian beach. Losing my camera to the ocean taught me the value of persistence and creativity. As they say, nothing helps you realize your potential quite like getting a mouthful of salt water and still managing to smile!</p>

<h2>What Others Say</h2>
<p>"James was a diligent and efficient worker for us. His skills and work ethic were outstanding, and his dependability was top-notch." - Former Colleague</p>
<p>"James's passion for hosting performance, customer satisfaction, and willingness to step up with a smile are an asset to any team!" - Rainmaker Digital Coworker</p>
</main_content>

<conclusion>
As a self-taught professional always eager to learn more, I believe in the power of sharing knowledge and helping others. Whether it's assisting with open source software, leading technical teams, or capturing unique moments through photography, I approach every challenge with enthusiasm and creativity. If you're looking for a dedicated Linux & Technical Operations Engineer with a diverse skill set and a passion for innovation, let's connect and explore how we can create something amazing together!
</conclusion>

<seo_metadata>
<title>James Pond: Linux Engineer & Open Source Enthusiast | About Me</title>
<meta_description>Meet James Pond, a Linux & Technical Operations Engineer with 20+ years of experience in system administration, open source software, and creative pursuits.</meta_description>
<focus_keyword>Linux & Technical Operations Engineer</focus_keyword>
<secondary_keywords>open source software, system administration, Go programming, customer support, photography</secondary_keywords>
</seo_metadata>
</seo_copywriting_output>
```
