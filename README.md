# Documentation Playbook

## Introduction

Welcome to our Documentation Playbook! This guide is designed to help you produce consistent documentation that is easy to read, understand, and use. By following the guidelines outlined in this playbook, you can ensure that your documentation is professional, accurate, and consistent in tone, voice, and formatting.

<br>

## Target Audience

Before you start writing your documentation, it's important to define your target audience. This will help you choose the appropriate tone and voice for your documentation, as well as determine the level of technical detail that you need to include.

Our target audience includes developers, technical writers, project managers, and other stakeholders who are involved in building and using our products and services. We assume that our readers have a basic understanding of programming concepts and terminology.

<br>

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

<br>

## Structure

For consistent documentation structure follow the two guides based on Fuel’s two main categories. 

1. Procedural, a tutorial based document to guide a user step by step through a specific task.
2. Conceptual, a piece of documentation which helps the user run through a general topic down to its specifics. 

| Procedural                                                                                                                                               | Conceptual                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. Title (h1)<br>2. Introduction (h3)<br>3. Prerequisites (h2)<br>4. Step 1 — Writing X (h2)<br>...<br>5. Step n — Building Y (h2)<br>6. Conclusion (h2) | 1. Title (h1)<br>2. Introduction (h3)<br>3. Prerequisites (optional) (h2)<br>4. Subtopic X (h2)<br>...<br>5. Subtopic Y (h2)<br>6. Conclusion (h2) |

When writing your guide you should be asking yourself questions about how this tutorial or article is going to benefit the reader and what they will accomplish. 

### Title (h1)

The purpose of the title should explicitly answer the question of "What the goal of this task will be?" in under 60 characters while being as specific as possible. 

**Template**
How to "task" with "software" on "infrastructure" 

**Example**
How to deploy a Sway smart contract on the Fuel beta-3 testnet

### Introduction

In one to three paragraphs motivate the reader about expectations of this tutorial and put emphasis on what they will acoomplish not just learn. Answer questions like

1. What the tutorial is about
2. Why the reader should be learning this topic
3. What will the reader do or create in this tutorial
4. What will they have accomplished by the end

**Example**

In this tutorial you will be writing a simple token smart contract smart contract and deploying int onto Fuel's beta-3 testnet. By the end you will be have a good grasp of the full Fuel suite from writing basic Sway code, to using the Fuel's Rust SDK for testing and the Forc toolchain.

### Prerequisites (h2)
Spell out exactly what the reader should have done before the current tutorial. Use a list with point linking to existing fuel tutorials and be specific. There is no need to repeat documentation that already exists for example you can simple point them to the quick start guide for installing the Fuel suite. 

**Example**
1. Installing forc
2. Installing rust
3. Installing fuelup
4. Git, node?
5. Accounts that users will need

### Steps (h2)

Try to be as granular as possible. Descibe to the reader two things what they need to do and why. Focus on the reader. Not we will learn but You will build. Should be running their own code block and sandwiched by. The instruction should be sandwich between by what the command does and after what the purpose of that command was.

1. What the command does
2. Command
3. Details about the command 
   1. Arguments purpose
   2. Why your reader is using them

Display the output in a separate block


### Transitions (p)
Introduction sentences to each step and closing transition should be used to help the reader internalize what the user has just completed and what the next step is. They act as a checkpoint to make sure that the user has understood and completed the steps properly.

**Example**
You have now written your first Sway contract you will need to make sure that it builds properly. To do this you will be 

### Conclusions (h2)
Try to summarize what the reader has accomplished during this tutorial or learned by reading this. Continue that focus on the reader by suggestion next Fuel, tutorials, documentaions, or articles they can explore.

**Example**
Now that you have successfully built and deployed a Sway smart contract on the Fuel beta testnet you can apply that to more complex contracts

<br>

## Formatting

All of the documentation for Fuel is in Markdown and to ensure consistency in formatting, we recommend using the following closely to this ruleset.

### Headers

Each section of tutorials needs a header. Rule of thumb is to use H3s as little as possible and try your best to not use H4s.
1. H1 are reserved for 
   - Titles
2. H2 are used for 
   - Defining prerequisites 
   - Steps in a tutorial
   - Conclusions
3. H3 are used for 
   - Introductions

For a step based tutorials, **-ing** words should be used. 

**Example**
| Recommended ✅                               | Not Recommended ❌                        |
|---------------------------------------------|------------------------------------------|
| # Deploying your Sway contract to the testnet | # Deploy your Sway contract to the testnet |

### Inline Text
   
When looking to include any of the following in **bolded**, *italics*, or `code` inline in any of your text explaining make sure that it is used in the correct category.

| **Bold**                                                                                                        | _Italics_                      | `Code`                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| 1. Visible GUI text<br>2. Hostnames usernames<br>3. Term lists<br>4. Emphasis when changing context for command | 1. Introducing technical terms | 1. Commands<br>2. Package names<br>3. Optional commands<br>4. Filenames and paths<br>5. Example URLs<br>6. Ports<br>7. Key Presses |

### Code blocks
Code blocks should be used for things like commands to execution commands, files and scripts, outputs, interactive dialogs only. Basically anything that the user can copy and paste into their own system. 

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
   $ sample <span style="color:DodgerBlue">DodgerBlue</span> sample
   </pre>


3. Codeblock use the proper command line highlighting when possible and use $ to indicate a commandline is being used

   ```bash
   $ cd
   $ forc new counter-contract
   ```

### Variables
   
Variables should always be highlighted to indicate to the user that a change is required. This includes URLs, version numbers, and modified lines in a file. When describing the highlighted variable avoid color labeling things as colors could change.

**Example**

```bash

```

### Images and diagrams

When including images within your tutorial, use a brief caption to bring context to the image. Images should always be paired with alt text incase of rendering issues. A brief caption should always be followed as well to give the image context. Maks sure the image is as short as possible so it does not take up unessesary space.

| Recommended ✅                                   | Not Recommended ❌                                                             |
|-------------------------------------------------|-----------------------------------------------------------------------------|
| 1. GUIs<br>2. Interactive dialog<br>3. Diagrams | 1. Code<br>2. Config files<br>3. Outputs <br>4. Anything that can be copied |

**Example Rendered Image**

<figure class="image">
<img src="./assets/block-explorer.png" alt="Some alt text">
<figcaption style="text-align: center">Caption for block explorer</figcaption>
</figure>

**Example Unrendered Image**

<figure class="image">
<img src="../assets/block-explorer.png" alt="Some alt text">
<figcaption style="text-align: center">Some caption for block explorer</figcaption>
</figure>