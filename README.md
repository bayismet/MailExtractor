# MailExtractor
To extract mails from a website.

It is a C# library.This library gives you a hand about finding and listing e-mails in a website. It just gives the addresses at a single webpage. However, you can modify it to get mail addresses from multi-links.

How It Works

It works very simply. It gets the source code of a website as html, find matches (e-mails) via RegEx, then put it in a "MatchCollection". Then, for every "Match" in "MatchCollection", it adds the "Match" to mail's body. Then send it to the address that you want.

How To Use

It's very simple to use.First you should create a "MailInfos" object. Then fill its properties by hand or from a form. Finally,you should invoke the "execute" function, in "func" class. To invoke it, you should give it a "MailInfos" object and a website.

Example

A website : "https://eksisozluk.com/ilginc-e-mail-adresleri--1434320"

It's innerhtml (I shorted it a little bit): 
<!doctype html>
<html lang="tr">
<head>
   <ul id="entry-list">
<li data-id="8726330" data-author="cyco" data-author-id="95631" data-flags="share report vote" data-isfavorite="false" data-favorite-count="1" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    <a rel="nofollow noopener" class="url" target="_blank" href="http://www.walla.com/">http://www.walla.com/</a> dan alınmış 3 gigabyte'lık yemin@walla.com...
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/8726330">18.12.2005 12:07</a>
      
      <a class="entry-author" href="/biri/cyco">cyco</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><li data-id="8726347" data-author="woodstock" data-author-id="35406" data-flags="share report vote" data-isfavorite="false" data-favorite-count="0" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    bir zamanlar iletilen e-postalar sayesinde öğrendiğimiz e-posta adresleridir (daha fazla bilgi için lütfen e-posta servisinizin <a class="b" href="/?q=%c3%a7%c3%b6p+kutusu">çöp kutusu</a>nu karıştırınız).
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/8726347">18.12.2005 12:10 ~ 12:11</a>
      
      <a class="entry-author" href="/biri/woodstock">woodstock</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><li data-id="12555616" data-author="huor elensar" data-author-id="380318" data-flags="share report vote" data-isfavorite="false" data-favorite-count="1" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    sevmisim_vermiyorlaryourname@example.com<br/><br/>yourname@ bölümünü zorunlu sanmış olmalı.
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/12555616">12.02.2008 01:35 ~ 11.09.2008 20:11</a>
      
      <a class="entry-author" href="/biri/huor-elensar">huor elensar</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><li data-id="16289507" data-author="boolenickmiolur" data-author-id="526670" data-flags="share report vote" data-isfavorite="false" data-favorite-count="0" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    adimgobekadimsoyadim@tirtmail.com
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/16289507">07.06.2009 04:02</a>
      
      <a class="entry-author" href="/biri/boolenickmiolur">boolenickmiolur</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><li data-id="17524428" data-author="jondaff" data-author-id="326375" data-flags="share report vote" data-isfavorite="false" data-favorite-count="1" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    karı koca olarak adres alanların adresleri misal. az önce gördüm. karı koca aliayseyılmaz@gmail.com gibisinden mail almışlar. mail göndermişler herkeslere. işte gerçek aşk bu. gezin yapışık ikiz gibi
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/17524428">15.12.2009 23:48</a>
      
      <a class="entry-author" href="/biri/jondaff">jondaff</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><div class="ad-adforminviewvideoad ads" data-info="{&quot;Name&quot;:&quot;AdFormInViewVideoAd&quot;,&quot;DisplayTypes&quot;:4}"><div id="adform-outstream" style="height:0;overflow:hidden"><script data-pmp-id="253317" language="javascript" src="//s1.adform.net/banners/scripts/video/outstream/inview.js"></script></div></div><li data-id="20312946" data-author="gotik sirin" data-author-id="570737" data-flags="share report vote" data-isfavorite="false" data-favorite-count="0" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    neytavuk_hayvanmi@xxx.com<br/><br/>evet bu gerçek bir mail adresi
  </div>
  <footer>
    <div class="feedback"></div><div class="info">
      <a class="entry-date permalink" href="/entry/20312946">13.09.2010 14:00</a>
      
      <a class="entry-author" href="/biri/gotik-sirin">gotik sirin</a>
    </div>
  </footer>
  <div class="comment-summary">
  <div class="comment-pages">
  </div>
</div>
</li><li data-id="21187090" data-author="jaja" data-author-id="494599" data-flags="share report vote" data-isfavorite="false" data-favorite-count="0" data-seyler-slug="" data-comment-count="0">
  <div class="content">
    g_sivrisinek@falancamail.com<br/><br/>insanlığından memnun olmayan bir arkadaş olsa gerek. <sup class="ab"><a title="(bkz: swh)" href="/?q=swh" data-query="swh">*</a></sup>
  </div>

</div></body>
</html>

An example mail (Splitted by ", "(includes space)): Bodyyemin@walla.com, yemin@walla.com, yemin@walla.com, sevmisim_vermiyorlaryourname@example.com, adimgobekadimsoyadim@tirtmail.com, lmaz@gmail.com, neytavuk_hayvanmi@xxx.com, g_sivrisinek@falancamail.com, pilavustu@xxx.com, ateshlipilich@xxx.com, pirzola@kasapnuri.com.tr,
