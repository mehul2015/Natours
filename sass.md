### SASS Cheatsheet (SCSS syntax)

## Variables

variables : $variable-name

## Nesting

navigation {
a{
li {

        }
    }

}

is equivalent to

navigation a li {

}

## Out of the box functions

darken()
lighten()

sass --watch sassFileName.scss:cssFileNameToBeCompiledTo.css

## Mixins

@mixin mixinName($someParameter){

    write many lines of css code here
    use someParameter somewhere as $someParameter

}

someSelector{

    @include mixinName($someArgument)

}

## Placeholder(you can think of it as classes where selectors can extend from)

%somePlaceholder{
a lot of css code goes here
}

someSelector{

    @extend somePlaceholder

}

##### SASS Compilation in this project

The package.json has a script called compile with the command : "node-sass sass/main.scss css/style.css -w"

npm run compile
