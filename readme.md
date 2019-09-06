# RegOps
Perform basic operations to manipulate regular expressions.

## Install
```npm i regops```
 
## Index

### Functions

* [autoBracket](_regops_.md#autobracket)
* [bracket](_regops_.md#bracket)
* [capture](_regops_.md#capture)
* [concat](_regops_.md#concat)
* [concatSpaced](_regops_.md#concatspaced)
* [initial](_regops_.md#initial)
* [kleene](_regops_.md#kleene)
* [kleeneConcatSpaced](_regops_.md#kleeneconcatspaced)
* [kleeneJoin](_regops_.md#kleenejoin)
* [kleenePoliteList](_regops_.md#kleenepolitelist)
* [kleeneSpaced](_regops_.md#kleenespaced)
* [optional](_regops_.md#optional)
* [optionalConcatSpaced](_regops_.md#optionalconcatspaced)
* [or](_regops_.md#or)
* [sourcify](_regops_.md#sourcify)
* [terminal](_regops_.md#terminal)
* [whole](_regops_.md#whole)

## Functions

###  autoBracket

▸ **autoBracket**(`str`: string): *string*

*Defined in [regops.ts:14](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L14)*

If necessary, put non-capturing brackets around a regex source string.

**Parameters:**

Name | Type |
------ | ------ |
`str` | string |

**Returns:** *string*

___

###  bracket

▸ **bracket**(`str`: string): *string*

*Defined in [regops.ts:9](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L9)*

Put non-capturing brackets around a regex source string.

**Parameters:**

Name | Type |
------ | ------ |
`str` | string |

**Returns:** *string*

___

###  capture

▸ **capture**(`operand`: RegExp | string, `groupName`: string): *RegExp*

*Defined in [regops.ts:125](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L125)*

Surround a regular expression with capturing parentheses, optionally specifying a group name.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |
`groupName` | string |

**Returns:** *RegExp*

___

###  concat

▸ **concat**(...`operands`: null | string | RegExp[]): *RegExp*

*Defined in [regops.ts:22](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L22)*

Concatenate a list a of regular expressions.

**Parameters:**

Name | Type |
------ | ------ |
`...operands` | null \| string \| RegExp[] |

**Returns:** *RegExp*

___

###  concatSpaced

▸ **concatSpaced**(...`operands`: null | string | RegExp[]): *RegExp*

*Defined in [regops.ts:31](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L31)*

Concatenate a list of regular expressions with a single-space (' ') delimiter.

**Parameters:**

Name | Type |
------ | ------ |
`...operands` | null \| string \| RegExp[] |

**Returns:** *RegExp*

___

###  initial

▸ **initial**(`operand`: RegExp | string): *RegExp*

*Defined in [regops.ts:113](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L113)*

Add a ^ marker at the beginning of a regular expression, so that it must match the beginning of a string.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *RegExp*

___

###  kleene

▸ **kleene**(`operand`: RegExp | string): *string*

*Defined in [regops.ts:56](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L56)*

Apply Kleene closure (*) operator to a regular expression.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *string*

___

###  kleeneConcatSpaced

▸ **kleeneConcatSpaced**(`stem`: RegExp | string, ...`optionalAppendages`: null | string | RegExp[]): *RegExp*

*Defined in [regops.ts:95](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L95)*

Concatenate an item with itself any number of times (using kleene closure *) using a single-space (' ') as a delimiter.

**Parameters:**

Name | Type |
------ | ------ |
`stem` | RegExp \| string |
`...optionalAppendages` | null \| string \| RegExp[] |

**Returns:** *RegExp*

___

###  kleeneJoin

▸ **kleeneJoin**(`operand`: RegExp | string, `delimiter`: string): *RegExp*

*Defined in [regops.ts:67](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L67)*

Apply Kleene repetitions of a regular expression with some specified delimiter.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |
`delimiter` | string |

**Returns:** *RegExp*

___

###  kleenePoliteList

▸ **kleenePoliteList**(...`operands`: string | RegExp[]): *RegExp*

*Defined in [regops.ts:74](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L74)*

Create a "polite list" (form: X, X, X and X) using Kleene closure to allow any number of items.

**Parameters:**

Name | Type |
------ | ------ |
`...operands` | string \| RegExp[] |

**Returns:** *RegExp*

___

###  kleeneSpaced

▸ **kleeneSpaced**(`operand`: RegExp | string): *RegExp*

*Defined in [regops.ts:63](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L63)*

Apply Kleene closure (*) operator to a regular expression, delimiting repetitions with a single-space (' ')

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *RegExp*

___

###  optional

▸ **optional**(`operand`: RegExp | string): *string*

*Defined in [regops.ts:49](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L49)*

Apply OPTIONAL (?) operator to a regular expressions.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *string*

___

###  optionalConcatSpaced

▸ **optionalConcatSpaced**(`stem`: RegExp | string, ...`optionalAppendages`: null | string | RegExp[]): *RegExp*

*Defined in [regops.ts:83](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L83)*

Concatenate a list of regular expressions with optional (?) modifiers.

**Parameters:**

Name | Type |
------ | ------ |
`stem` | RegExp \| string |
`...optionalAppendages` | null \| string \| RegExp[] |

**Returns:** *RegExp*

___

###  or

▸ **or**(...`operands`: null | string | RegExp[]): *RegExp*

*Defined in [regops.ts:40](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L40)*

Combine regular expressions with OR (|) operator.

**Parameters:**

Name | Type |
------ | ------ |
`...operands` | null \| string \| RegExp[] |

**Returns:** *RegExp*

___

###  sourcify

▸ **sourcify**(`list`: null | String | RegExp[]): *string[]*

*Defined in [regops.ts:2](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L2)*

Convert a list of convert regexs to their source strings.

**Parameters:**

Name | Type |
------ | ------ |
`list` | null \| String \| RegExp[] |

**Returns:** *string[]*

___

###  terminal

▸ **terminal**(`operand`: RegExp | string): *RegExp*

*Defined in [regops.ts:119](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L119)*

Add a $ marker at the end of a regular expression, so that it matches the end of a string.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *RegExp*

___

###  whole

▸ **whole**(`operand`: RegExp | string): *RegExp*

*Defined in [regops.ts:107](https://github.com/joelyjoel/RegOps/blob/c2156cd/src/regops.ts#L107)*

Add ^ and $ markers either side of a regular expression so that it must match an entire string.

**Parameters:**

Name | Type |
------ | ------ |
`operand` | RegExp \| string |

**Returns:** *RegExp*