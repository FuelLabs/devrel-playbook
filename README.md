# Documentation Playbook

## Introduction

Welcome to our Documentation Playbook! This guide is designed to help you produce consistent documentation that is easy to read, understand, and use. By following the guidelines outlined in this playbook, you can ensure that your documentation is professional, accurate, and consistent in tone, voice, and formatting.

## Target Audience

Before you start writing your documentation, it's important to define your target audience. This will help you choose the appropriate tone and voice for your documentation, as well as determine the level of technical detail that you need to include.

Our target audience includes developers, technical writers, project managers, and other stakeholders who are involved in building and using our products and services. We assume that our readers have a basic understanding of programming concepts and terminology.

## Tone and Voice

Borrowed from [Microsoft](https://learn.microsoft.com/en-us/style-guide/top-10-tips-style-voice) and [Digital Ocean](https://www.digitalocean.com/community/tutorials/digitalocean-s-technical-writing-guidelines)

1. Friendly but formal

- do not include jargon, memes, excessive slang, or emojis.
- Use second person to keep the focus on the reader and what they'll accomplish (e.g., "You will configure..")

2. Define acronyms and project-specific terms upfront

If you're using acronyms or words that the general audience may not understand, you should define these upon the first use. Then, you can use the acronym in subsequent writing.

**Example**
Sway introduces a new type called Address, which could represent an EOA (externally owned account) or a smart contract. EOAs are the most common type of account.

2. Use bigger ideas, fewer words
   Shorter is always better.

**Example**
Replace this: If you're ready to purchase Office 365 for your organization, contact your account representative.

With this: Ready to buy? Contact us.

3. Write like you speak
   Read your text aloud.

Does it sound like something a real person would say? Be friendly and conversational. No. Robot. Words.

**Example**
Replace this: Invalid ID

With this: You need an ID that looks like this: someone@example.com

4. Lead with verbs
   Most of the time, start each statement with a verb. Edit out you can and there is, there are, there were. To learn more, see Verbs and Word choice.

**Example**
Replace this: You can access apps across your devices, and you get online file storage and sharing.

With this: Store files online, access them from all your devices, and share them with coworkers.

## Formatting

All of the documentation for Fuel is in Markdown and to ensure consistency in formatting, we recommend using the following closely to this ruleset.

### Headers

Each section of tutorials needs a header. Rule of thumb is to use H3s as little as possible and try your best to not use H4s.
1. H1 are reserved for 
     - Titles
2. H3 should be used for 
   - Introductions
3. H2 are used for 
     - Prerequisites
     - Steps
     - Conclusions

For a tutorial -ing words should be used. 

```md
Deploying your Sway contract to the 
```

### Inline Text
When looking to include any of the following in bolded, italics, or code inline in any of your text explaining make sure that it is used in the correct category.

| **Bold**                                                                                                        | _Italics_                      | `Code`                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| 1. Visible GUI text<br>2. Hostnames usernames<br>3. Term lists<br>4. Emphasis when changing context for command | 1. Introducing technical terms | 1. Commands<br>2. Package names<br>3. Optional commands<br>4. Filenames and paths<br>5. Example URLs<br>6. Ports<br>7. Key Presses |


### Code blocks
Code blocks should be used for things like commands to execution commands, files and scripts, outputs, interactive dialogs.


1. File omissions should always use ellipses (...)

   ```rust
   contract;

   ...

   impl HelloModular for Contract {
      #[storage(read)]
      fn greet() -> str[16] {
         storage.greet
      }
   }
   ```

2. New code changes should have a different color indicating new lines or changes

   <pre>
   sample <span style="color:DodgerBlue">DodgerBlue</span> sample
   </pre>


3. Codeblock use the proper command line highlighting when possible and use $ to indicate a commandline is being used

   ```bash
   $ cd
   $ forc new counter-contract
   ```

### Variables

### Images and diagrams

When including images within your tutorial, use a brief caption to bring context to the image. Alt text should always be included in case the image cannot be rendered. A brief caption should always be followed as well to give the image context. It is as short of a height as possible to ensure that the images don’t take up too much space. 

| Recommended ✅                                   | Not Recommended ❌                                                          |
|-------------------------------------------------|-----------------------------------------------------------------------------|
| 1. GUIs<br>2. Interactive dialog<br>3. Diagrams | 1. Code<br>2. Config files<br>3. Outputs <br>4. Anything that can be copied |
