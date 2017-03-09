# NAME

MojoX::CloudFlare::Simple - simple cloudflare client without wrapper

# SYNOPSIS

```perl
use MojoX::CloudFlare::Simple;

my $cloudflare = MojoX::CloudFlare::Simple->new(
    email => 'blabla@blabla.com',
    key   => 'secretkeyblabla',
);

my $zones = $cloudflare->request('GET', 'zones');
say Dumper(\$zones);

my $result = $cloudflare->request('DELETE', "zones/$zone_id/purge_cache", {
    files => [
        'http://bsportsfan.com/',
        'https://assets.bsportsfan.com/images/team/s/34953.png'
    ]
});
say Dumper(\$result);
```

# DESCRIPTION

MojoX::CloudFlare::Simple is a simple client for cloudflare. it does not have any wrap or trick. it just simply send the requests and return your data. you need handle everything yourself.

You can get your key from [https://www.cloudflare.com/a/account/my-account](https://www.cloudflare.com/a/account/my-account)

you can find some examples scripts like get zones, purge files under examples.

please use ENV MOJO\_USERAGENT\_DEBUG for debug.

# AUTHOR

Fayland Lam <fayland@gmail.com>

# COPYRIGHT

Copyright 2016- Fayland Lam

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.

# SEE ALSO
