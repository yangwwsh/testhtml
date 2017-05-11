# Exploring DITA Open Tool
## Preparations
1. Get `dita-ot` here: http://www.dita-ot.org/
2. Get the markdown parser plugin here: https://github.com/jelovirt/dita-ot-markdown
3. Add the dita-ot path (`<dita-ot dir>\bin;`) into the `PATH` system variable 
3. Change the document type declaration of IBM dita topics to the standard OASIS document types    
   Note: This is because the open toolkit only support the industry standard doc types (IBM DTD has IBM customizations based on standard)
   From
   ```
   <!DOCTYPE concept PUBLIC "-//IBM//DTD DITA IBM Concept//EN" "ibm-concept.dtd">
   ```
   to
   ```
   <!DOCTYPE concept PUBLIC "-//OASIS//DTD DITA Concept//EN" "concept.dtd">
   ```
   Similar to the other document types.

## Build output
In the command shell, run `dita --input=input-file --format=format options`
The jelovirt markdown plugin has the following output format options:  
- `markdown`: publish Markdown DITA files
- `markdown_github`: generate GitHub Flavored Markdown files
- `markdown_gitbook`: publish GitHub Flavored Markdown and generate a SUMMARY.md table of contents file for publication via GitBook
For more information about how to use the arguments, see http://www.dita-ot.org/dev/user-guide/build-using-dita-command.html

## Check my test result
You can start from the top-level topic
[apigw_overview.md](apigw_overview.md)
