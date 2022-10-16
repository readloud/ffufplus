# ffufplus - ffuf on Steroids

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/dark-warlord14/ffufplus/issues)

ffufplus - ffuf on Steroids

<img src="https://securityjunky.com/wp-content/uploads/2020/04/carbon-17-1024x497.png" alt="ffufplus" width="750">

---

### Installation

```
bash install.sh
```

### Usage

To run the tool, just use the following command.
```
bash script.sh
```

# Scripts and snippets for ffuf payloads

A collection of scripts that enable different kinds of payloads to be used with [ffuf](https://github.com/ffuf/ffuf).

### ffuf_basicauth.sh - HTTP Basic authentication

A script that generates base64 encoded combinations of username:password values in the provided wordlists. Iterates through every possible combination.

#### Example usage
Test each HTTP basic authentication username:password combination in https://example.org/endpoint, and filter out 403 - Forbidden responses.

```
./ffuf.sh usernames.txt passwords.txt |ffuf -w -:AUTH -u https://example.org/endpoint -H "Authorization: Basic AUTH" -fc 403 -c
```

## Contributing

We welcome any and all contributions. Please see `ffuf_basicauth.sh` for the preferred script header format for usage examples and author information.

### Thanks

- [@joohoi](https://twitter.com/joohoi) - for the great ffuf
