---
ID: 359
post_title: Mencoba snippet lagi
author: Muhammad Ikhsan
post_date: 2017-02-17 09:19:29
post_excerpt: ""
layout: snippet
permalink: >
  http://belajarpemrograman.app/snippet/mencoba-snippet-lagi/
published: true
---
Ini snippet mestinya
<pre data-line="2"><code class="language-php">function yx_shop_noindex_pages() {
  if (isset($_GET['orderby'])) {
    echo '&lt;meta name="robots" content="noindex, nofollow, noarchive"&gt;';
  }
}
add_action('wp_head', 'yx_shop_noindex_pages');</code></pre>