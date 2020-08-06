# regex-snippets
Collection of useful regex snippets that I make &amp; want to preserve

## JavaScript / TypeScript

### Convert class methods into arrow functions
Find: `^(async |)([^\( ]*)\(([^\)]*)\) \{`
- `async getUserWithLogin(email, password) {`

Replace: `const $2 = $1($3) => {`
- `const getUserWithLogin = async (email, password) => {`

### Convert CommonJS imports into ES2015 imports
Find `const ([^=]*)= require\((.*)\);`
- `const express = require('express');`

Replace: `import $1from $2;`
- `import express from 'express';`
