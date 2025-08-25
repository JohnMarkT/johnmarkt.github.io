---
layout: post
title: Bookmarklets
---

To use, drag button to bookmarks bar first.

[root](javascript:location.href=location.origin){: .btn }
Go to root of current website

[SSL](javascript:((l,h,hs)=>{l.protocol=l.protocol==h?hs:h;})(location,'http:','https:')){: .btn }
Toggle SSL of current URL

[clear qs](javascript:(l=>{l.href=l.origin+l.pathname})(location)){: .btn }
Remove query string parameters of current URL

[cache bust](javascript:((p,l,s)=>{p=new URLSearchParams(l[s]);p.set('_cb',Date.now());l[s]=p})({},location,'search')){: .btn}
Bust site's cache by adding timestamp to query string

[del el](javascript:((j,b)=>{j.t=!j.t;const f=j.t?b.addEventListener:b.removeEventListener;console.log('remove mode %s',j.t?'on':'off');j.rE=j.rE||(e=>{const el=e.target;e.preventDefault();console.log('removing:',el);el.parentNode.removeChild(el);});f('click',j.rE,0);})(window.JMT=window.JMT||{},document.body)){: .btn}
Delete element from page -- click again to disable
