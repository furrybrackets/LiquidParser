# LiquidParser
A multi-utility parser for Parsing Liquid Markdown.

## Parsing Liquid Markdown

Example:

```ts
import { ParseMarkdown } from '@liquidmd/markdown';
import { readFileSync } from 'fs';

const Parse = new ParseMarkdown({
  spec: 'liquid', // 'liquid' | 'github' | 'common'
  type: 'ast' // 'ast' | 'html'. HTML is only available for GitHub & CommonMark types
});

const file = readFileSync('markdown.md', {encoding:'utf8', flag:'r'}).toString();

console.log(Parse.gen(file));
```
