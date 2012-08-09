Quick Usage Guide
---

###Global Options - Default Values:

*  Default Title   	- The title tag content to use if no title tag is found
*  Default Keywords 	- The keywords to use if no keyword content is found
*  Default Description 	- The description content to use if no description is found

Also note that title, keywords and description tags will fallback to the entry_id
corresponding to the last uri segment, if it exists, before falling back to the
defaults in the module control panel.

###Global Options - Additional Options
* Prepend to all title tags 	 - Any content to add before all site title tags created via the module. You may need to add spaces after the text as necessary
* Append to all title tags		 - Any content to add after all site title tags created via the module. You may need to add spaces before the text as necessary
* Visbility to robots (privacy) - Set the ROBOTS meta tag as appropriate


###Tags
Sample tags. Note that any parameters surrounded by square brackets "[ ]" are optional. Square brackets seen below should not be used within templates.

####Title

    {exp:seo:title [entry_id="{entry_id}"] [prepend="override prepend"] [append="override append"] [fallback="override fallback title text"]}

Sample Output:

    An Article - MySite.com

Note that use of prepend / append parameters will override the global append / prepend options.  If defined, fallback text will be used in the case that a title is not defined in the seo tab of the entry.  Otherwise,
text will fallback to the title of the entry first, then to the default title text defined in seo's settings.

####Keywords

    {exp:seo:keywords [entry_id="{entry_id}"]}

Sample Output:

    these,are,my,keywords

####Descriptions

    {exp:seo:description [entry_id="{entry_id}"]}

Sample Output:

    This is my short description that will show up in the SERPS

####Canonical Links

    {exp:seo:cononical url="{title_permlink='some/template'}"}

Sample Output:

    <link rel="canonical" href="http://mysite.com/template/a_specific_article" />

####NoIndex, NoFollow

    {exp:seo:privacy}

Sample Output:

    <meta name="robots" content="index,follow" />