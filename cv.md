## SUMMARY


# Michael Penzov
## Contacts:


> Gmail: gig40594@gmail.com

> Mail ru: gig405@mail.ru

> Telegram: @Coldstation_021

> Discord: Rendyq#5916

## My goal:

### I want to get a good theoretical and practical knowledge and skills of frondend development for make a good career and become a professional.

## Skills:

### Professional skills:
* Languages: C++,C#, Java, Delphi,JavaScript;
* Have some experience with the Java Spring Framework;
* HTML5/CSS3;
* Microsoft SQL Server, MongoDB, Postgresql;
* Basic skills in Adobe Photoshop.
### Languages skills:
* Russian;
* English;
* Belarusian.
## Exaple of latest code:

>Some part of my Telegram Bot on NodeJS:

```javascript
let eventParser = require("../helpers/eventParser");
let createEventByUserId = require("../helpers/dbmanager").createEventByUserId;

module.exports = function (bot) {
    bot.command("addevent", async (ctx) => {
        let event = eventParser(ctx);
        console.log("EVENT", event);
        if (event) {
            try {
                const createdEvent = await createEventByUserId(event);
                console.log("ADD EVENT OBJ", createdEvent);
                try {
                    await createdEvent.save((e)=> {
                        console.log(e);
                    });
                } catch (e) {
                    console.log(e);
                }
            } catch (e) {
                console.error(e);
                await ctx.reply("Oops! Something went wrong.");
            }
            await ctx.reply("Event has been successfully added to the database.");
        } else {
            await ctx.reply("Oops! Something went wrong. Check /addevent command example message to be used.");
        }
    });
};
```
## Education
* Graduated from school in 2017;
* Now I am a student at the international university "MITSO".