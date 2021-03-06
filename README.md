[![Build Status](https://travis-ci.org/tyldum/Mojolicious-Plugin-NamedHelpers.svg?branch=master)](https://travis-ci.org/tyldum/Mojolicious-Plugin-NamedHelpers) [![MetaCPAN Release](https://badge.fury.io/pl/Mojolicious-Plugin-NamedHelpers.svg)](https://metacpan.org/release/Mojolicious-Plugin-NamedHelpers) [![Coverage Status](http://codecov.io/github/tyldum/Mojolicious-Plugin-NamedHelpers/coverage.svg?branch=master)](https://codecov.io/github/tyldum/Mojolicious-Plugin-NamedHelpers?branch=master)
# NAME

Mojolicious::Plugin::NamedHelpers - Mojolicious Plugin

# SYNOPSIS

    # Mojolicious
    $self->plugin('NamedHelpers');
    $self->named_helper( my_little_helper => sub { ... } );

    # Mojolicious::Lite
    plugin 'NamedHelpers';

    # Mojolicious::Lite - with custom namespace
    plugin 'NamedHelpers' => { namespace => 'My::App::Helpers' };

# DESCRIPTION

[Mojolicious::Plugin::NamedHelpers](https://metacpan.org/pod/Mojolicious::Plugin::NamedHelpers) is a [Mojolicious](https://metacpan.org/pod/Mojolicious) plugin that sets a fully qualified name to anonymous helper subs using a tiny wrapper upon helper creation.
Without this plugin those subs will be named \_\_ANON\_\_, but now they will be named after the helper.

By default the namespace will be the same as the app, but this can be overridden if desired.

The author's use-case is for providing more context in JSON-based application logs, where all helpers would identidy themselves as \_\_ANON\_\_.

# HELPERS

## named\_helper

This plugin provides a new helper called "named\_helper".

By registering your helpers with "named\_helper" the name of the sub will be set equal to the name of the helper.

# AUTHOR

This module is written by Vidar Tyldum, but withcrucial help from the #mojo IRC channel on irc.perl.org.

# SEE ALSO

[Sub::Util](https://metacpan.org/pod/Sub::Util)>, [Mojolicious](https://metacpan.org/pod/Mojolicious), [Mojolicious::Guides](https://metacpan.org/pod/Mojolicious::Guides), [http://mojolicious.org](http://mojolicious.org).
