# sd-helper

[![Last commit](https://img.shields.io/github/last-commit/aydwi/sd-helper.svg)]()

A bot to automatically post useful information on the SecureDrop Gitter room. Messages can be scheduled to be posted on specific day(s) of the week at specific time(s). It can be used in any other Gitter room as well.

## Requirements

1. Python [Requests](http://docs.python-requests.org/en/master/)

    `pip3 install requests`

2. Python [schedule](https://schedule.readthedocs.io/en/stable/)

    `pip3 install schedule`
    
## Usage

1. Sign in with a Github account on https://developer.gitter.im/ to obtain the authentication token required to access the Gitter API.

2. Clone the repo, and `cd` into it.

3. Create a file **auth.yml** with its contents as

   `apitoken: <your-gitter-api-token>`

4. Run `python3 sd-helper.py` to start the bot.

## Configuring the bot's behavior

The behavior of the bot can be configured by editing **data.yml**. Add tasks by specifying 3 things-

1. `message` - The message that needs to be posted. 
2. `day` - Integer value(s) denoting day(s) of a week. The week starts from Monday(0) and goes till Sunday(6).
3. `time` - Time value(s) at which the message is to be posted, according to your timezone. It should be in 24h format, like `HH:MM`.

The name of the task does not matter.

## Notes

1. Make sure the Gihub account has joined the room before posting.
2. Do not post same message too frequently. Gitter's spam detection may flag your account.
3. Register an OAuth 2.0 application at https://developer.gitter.im/apps for highly active bots.
