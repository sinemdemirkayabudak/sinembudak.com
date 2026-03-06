+++
date = '2026-03-06T23:57:07+03:00'
draft = true
title = 'Why I Finally Started Using copilot-instructions.md'
tags = ['GitHub Copilot']
+++

I loved GitHub Copilot at first. But I kept rewriting its suggestions. Then I realized: Copilot didn't know me. It didn't know my style, my patterns, my opinions about code. That changed when I discovered `.github/copilot-instructions.md`.

#### The Problem: Copilot Didn't Know Me
So every response needed tweaking. Every suggestion required context switching. When I created a function, I had to rewrite it to fit my style: formatting, naming, adding type hints and comments, etc. It felt like I was still doing half the work.

#### The Solution: Repository-Wide Custom Instructions
Then I learned about `.github/copilot-instructions.md` — a simple Markdown file that tells Copilot exactly how I work.

The magic? Once I create it, Copilot automatically uses it for every request in that repository. No manual prompting. No remembering to add context. It just knows me.

#### How to Set It Up
1. Create the File
2. Write Your Standards
- No special syntax, just Markdown. Here's what mine looks like:

```
# My Project Copilot Instructions

## Key rules
- Use camelCase for variable and function names.
- Format code with 2 spaces for indentation.
- ⁠All new dependencies go through ⁠uv add.
- ⁠Follow ruff formatting rules.

## Testing
Write unit tests for every new function using pytest.

## Documentation
Include docstrings for all functions and classes.
```

3. Save and Go
VS Code immediately picks it up. Copilot starts using it right away.


#### Benefits

- **Fewer Corrections**  
    I spend less time reformatting code. Copilot gets it right the first time because it knows my preferences.

- **Faster Coding**  
    No more context-switching between different code styles. I just keep building.

- **Better Learning**  
    When Copilot understands my patterns, it generates suggestions that align with how I actually build things. More relevant, more useful.

- **Confidence in Quality**  
    My code is consistent across all my projects. That consistency means fewer bugs and easier maintenance months later.

#### You Can See It Working
In VS Code, when Copilot uses your custom instructions, they appear in the References section of its response. You can verify exactly what context it had. That transparency is reassuring.

#### Keep It Updated
Custom instructions work best when they reflect how you actually code. As I evolve my practices, I update the file. It's like having a co-pilot that grows with me.

#### The Bottom Line
One file —`copilot-instructions.md`— is the difference between Copilot knowing what I want and knowing how I want it. That single file bridges that gap.

If you're building your own projects and using Copilot, setting this up is one of the best 5 minutes you can invest.