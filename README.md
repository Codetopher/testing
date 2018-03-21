# testing
a testing repository
const Discord = require('discord.js');
const Client = new Discord.Client();
const OwnerID = "130515926117253122";

const prefix = "!"

Client.on("ready", () => {
	console.log("online");
});

Client.on("message", async (message) => {
	if (message.author.bot) return;
	if (!message.content.startsWith(prefix)) return;

	let command = message.content.split(" ")[0];
	command = command.slice(prefix.length);

	let args = message.content.split(" ").slice(1);

	if (command == "setup") {
		const embed = new Discord.RichEmbed()
		.setColor(0x954D23)
		.setDescription("`The Rule of law will prevail! Fairness and justice will be served! Campaign for GermanicvsJvlivs!`\n\n**Become a Campaigner** <#419949164533645312>\n\nThe campaign staff is composed of teams. Joining one makes you a part of the campaign staff.\n\n**TEAMS:**\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&417811419195506689>\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&417811494986711060>\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&417811529241722882>\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&417811561432743938>\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&417811594349903882>\n<:GermanicvsJvlivsforSheriff:419683081931325441> <@&418189325403160576>\n\nYou can ping the leader of that team like so:\n'*<@&418189325403160576> I want to join.*'\n\nMore information will follow once you have joined a team.")
    .setFooter("Last Edited", "https://media.discordapp.net/attachments/335547742783012865/418923429874368523/2ndgerm1.png")
    .setThumbnail("https://media.discordapp.net/attachments/335547742783012865/418923429874368523/2ndgerm1.png")
    .setTimestamp();

    message.channel.send({embed})
	}

});
