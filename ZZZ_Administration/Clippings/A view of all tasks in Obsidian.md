---
title: A view of all tasks in Obsidian
source: https://www.reddit.com/r/ObsidianMD/comments/15a0bz9/a_view_of_all_tasks_in_obsidian/
author:
published: 2023-07-26
created: 2026-01-23
description:
tags:
  - clippings
---
Hi,

I'm looking for a way to create a note/page/view of all the tasks globally from all my notes, preferably organized and grouped by their source or note that they come from.

Is there a way to do this? I was thinking of using a query but I didn't find any solution online, and I'm too much of a beginner to Obsidian to do it myself from scratch.

Any help will be appreciated! Thanks!

---

## Comments

> **lillemets** • [8 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jti449u/) •
> 
> The Dataview plugin supports querying and listing task lines, e.g.
> 
> \`\`\`dataview
> TASK
> FROM #tag
> GROUP BY file.name
> \`\`\`

> **TRexPhilbo** • [5 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jti0l6f/) •
> 
> You can use the Tasks plugin to do this.
> 
> [Here’s the plugin’s Github page](https://github.com/obsidian-tasks-group/obsidian-tasks) and [here’s the documentation](https://publish.obsidian.md/tasks/Introduction)
> 
> > **Combinatorilliance** • [15 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jti3kuf/) •
> > 
> > You need to install the plugin. Go to settings, community plugins, enable plugins if you haven't yet. Find the **tasks** plugin, install and enable it.
> > 
> > You're now good to go.
> > 
> > In any note, just copy any of the below ones. For more advanced queries you can look at the documentation [u/TRexPhilbo](https://www.reddit.com/user/TRexPhilbo/) linked
> > 
> > To show all tasks, all you need to write is
> > 
> > \`\`\`tasks
> > \`\`\`
> > 
> > To show all tasks that are not finished yet
> > 
> > \`\`\`tasks
> > status.name includes todo
> > \`\`\`
> > 
> > I prefer to group them by filename
> > 
> > \`\`\`tasks
> > status.name includes todo
> > 
> > group by path
> > \`\`\`
> > 
> > > **randomUserPardonMe** • [1 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/m5pzqm5/) •
> > > 
> > > How to remove template files from this list.
> > > 
> > > > **Combinatorilliance** • [1 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/m5q0w2v/) •
> > > > 
> > > > I don't know. You can look at the documentation, it's in the link by TRex.
> > 
> > **InstructionCool1232** • [1 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/n37x6sg/) •
> > 
> > I love you for this

> **Sipstaff** • [6 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jtihlx8/) •
> 
> Solution without plugins:
> 
> This query gives you all open todos
> 
> \`\`\`query  
> task-todo:""
> \`\`\`
> 
> Unfortunately it doesn't look very good and you can't tick things off from the embedded query. At least you can use it to quickly switch to the note the tasks are in.
> 
> > **fabr1zio** • [0 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jtkhz37/) •
> > 
> > You can create a canvas with different tasks query (tasks support tags so you can have a canvas frame for tags with the same tags)
> > 
> > > **Sipstaff** • [2 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jtkpbm3/) •
> > > 
> > > Can you elaborate? I'm not sure what you're trying to say.

> **ostrowele** • [1 points](https://reddit.com/r/ObsidianMD/comments/15a0bz9/comment/jti7c95/) •
> 
> Thank you, that's exactly what I was looking for!