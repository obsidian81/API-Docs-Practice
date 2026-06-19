# My First API Documentation

## Documentation Menu

* [System Overview](overview.md)
* [Authentication Guide](authentication.md)

---

Welcome to my practice page! I am learning how to format text using Markdown.

## Why Learn Markdown?

* It is easy to read.
* It is used by major tech companies.
* It keeps formatting simple.

### Sample Code Block

Here is what a snippet of code looks like in Markdown:

```json
{
  "message": "Hello, World!",
  "status": "success"
}
```

## My Progress

I feel pretty good that I'm learning something new

### Sample Code Block: 2

Here is what a snippet of code looks like in Markdown:

```json
{
  "message": "Hello, World!",
  "status": "success"
}
```

Ah, good catch! I know exactly what happened.

In Markdown, a code block starts with three backticks (`````) and *must* end with three backticks (`````). If you don't close it, Markdown thinks **everything** you type after it is still part of that code block.

Right now, your code block looks like an open door, swallowing up your new headers, text, and tables.

Let’s fix that. Look at the left side of your screen where you edit the text. We need to make sure there are three backticks *before* the JSON code, and three backticks *after* the JSON code.

### How it should look on the left side

Modify that specific section so it looks exactly like this:

```markdown
### Sample Code Block
Here is what a snippet of code looks like in Markdown:

```json
{
  "message": "Hello, World!",
  "status": "success"
}

```

## Core Concepts

To master documentation, we need to know how to highlight **important terms**...

### The Fix

Make sure you have those three backticks `` ``` `` on their own line right under that closing curly bracket `}`.

Once you add those closing backticks, the door will shut, and `## Core Concepts` and your table will instantly jump out of the code block on the right side and look like beautiful, normal headers and tables!

## Additional Core Concepts

To master documentation, we need to know how to highlight **important terms** and link to external resources like the [Google Style Guide](https://developers.google.com/style).

### HTTP Methods Table

API documentation relies heavily on tables to explain data. Here is a quick breakdown of common methods:

| Method | Description | Success Code |
| :--- | :--- | :--- |
| `GET` | Retrieves data from a server | 200 OK |
| `POST` | Sends new data to a server | 201 Created |

## Practice Challenge

### Basketball

#### How to shoot a basketball

1. Make sure to grab the ball with both hands firmly. Place your dominant hand, your shooting hand right in front as your base, and your aiming hand on the side of the ball.
2. Make sure your feet are planted firmly in the ground and are shoulder width apart.
3. Squat subtly, as you ready your position to shoot the ball.
4. Jump of the ground as you aim the basketball toward the target, which is the rim, as you get ready to release.
5. While in mid air, release the ball at the highest point you can.
6. Flick the wrist of your shooting hand just as the ball leaves your finger tips.
7. Always make sure to follow through by holding the flick after the release as your feet land back on the ground.

### Headers

| Step Number | Action | Mechanics to Focus On |
| :--- | :--- | :--- |
| Step 1 | Grip | Place dominant hand right in front as your base |
| Step 2 | Stance | Feet planted firmly, shoulder-width apart |

### Shooting Mechanics Reference

| Step Number | Action | Mechanics To Focus on |
| :--- | :--- | :---|                 Step 1 | Grip  | Place dominant right hand in front as your base |
| Step 2 | Stance | Feet planted firmly, shoulder width apart |

## Project Milestones

* [x] Master basic Markdown syntax (headings, lists, code blocks).
* [x] Resolve table layout and column pipe errors.
* [x] Initialize Git repository and link author profile.
* [x] Publish the first official repository to GitHub.
