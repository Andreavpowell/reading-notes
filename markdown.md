***This is where I will put my reading notes for markdown.***

____________________________________________________________________________________________________________________________________________________________________

# What is Markdown Syntax?
Markdown is a simple, lightweight markup language to add effortless formatting to a plain text document and generate that document as an HTML file. Markdown is comprised of regular text with only a few special characters used for rendering code.  Markdown is used *very* frequently within GitHub.

_____________________________________________________________________
# How to use Markdown Syntax:

\- Headers:

    # is equal to <h1> (largest)
    ###### is equal to <h6> (smallest)

\- Images:
  
    ![Alt Text](URL)

\- Blockquotes:

    > Typically used to symbolize a direct quotation
    > Usually used if said quote is more than 4 lines
    
\- Links:

    Automatic if you use a live URL
    [Alt Text](URL)
    
\- Ordered List:

    1. XXX
    2. XXX
    3. XXX
    
***or***
  
    1. XXX
      1. XXX
      2. XXX
    2. XXX
    3. XXX
    
\- Unordered List:

    * XXX
    * XXX
     * XXX
     * XXX
     
***or***
 
     > XXX
     > XXX
      > XXX
      > XXX
      
\- Emphasis:

    *italic*
    _italic_
    
    **bold**
    __bold__
    
    ***both***
    ___both___
    
    _italic**bold**italic_

\- Inline Code:

    'code'
    
\- To Escape Syntax:

    \>, \#, \&, etc...

______________________________________________________________________

# GitHub Flavored Markdown Spec (GFM)
Some Markdown features are ***only*** available within GitHub

\- GitHub Specific Syntax:
- \@mentions
- SHA-1 hashes
- Issues
- Pull Requests
- Taks Lists (available in Gist comments and Gist Markdown files)

\- Syntax Highlighting:
- Indent your code by 4 spaces or 2 tab
- ''' XXXXXXXXXXXXX '''

\- Tasks Lists:

    - [x] 
    - [x] 
    - [x] 
    - [ ] 
Also works in Pull Requests

\- Tables:
Divide your list of words with \- (for the first row) and separate columns with \|.

    Header | Header
    ------ | ------
    XXX    | XXX
    XXX    | XXX
    
***rendered***
    
  Header | Header
  ------ | ------
  XXX    | XXX
  XXX    | XXX    

\- SHA references:
SHA-1 hash references are converted to links.

\- Issue References within Repositories:
Issue and Pull Request numbers are converted to links.

\- \@mentions:
Mentioining someone's username or a team will notify them.

\- URLs:
URLs are converted to links.

\- Strikethrough:

    --strikethrough--
    
\- Emoji:
GitHub supports most [Emojis](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)
