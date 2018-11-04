# PG Format and Converters

version 0.1.0

## Quick Start

Create sample data:

    $ vi data.pg
    p1 :person name:John
    p2 :person name:Mary
    p1 p2 :follows since:2013

Run pg2pgx command for example:

    $ alias pg2pgx='docker run --rm -v $PWD:/shared g2gml/pg:0.1.0 pg2pgx'
    $ pg2pgx data.pg data
    "data.pgx.nodes" has been created.
    "data.pgx.edges" has been created.
    "data.pgx.json" has been created.

For converting other formats:

    $ pg2pgx <input_pg_file> <output_path_prefix>
    $ pg2neo <input_pg_file> <output_path_prefix>
    $ pg2aws <input_pg_file> <output_path_prefix>
    $ pg2dot <input_pg_file> <output_path_prefix>

# Local Installation

Requirements:

* Git
* Node

Install:

    $ git clone -b v0.1.0 https://github.com/g2gml/pg.git
    $ cd pg
    $ npm install
    $ npm link
