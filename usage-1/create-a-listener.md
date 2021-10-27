# Listener

## Create a listener

To create a listener, it is recommended to use the [CLI](https://www.npmjs.com/package/make-bot.ts) to generate the listener body correctly.

### CLI pattern

By typing `make listener -h` you will get this following information.

```bash
make listener <event>

Positionals:
  event       # listener event                                             [required]

Options:
  --version  # Show version number                                       [boolean]
  --help     # Show help                                                 [boolean]
```

### Example

For a "guildCreate" event, type the following command.

```bash
make listener "guildCreate"
```

Then, the `src/listener/guildCreate.ts` file will be ready to be implemented.

## Arguments

{% hint style="info" %}
The `name` and `description` argument properties are obligatory.
{% endhint %}

### Required

If argument is required, it will never have the `null` value and will return an error message before the execution of the listener if it is missing. The listener will then not be executed.
