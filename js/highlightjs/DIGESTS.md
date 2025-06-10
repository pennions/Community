## Subresource Integrity

If you are loading Highlight.js via CDN you may wish to use [Subresource Integrity](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) to guarantee that you are using a legimitate build of the library.

To do this you simply need to add the `integrity` attribute for each JavaScript file you download via CDN. These digests are used by the browser to confirm the files downloaded have not been modified.

```html
<script
  src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/11.11.1/highlight.min.js"
  integrity="sha384-5xdYoZ0Lt6Jw8GFfRP91J0jaOVUq7DGI1J5wIyNi0D+eHVdfUwHR4gW6kPsw489E"></script>
<!-- including any other grammars you might need to load -->
<script
  src="//cdnjs.cloudflare.com/ajax/libs/highlight.js/11.11.1/languages/go.min.js"
  integrity="sha384-HdearVH8cyfzwBIQOjL/6dSEmZxQ5rJRezN7spps8E7iu+R6utS8c2ab0AgBNFfH"></script>
```

The full list of digests for every file can be found below.

### Digests

```
sha384-gRTR/fmk+6+ygbihH/fJvHgmffnOrd/eO7DW5zgu1uN9GBohtDx+OBs0DI0ejigB /es/languages/bash.js
sha384-Pg7b9hYE6kefjcNqAabhv8jOLCVoZubUaM4bZFjUJd0CaaQ14ksDI0GVllMtAF4S /es/languages/bash.min.js
sha384-Gmvct15f4Mo9AXQG5bk5w78N1YjBLXXU3KIV7no+mOVnApXlwfw1dwjfueAwljIV /es/languages/css.js
sha384-1D7DbOic0Z5nM2ldSO9O/EsBfsg/5x7X7So1qnMgscI2ucDevptcg7cTvrD9rL0D /es/languages/css.min.js
sha384-g7t9fKR5Tvod4iWv7BQXN+/JMn5GT9sD6FG3h7Fgl+KCv5k4NnnCzEqUe7BMJ9Mv /es/languages/javascript.js
sha384-f7huPivS1dV2T5V+g0aJpgsY7WBHWCsioIq30tpNoXGizD65fWJYGuXXVPNI52VB /es/languages/javascript.min.js
sha384-8CRS96Xb/ZkZlQU+5ffA03XTN6/xY40QAnsXKB0Y+ow1vza1LAkRNPSrZqGSNo53 /es/languages/json.js
sha384-UHzaYxI/rAo84TEK3WlG15gVfPk49XKax76Ccn9qPWYbUxePCEHxjGkV+xp9HcS/ /es/languages/json.min.js
sha384-4OPZSHQbxzPqFMOXnndxQ6TZTI/B+J4W9aqTCHxAx/dsPS6GG25kT7wdsf66jJ1M /es/languages/php.js
sha384-VxmvZ2mUpp1EzFijS40RFvIc7vbv/d5PhMxVFG/3HMpVKD4sVvhdV9LThrJDiw9e /es/languages/php.min.js
sha384-Cmq5lORXzyHraasLNqmfchH07JRXyEmjDF+j6tSggoXjYHwtgX/ySW6kkRytM5uu /es/languages/python.js
sha384-ZV5sgX70bBgLkDR5Mtox5UsbJedBc39hRKPdvTw6miK4lSkE/wv94cLY2iyZb/sB /es/languages/python.min.js
sha384-s1ZfN6xtlNKAZux8QYAG7upUsit3RwK5XDoCAN3g6Kj33RrIqbmkuGjdNF9RvzPM /es/languages/sql.js
sha384-y25cn06synxhYnlKVprZdpakuFWVrm2jvn8pqiF4L85a05CI/6bNeT2+qXbUYIyW /es/languages/sql.min.js
sha384-Z61gsCS2W7Q+3fT1fdya/Sz4wlmsotT9iEGzgIlNqP0soaKH1NzysutxWp08Hh3E /es/languages/typescript.js
sha384-Tv4mr9B7b+x2IynRXW/xcAxUj1+AoN9zyp0n9BWE1Nle3Zfm/zUeEztNLhIRjgE7 /es/languages/typescript.min.js
sha384-82eHXc3kQTsEJ65AcO2c8eVqB9ynJzosSiMwdPYwt5oNRVsMKuxWoWkO5KFekVYB /es/languages/wasm.js
sha384-YBbT3eXpwj5Ddx0MS774iycYICw4gZ1Rs1ExYGIdcYC4EJhaWsfd9uNlaJZBuDaa /es/languages/wasm.min.js
sha384-Jrkpn2hK0TY04skYBXB9fj7mMpKYy7g726cPwXGXf6mdBXnFlTDXFduxikMCRXT7 /languages/bash.js
sha384-BbT8tZtvkh8HPXIvL5RtzuljBwI3gR5KIdYxZyYSyI5C/+KNAGdzAiexvmxuroag /languages/bash.min.js
sha384-bsb3QmLtUiyaiHwtrL4YoAVI9yLsjyqxgoAsk4Zd+ass9rSK1WWRiCDSu/hm8QRp /languages/css.js
sha384-0XGvxIU7Oq1DQMMBr1ORiozzBq3KpZPE/74mJysWRBAop1dZ9Ioq/qRWe8u30Ded /languages/css.min.js
sha384-yxv7Fv9ToggiLsR67t98hV5ZRup6XX6xL1Rkbi/cGV5J8y7fosCi9POqlBkiBWFg /languages/javascript.js
sha384-tPOrIubtDHoQU7Rqw0o88ilthGO0/4xEZGB47XrQKWhrc1/SchwsDx+AP74u4nk0 /languages/javascript.min.js
sha384-pUlqdjoNePvHvdi7GVKJJnh/P2T3EvXXodl5j0JtTkbNC4DRH7gwGbcHFa84bFOP /languages/json.js
sha384-3C+cPClJZgjKFYAb0bh35D7im2jasLzgk9eRix3t1c5pk1+x6b+bHghWcdrKwIo3 /languages/json.min.js
sha384-0XBmTxpMLuDjB2zdfbi3Lv4Yokm2e1YFGZ9mCmI5887Kpi23jMF5N7rPrf0GdoU/ /languages/php.js
sha384-Bv/Sxv6HlOzYOdV1iQpJTG3xiqGWIIMq9xsFfEX8ss7oNWMgKqOa/J2WSFG2m7Jd /languages/php.min.js
sha384-ueSSFZFqg7cVD0dpEqIk9EefJiJUYan0PH6I8u/p+bNLLx7dMs4J2keMaFXqCN8P /languages/python.js
sha384-eXRt+aAa2ig1yFVDQCLis8k9s/1dikTcigj+/R07yNdIxc8BAG/b1uHDyEW3of17 /languages/python.min.js
sha384-2sXmcW3eKeNDWiLtuq9NgFJC4NsLBN/fDTzZevmcgBrSERv6iO/k+c7r9T09Fb8J /languages/sql.js
sha384-jrnLoVn13sB+/dTfoAYVPhg0tYGQzzuzSGP3WTk8OvKAY0hDejpUXFYYI3bohAyW /languages/sql.min.js
sha384-8v3YMaXFO9cmTNxsHWqwn9wJsV1jVO7rwx4huxqlEQpT/P2tuDbtm+Hs0EdYqu0a /languages/typescript.js
sha384-df1w1nJ43GNwmgbSCrT8YFIYyqFAm+lzj+b6ofuziX8Cfdg9QHFwbORDgAaj//wi /languages/typescript.min.js
sha384-TCN/hvup/XKpDtGmR/RyK6NSG247wkNROUpO2sAoJuwpMvcr4KP9HA+K5L2rvOKg /languages/wasm.js
sha384-J3pUKFGnHJH0czAle+lKF96F/08caYKJfTEzlt5dGbGTR9M4BwOeOqAgvSzsjOsP /languages/wasm.min.js
sha384-J95k4LejYH373YAxjicOnKQkv+77W/R7ag6yf9oEGKWFUqW8N4+X5lbSqP7nknG0 /highlight.js
sha384-f11I8JaNSvlRIvCGb7ZE4K9vFdKNEkQJ0iE5oOtiMnt/5nIUbECp2Brmp2R9BY53 /highlight.min.js
```

