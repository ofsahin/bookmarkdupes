# bookmarkdupes

(C) Martin Väth <martin@mvath.de>

This project is under the GNU Public License 2.0.

A WebExtension which can display/remove duplicate bookmarks, empty folders, or descriptions

After installing bookmarkdupes, the usage is rather simple:

Click on bookmardupes' symbol (duplicate stars) and then
select in the popup window what you want to display:

1. Bookmark duplicates (exact)
2. Bookmark duplicates (similar)
3. Empty folders
4. All bookmarks

The difference between 1 and 2 is that in case

1. The URLs of the bookmarks must match exactly
2. The URLs of the bookmarks must match up to the first ? symbol;
   the URL text after the ? symbol is appended to the displayed bookmark.

After this, you will be offered the list of bookmarks with checkboxes;
in case 1 and 2 numbers indicate the order in which matching bookmarks
were added according to the internally stored date.
There are also buttons to select/unselect convenient sets of checkboxes.

Finally, there are buttons to remove the selected bookmarks in case 1-3,
or to strip the descriptions of the selected bookmarks in case 4.
(The latter has some side effects, see section **Known Bugs**).

#### Note
When you close the popup window and removal of bookmarks/descriptions is not
yet finished, it will continue in the background.

## Important

When you reorganized/added/removed bookmarks, make sure to update the
displayed list (by pressing the corresponding button) before removing
bookmarks or stripping descriptions!
In particular, stripping descriptions with an outdated list will move
the corresponding bookmarks to their previous location in the bookmark menu!

## Known Bugs

1. Certain special folders (e.g. rss folders) are not distinguished from
   empty folders.
   https://github.com/vaeth/bookmarkdupes/issues/4
2. Stripping of descriptions works by replacing the bookmark by a freshly
   created one. In particular, it updates the internally stored date when
   the bookmark was added.
3. In certain situations, it might happen that the procedure of creating a
   new bookmark (when stripping descriptions, see bug 2 above) places the
   freshly created bookmark to a wrong location. In particular, this might
   happen in connection with special folders/bookmarks as in 1 or when
   an outdated list is used.
   https://github.com/vaeth/bookmarkdupes/issues/11 and the second part of
   https://github.com/vaeth/bookmarkdupes/issues/8

## Contributions

(in alphabetical order)

- Henaro aka Ironwool https://github.com/perdolka (Russian and Ukrainian translation)
- Juan Salvador Aleixandre Talens https://github.com/juaalta (Spanish translation)
- YFdyh000 <yfdyh000 at gmail.com> https://github.com/yfdyh000 (Simplified Chinese translation)
