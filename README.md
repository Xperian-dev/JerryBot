## Commands
All commands require an admin role which you can set by using `j/admin` (requires administrator permissions on the server). The bot will reply with missing permissions otherwise. Executing a command without any argument will prompt the bot to provide you with instructions on how to use the command effectively.

- `j/help` shows this set of commands along with a link to the repository.
- `j/new` starts the creation process for a new reaction role message. Check [below](#example) for an example.
- `j/edit` edits the text and embed of an existing reaction role message.
- `j/reaction` adds or removes a reaction from an existing reaction role message.
- `j/notify` toggles sending messages to users when they get/lose a role (default off) for the current server (the command affects only the server it was used in).
- `j/colour` changes the colour of the embeds of new and newly edited reaction role messages.
- `j/activity` adds an activity for the bot to loop through and show as status.
- `j/rm-activity` removes an activity from the bot's list.
- `j/activitylist` lists the current activities used by the bot as statuses.
- `j/admin` adds the mentioned role or role id to the admin list, allowing members with a certain role to use the bot commands. Requires administrator permissions on the server.
- `j/rm-admin` removes the mentioned role or role id from the admin list, preventing members with a certain role from using the bot commands. Requires administrator permissions on the server.
- `j/adminlist` lists the current admins on the server the command was run in by mentioning them and the current admins from other servers by printing out the role IDs. Requires administrator permissions on the server.
- `j/kill` shuts down the bot.
- `j/systemchannel` updates the main or server system channel where the bot sends errors and update notifications.

### Usage Example
In this example the prefix used is `j/`. Once you initiate the process, be sure only to answer to the bots questions or the bot might record unwanted messages as instructions. You can still send messages to other channels, and others can send messages to the channel you initiated the process in.

Initiate the message creation process with `j/new`.
```
User: j/new
```

Next, you will be asked to attach emojis to roles. Only use standard emojis or those that are hosted on servers the bot has access to. Send a single message for each single combination and then type `done` when you have finished attaching emojis to their respective roles. Ensure that the roles are mentionable when you are doing this step. You can disable mentions after finishing this step.
```
Bot: Attach roles and emojis separated by a space (one combination per message).
When you are done type `done`. Example:
:smile: `@Role`
User: :rage: @AngryRole
User: :sob: @SadRole
User: :cry: @EvenSadderRole
User: :joy: @HappyRole
User: done
```

Next, you will be asked if you want to allow users to select multiple reactions (and role) at a time or not. Then, you will be asked to either create a new message or use an existing one. Using an existing message will prevent you from using `j/edit` if the target message wasn't created by the bot. If you choose to use an already existing message simply react to it with 🔧, the bot will remove the 🔧 reaction and add the ones you chose.

Otherwise, you will have to customise the message that the bot is going to send with the roles attached to it. Enter a title and the content of your message by separating them with ` // ` (the space before and after `//` is important).
```
Bot: What would you like the message to say? Formatting is: `Message // Embed_title // Embed_content`. `Embed_title` and `Embed_content` are optional. You can type `none` in any of the argument fields above (e.g. `Embed_title`) to make the bot ignore it.
User: none // Select your roles // Click on the buttons below to give yourself some roles!
```

Finally, the bot will send the message to the channel specified in the first step, and it will react with each reactions specified so that the buttons are ready to be used. The bot will remove any new reactions to the message to avoid clutter. For example, if you added an `:eggplant:` reaction to the message created in this example, the bot will remove it as it is not attached to any role.