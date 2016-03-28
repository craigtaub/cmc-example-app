# Example app using CJS Mustache Compiler

Browserify handles converting CJS into Vanilla JS and builds it into bundle.
Universal ES6 (client + server side).

Setup

    npm install
    gulp

Tests

    gulp test

Linter

    gulp lint

Architecture
- Server-side: node + express + mustache
- Client-side: page + browserfiy + mustache

Research

    MUSTACHE PARTIALS
    even if does under .partials object how will mustache compiler know to look for them?
    it wont...
    It looks in 3rd argument for key/value of partial name.

    HOGAN
    creates global templates object.
    can compile into template BUT isnt CommonJS Module so has no Hogan ref and doesnt export.
    doesnt build partials as Hogan templates
    must compile Template/Partials seperately

    COMMONJS COMPILER
    https://github.com/dsheiko/cjsc
    doesnt wrap mustache view in CJS.
    i need template wrapped in CJS
    HAVE to compile template with dynamic params in..cant work.

    JADE:
    nice that partials are contained within so dont register them (Handlebars) or pass as 3rd argument (Mustache)
