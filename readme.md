# RegOps (Regular Expression Operations)
A small library for performing operations on regular expressions.

## concat(...operands)
Concatenate any number of regular expressions.

## concatSpaced(...operands)
Concatenate any number of regular expressions with space characters inbetween.

## or(...operands)
Create a regular which matches any of the operand RegExp.

## optional(operand)
Add a `?` operator, making the operand optional.

## kleene(operand)
Add a `*` operator, applying Kleene closure to the operand.


## kleeneSpaced(operand)
Apply Kleene closure to the operand separated by space characters.

## kleeneJoin(operand, separator)
Apply Kleene closure to the operand separated by a given separator RegExp.

## kleenePoliteList(...operands)
Matches a list of the form "operand, operand and operand", with any number of items

## kleeneConcatSpaced(stem, appendages)
Concatenate (with a space) the appendages to the stem using kleene closure. The resulting RegExp will match the stem + zero or more appendages.

## optionalConcatSpaced()
Concatenate (using a space) the appendages to the stem using an optional operator.

## autoBracket(operand)
Add non capturing brackets to the operand unless it is very simple.

## whole(operand)
Add `^` and `$` at the beginning and end of the operand so it matches an entire string.

## capture(operand[, groupName])
Include the operand in an (optionally named) capturing group.
