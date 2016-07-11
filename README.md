# ytnobody/covernment

[Devel::Cover::Reporter::Html](https://metacpan.org/pod/Devel::Cover::Report::Html) as a Service

## DESCRIPTION

Devel::Cover::Report::Html as a Service

## SYNOPSIS

Run a server

    docker run --rm -p 9210:9210 -it ytnobody/covernment

Then, create `.proverc` in your repository as following.

    --lib
    --color
    --failures
    --recurse
    --timer
    --trap
    --exec "perl -Ilib -MDevel::Cover=+ignore=.*,+select,^lib"

Afterword, run `prove` for testing. Then, get a covernment client and run it.

    curl -L https://is.gd/covernment > covernment
    bash ./covernment MyProjectName http://yourhostname:9210

That's all. Dashboard is http://yourhostname:9210/dashboard/index.html

## AUTHOR

ytnobody - ytnobody at gmail dot com
