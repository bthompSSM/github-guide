# Configuring Git

To configure Git locally, it is recommended to use the following commands:

```bash
git config --global user.name "name" # Where name is your full name (e.g., "Brian Thompson")
git config --global user.email "email" # Where email is your SSM email (e.g., "brian.thompson@ssmhealth.com")
```

You can also configure Git to save your credentials for a certain period of time, which is useful if
you don't want to have to enter your credentials every time you push or pull.

```bash
git config --global credential.helper store
```

To increase the amount of time Git will save your credentials, you can use the following command,
where the timeout is in seconds (e.g., 3600 seconds = 1 hour):

```bash
git config --global credential.helper 'cache --timeout=604800' # 1 week
```
