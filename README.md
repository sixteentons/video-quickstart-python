# Video Quickstart for Python

This application should give you a ready-made starting point for writing your
own video chatting apps with Twilio Video. Before we begin, we need to collect
all the credentials we need to run the application:

Credential | Description
---------- | -----------
Twilio Account SID | Your main Twilio account identifier - [find it on your dashboard](https://www.twilio.com/console).
Twilio Video Configuration SID | Adds video capability to the access token - [generate one here](https://www.twilio.com/console/video/profiles).
API Key | Used to authenticate - [generate one here](https://www.twilio.com/console/dev-tools/api-keys).
API Secret | Used to authenticate - [just like the above, you'll get one here](https://www.twilio.com/console/dev-tools/api-keys).

## A Note on API Keys

When you generate an API key pair at the URLs above, your API Secret will only
be shown once - make sure to save this in a secure location, 
or possibly your `~/.bash_profile`.

## Setting Up The Python Application

This application uses the lightweight [Flask Framework](http://flask.pocoo.org/). 
Begin by creating a configuration file for your application:

```bash
cp .env.example .env
```

Edit `.env` with the four configuration parameters we gathered from above. 

Next, we need to set up your Python environment. Install `virtualenv` via `pip`:

```bash
pip install virtualenv
```

Activate your virtual environment and install our dependencies:

```bash
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
```

Now we should be all set! Run the application using the `python` command.

```bash
python app.py
```

Your application should now be running at [http://localhost:5000](http://localhost:5000). Send an invite 
to another user in another browser tab or window to start video chatting! When you're finished, deactivate your virtual environment using `deactivate`.

![screenshot of chat app](http://i.imgur.com/nVR70FQ.png)

## License

MIT
