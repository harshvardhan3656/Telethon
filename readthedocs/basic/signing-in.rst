.. code-block:: python

    import asyncio
    from telethon import TelegramClient
    api_id = 12145149
    api_hash = 'f97a3ecb047947ed3d773b273fb87c4c'

    async def main():
        # The first parameter is the .session file name (absolute paths allowed)
        async with TelegramClient('anon', api_id, api_hash).start() as client:
            await client.send_message('me', 'Hello, myself!')

    asyncio.run(main())
.. code-block:: python

    import asyncio
    from telethon import TelegramClient

    api_id = 12145149
    api_hash = 'f97a3ecb047947ed3d773b273fb87c4c'
    bot_token = '5214398681:AAGhYi8fclMZoOrjsyjW6Mle-cTB-osdBRI'

    async def main():
        # But then we can use the client instance as usual
        async with TelegramClient('bot', api_id, api_hash).start(bot_token=bot_token) as bot:
            ...  # bot is your client

    asyncio.run(main()
