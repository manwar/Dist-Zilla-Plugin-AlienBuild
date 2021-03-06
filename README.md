# Dist::Zilla::Plugin::AlienBuild [![Build Status](https://secure.travis-ci.org/plicease/Dist-Zilla-Plugin-AlienBuild.png)](http://travis-ci.org/plicease/Dist-Zilla-Plugin-AlienBuild)

Use Alien::Build with Dist::Zilla

# SYNOPSIS

    [AlienBuild]

# DESCRIPTION

This [Dist::Zilla](https://metacpan.org/pod/Dist::Zilla) plugin is designed to help create [Alien](https://metacpan.org/pod/Alien) modules using
the [alienfile](https://metacpan.org/pod/alienfile) and [Alien::Build](https://metacpan.org/pod/Alien::Build) recipe system with [Alien::Base](https://metacpan.org/pod/Alien::Base).  The
intent is that you will maintain your [alienfile](https://metacpan.org/pod/alienfile) as you normally would,
and this plugin will ensure the right prereqs are specified in the `META.json`
and other things that are easy to get not quite right.

Specifically, this plugin:

- adds prereqs

    Adds the `configure` requirements to your dist `configure` requires.  It
    adds the `any` requirements from your [alienfile](https://metacpan.org/pod/alienfile) to your dist `build`
    requires.

- adjusts Makefile.PL

    Adjusts your `Makefile.Pl` to use [Alien::Build::MM](https://metacpan.org/pod/Alien::Build::MM).  In the future `Build.PL`
    may be supported.

- turn on dynamic prereqs

    Which are used by most [Alien::Build](https://metacpan.org/pod/Alien::Build) based [Alien](https://metacpan.org/pod/Alien) distributions.

# SEE ALSO

[Alien::Build](https://metacpan.org/pod/Alien::Build), [alienfile](https://metacpan.org/pod/alienfile), [Alien::Base](https://metacpan.org/pod/Alien::Base), [Alien::Build::MM](https://metacpan.org/pod/Alien::Build::MM)

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2017 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
