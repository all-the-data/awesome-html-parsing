# awesome-html-parsing

You have HTML. We have parsers.

HTML parsing for kicks.

## Draft list

- [grep](https://www.gnu.org/software/grep/manual/grep.html). Just no.
- sed
- awk?
- node / javascript
    - https://github.com/jsdom/jsdom
    - https://github.com/cheeriojs/cheerio
    - https://github.com/fb55/htmlparser2
    - https://github.com/fb55/DomUtils
    - https://github.com/fb55/domhandler
    - https://nodejs.org/en/knowledge/command-line/how-to-parse-command-line-arguments/
    - https://nodejs.dev/learn/reading-files-with-nodejs
    - https://nodejs.org/api/fs.html#filehandlereadfileoptions
    ...grargh
- htmlq
  - Written in rust
  - Uses CSS selectors
  - `sudo apt install -y cargo && time cargo install htmlq`
  - `cat file.html | htmlq 'div > song > content > h3'`
  - Cannot extract text content
  - Cannot remove whitespace, etc. For that you need to combine with sed `| sed 's/^ *//g' | sed '/^[[:space:]]*$/d'`
- Perl regex
  - Similar to grep, but more powerful
  - `cat file.html | perl -C7 -0777 -e '(@s) = <STDIN> =~ m{<h3>(.+?)</h3>}sg; @s = map { s/^\s*//; s/\s*$//; s/\s{2,}//g; $_ } @s; print "@s"`
- Perl modules
  - TODO
- Python
   - [html.parser](https://docs.python.org/3/library/html.parser.html)
   - event-based, not dom. Ugh
- Ruby
  - [nokogiri](https://nokogiri.org/tutorials/searching_a_xml_html_document.html#basic-searching)
  - TODO
- Go
  - TODO
- GUIs, Applications, Web services
  - Real Programmers Don't Use GUIs

## To do

- Add "hello world" examples for each entry

## See also

- Other "awesome web scraping" github repos
- [How to analyse HAR files](https://gist.github.com/willsheppard/f0bdc1a2290f3d24d9579856ab5b7b53#file-jq_cheat_sheet-md)

