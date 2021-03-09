---
title: Subfile Paging

Id: amfSubfilePaging
TocParent: amfDdsSubfileClassUseSubfilePagingProperty
TocOrder: 290

keywords: Subfile Pages
keywords: MonarchSubfilePageChanged
keywords: MonarchSubfilePageChanging
keywords: Subfile Paging
keywords: Subfile AJAX

---

Subfile paging is controlled under the hood using [UseSubfilePaging='True'](http://www.w3schools.com/xml/ajax_intro.asp">AJAX</a>. When a subfile (<a href="amfDdsSubfileClassUseSubFilePagingProperty.html)), and the application has written more records than what are presented per page (<code>DdsSubfileControl</code>'s <code>SubfilePage</code> and <code>SubfileSize</code>), then the additional records are cached in the server controls.

When <code>PgDn</code> is invoked, there is an AJAX request to the server controls to fetch the next block of records (from the cache). When the response comes back, the HTML elements for the old records in the subfile are **removed** from the DOM and new ones are created.

If the developer adds attributes and/or other elements to the subfile records when the Page loads the first time, those elements/attributes will be lost by the AJAX response code - after <code>PgDn</code> or <code>PgUp</code> - (because the response handling code removes the subfile contents).

To solve that challenge, the Subfile AJAX implementation looks for the existence of the following GLOBAL JavaScript - user defined - functions:
<pre><code>
MonarchSubfilePageChanging(sflFmtName, sflId, from, to)</code>
</pre>
<pre><code>MonarchSubfilePageChanged(sflFmtName, sflId, from, to)
</code></pre>

<code>From</code> and <code>to</code> parameters to the function are the RRN numbers indicating the range of records, in case the handling code cares.

If the first callback exists, then **before** the elements in the subfile are replaced the function is called.

If the second callback exists, then right **after** the elements in the subfile have been replaced, the function is called.
