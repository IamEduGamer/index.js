const Discord = require("discord.js")

const intents = new Discord.Intents(32767)

const client = new Discord.Client({ intents })

client.on("messageCreate", async (message) => {
  
  let prefix = '.'//poner cualquier prefix para el bot//

  if(message.channel.type === "DM") return;
  if(message.author.bot) return;
  if(!message.content.startsWith(prefix)) return;

  const args = message.content.slice(prefix.length).trim().split(/ +/g);
  const command = args.shift().toLowerCase();
  
  if(command === 'edugamer'){//poner cualquier comando que quieras//
     message.channel.send("Valla, Ya se que quieres conocer a mi amo IamEduGamer Contactalo: IamEduGamer#7724")//pon cualquier texto al ejecutar el comando//
  }
  if(command === 'help'){//poner cualquier comando que quieras//
     message.reply(" **COMANDOS** 1.help 2.alianzas 3.yt 4.edugamer **PROXIMAMENTE MAS** ")//pon cualquier texto al ejecutar el comando//
  }
  
  if(command === 'alianzas'){//poner cualquier comando que quieras//
    message.channel.send("Wow, ¿Quieres Hacer Una Alianza?, Para Hacer Esto Tienes Que Tener: mas de 60 miembros sin contar los bots nada mas. Hacernos premocion y llegar a los 20 miembros")//pon cualquier texto al ejecutar el comando//
  }
  if(command === 'yt'){//poner cualquier comando que quieras//
     message.reply("https://www.youtube.com/channel/UCD7bP4lvvwD9jMfJUet5IcQ")//pon cualquier texto al ejecutar el comando//
  }  

})



client.login("TOKEN DEL BOT")
