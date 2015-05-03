# Luapress v2

Luapress is *yet another* static blog generator, written in Lua, with posts in markdown.

## Install

`luarocks install luapress`

## How-To

+ Create an empty directory, cd into it
+ Run `luapress init` to create the base config/directories
+ Drop markdown files in `posts/` and `pages/`
+ Run `luapress`
+ Copy the contents of `build/` to web

## Options & Notes

+ Set `config.link_dirs = true` in `config.lua` to have posts & pages generated at `/name/index.html` rather than `/name.html`
+ The `inc/` directory will be copied to `build/inc/`, and your template inc to `build/inc/template`
+ Set `$key=value` in posts for custom data (use `<?=self:get('post').key ?>` in template)
+ Set `$time=time_in_epoch_seconds` or `$date=day/month/year` to customize post time (default file update time)
+ With pages set `$order=number` to determine page ordering in links list
+ Hide pages from the link list with `$hidden=true`
+ Add `nocache` before the URL to ignore caching (for template dev)
+ Add `clean` before the URL to empty the `inc/` directory before starting (forces `nocache`)

## Example

I'm using it for my blog, [Pointless Ramblings](http://pointlessramblings.com).
