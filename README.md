## Fork by vim-scripts/taglist.vim
#### This fork fix some bugs.
bugs:  
fix bugs in Tlist_Refresh_Folds

```
diff --git a/plugin/taglist.vim b/plugin/taglist.vim
old mode 100644
new mode 100755
index 59901f6..2d1d26b
--- a/plugin/taglist.vim
+++ b/plugin/taglist.vim
@@ -4097,6 +4097,10 @@ endfunction
 " window. Used after entering a tab. If this is not done, then the folds
 " are not properly created for taglist windows displayed in multiple tabs.
 function! s:Tlist_Refresh_Folds()
+    if g:Tlist_Show_One_File
+    	return
+    endif
+
     let winnum = bufwinnr(g:TagList_title)
     if winnum == -1
         return
```

## original readme: ##
This is a mirror of http://www.vim.org/scripts/script.php?script_id=273

The "Tag List" plugin is a source code browser plugin for Vim and
provides an overview of the structure of source code files and allows
you to efficiently browse through source code files for different
programming languages.  You can visit the taglist plugin home page for
more information:

      http://vim-taglist.sourceforge.net

You can subscribe to the taglist mailing list to post your questions
or suggestions for improvement or to report bugs. Visit the following
page for subscribing to the mailing list:

      http://groups.yahoo.com/group/taglist/

For more information about using this plugin, after installing the
taglist plugin, use the ":help taglist" command.
