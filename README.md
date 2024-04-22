# cevre-kirliligi
import discord
from discord.ext import commands

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'{bot.user} olarak giriş yaptık')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Merhaba! Ben {bot.user}, bir Discord sohbet botuyum!')

@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)

@bot.command()
async def hava(ctx):
    await ctx.send("Havanın doğal bileşiminin çeşitli nedenlerle değişmesi, havada katı, sıvı ve gaz şeklindeki yabancı maddelerin insan sağlığına, canlı hayatına, ekolojik dengeye ve eşyalara zararlı olabilecek derişim ve sürede bulunmasıdır.")    
    
@bot.command()
async def kara(ctx):
    await ctx.send("Toprak kirliliği, katı, sıvı ve radyoaktif artık ve kirleticiler tarafından toprağın fiziksel ve kimyasal özelliklerinin bozulmasıdır.")


@bot.command()
async def su(ctx):
    await ctx.send("Su kirliliği; göl, nehir, okyanus, deniz ve yeraltı suları gibi su barındıran havzalarda görülen kirliliğe verilen genel addır. Her çeşit su kirliliği, kirliliğin bulunduğu havzanın çevresinde veya içinde yaşayan tüm canlılara zarar verdiği gibi, çeşitli türlerin ve biyolojik toplulukların yok olmasına ortam hazırlar.")

