# A Guestbook (made using Symfony)

This is a Guestbook application. More precicely, a backup of the lessons from the book "Symfony 6: The Fast Track" by Symfony founder Fabien Potencier. In this repository I will commit and document the steps taken in the book. Therefore, this readme can be seen as an abstract of the book. 
During the learning process the project will be hosted at Platform.sh - which students of the book are encouraged to use -, but later the project should be migrated to a different host as Platform.sh is free for a limited time. 

## How to Install and Run the Guestbook

### Environment configuration

This application needs PHP 8.1 and other tools to be either installed locally or configured, instructions found [here](https://symfony.com/doc/current/the-fast-track/en/1-tools.html), if you already have the tools, pay special attention to PHP [extensions](https://symfony.com/doc/current/the-fast-track/en/1-tools.html#php).

## How to Use the Guestbook

### Connecting to database locally
This can be done with the help of the Symfony-cli, just type: `symfony run psql`;
Dumping the database: `symfony run pg_dump --data-only > dump.sql`;
Restoring: `symfony run psql < dump.sql`;

## Troubleshooting

- Althought manipulating data in production should be avoided at all cost, if this is needed, the symfony-cli has commands to help with that:

```bash
symfony cloud:tunnel:open
symfony var:expose-from-tunnel

# INTERACTIVE SHELL:
symfony run psql

# OR batch:
symfony sql

# DON'T FORGET to close the connection afterwards with:
symfony cloud:tunnel:close
```

## Developments details

### Template engine

Symfony utilizes the Twig template engine. The advantages of utilizing a template engine include, but not only, the automatically treatment of front-end variables with the php native function `htmlspecialchars()`, which helps to avoid XSS attacks. 

### Symfony profiler toolbar

The Symfony profiler can be used to measure performance of different components, find errors, read dumps.

### Configuration files

Describing infrastructure with configuration files allow for code and infrastructure changes as part of the same patches.

## Glossary

### Acronyms
- FQCN / fqcn: "Fully Qualified Class Name";

## Credits

[Symfony 6: The Fast Track](https://symfony.com/doc/current/the-fast-track/en/index.html)\
[freeCodeCamp: How to Write a Good README File for Your GitHub Project](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/)