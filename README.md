# Project based vimrc setup

## Why?

Let's say you do development in your free time and you also work for a company or on an open source project. That project happens to have different styling than your personal project such as using spaces instead of tabs.

Instead of using different editors, you can share a file so that you can easily follow the style guide (or use other configuration options).

## How?

In your main .vimrc file add:

```
set exrc            " enable per-directory .exrc files
set secure          " disable unsafe commands in local .vimrc files
```

Setup all your dev for this company/team/project/etc in a master directory. For example all projects should be in `~/development/company`

Add a `.exrc` file in `~/development/company`

It should contain the company styles for vim such as:

```
set encoding=utf-8
set expandtab
set tabstop=2
set shiftwidth=2
set ts=2
```

That's it!

All projects you create/edit/checkout in `~/development/company` should follow the styling above (2 spaces for tabs – or however you configure it).