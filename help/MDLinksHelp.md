###Markdown Links Workflow help  
===
The **Markdown Links Worklow** allows you to easily copy formatted mardown links to your clipboard for easy pasting. 
<BR>  
  
![MD Links](https://raw.githubusercontent.com/unforswearing/images/master/MDLinksAlfred.gif)  

<BR>


###Usage  

There are three types of links this workflow can handle:  
  
Keyword `mdlink` will copy a standard markdown link to your clipboard.   

- To use, enter `mdlink yourtext`
- A markdown link `[yourtext](url)` will be copied. 


Keyword `mdimage` will copy a mardkown formatted image to your clipboard. 

- To use, enter keyword `mdimage youralttext`
- An image link  `![youralttext](img url)` will be copied. 

Keyword `mdclick` will copy a click-through image link to your clipboard. 

- To use, enter `mdclick yourclickthroughlink` 
- The link `[![img url][1]][2]` (and corresponding `[1]` and `[2]` footnote links) will be copied. 
- `[1]` will be the link copied from your clipboard (`img url`) and `[2]` is the destination link you specify (`yourclickthroughlink`). 
- The output will appear as:

> [![img url][1]][2]  
> 
> [1]: img url    
> [2]: your click through link  

###To Do  

Suggestions for improvement are always welcome.  
