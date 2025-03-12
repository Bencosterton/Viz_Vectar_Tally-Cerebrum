## This is how you get tallt info from Viz Vectar using EVS Cerebrum;

### Step 1 - Curl

Note: I have omited the Vectar username and password - Replace with your own. <br>
Note: I have ommited three values form the curl response (NONCE, CNONCE, and RESPONSE). You will need to copy these values form the curl response to the Cerebrum Header.

To obtain the authorisaiton values we can curl the endpoint of the Vectar Tally data;
```bash
curl -v --digest -u {VECTAR-USERNAME}:{VECTAR-PASSWORD} "http://{VECTAR-IP}/v1/dictionary?key=tally" -H "Accept: application/xml"
```

It will return the following;
```bash
*   Trying {VECTAR-IP}:80...
* Connected to {VECTAR-IP} ({VECTAR-IP}) port 80
* using HTTP/1.x
* Server auth using Digest with user '{VECTAR-USERNAME}'
> GET /v1/dictionary?key=tally HTTP/1.1
> Host: {VECTAR-IP}
> User-Agent: curl/8.10.1
> Accept: application/xml
>
< HTTP/1.1 401 Unauthorized
< Date: Wed, 12 Mar 2025 11:43:34 GMT
< Connection: close
< Content-Length: 0
< WWW-Authenticate: Digest qop="auth", realm="", nonce="{NONCE-VALUE}"
<
* shutting down connection #0
* Issue another request to this URL: 'http://{VECTAR-IP}/v1/dictionary?key=tally'
* Hostname {VECTAR-IP} was found in DNS cache
*   Trying {VECTAR-IP}:80...
* Connected to {VECTAR-IP} ({VECTAR-IP}) port 80
* using HTTP/1.x
* Server auth using Digest with user '{VECTAR-USERNAME}'
> GET /v1/dictionary?key=tally HTTP/1.1
> Host: {VECTAR-IP}
> Authorization: Digest username="{VECTAR-USERNAME}",realm="",nonce="{NONCE-VALUE}",uri="/v1/dictionary?key=tally",cnonce="{CNONCE-VALUE}",nc=00000001,response="{RESPONSE-VALUE}",qop="auth"
> User-Agent: curl/8.10.1
> Accept: application/xml
>
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: text/xml
< timestamp: 1281138546
< Access-Control-Allow-Origin: *
<
<tally>
  <column name="input1" index="0" on_pgm="false" on_prev="true" ndi_id="0" />
  <column name="input2" index="1" on_pgm="false" on_prev="false" ndi_id="1" />
  <column name="input3" index="2" on_pgm="false" on_prev="false" ndi_id="2" />
  <column name="input4" index="3" on_pgm="false" on_prev="false" ndi_id="3" />
  <column name="input5" index="4" on_pgm="false" on_prev="false" ndi_id="4" />
  <column name="input6" index="5" on_pgm="false" on_prev="false" ndi_id="5" />
  <column name="input7" index="6" on_pgm="false" on_prev="false" ndi_id="6" />
  <column name="input8" index="7" on_pgm="true" on_prev="false" ndi_id="7" />
  <column name="input9" index="8" on_pgm="false" on_prev="false" ndi_id="8" />
  <column name="input10" index="9" on_pgm="false" on_prev="false" ndi_id="9" />
  <column name="input11" index="10" on_pgm="false" on_prev="false" ndi_id="10" />
  <column name="input12" index="11" on_pgm="false" on_prev="false" ndi_id="11" />
  <column name="input13" index="12" on_pgm="false" on_prev="false" ndi_id="12" />
  <column name="input14" index="13" on_pgm="false" on_prev="false" ndi_id="13" />
  <column name="input15" index="14" on_pgm="false" on_prev="false" ndi_id="14" />
  <column name="input16" index="15" on_pgm="false" on_prev="false" ndi_id="15" />
  <column name="input17" index="16" on_pgm="false" on_prev="false" ndi_id="16" />
  <column name="input18" index="17" on_pgm="false" on_prev="false" ndi_id="17" />
  <column name="input19" index="18" on_pgm="false" on_prev="false" ndi_id="18" />
  <column name="input20" index="19" on_pgm="false" on_prev="false" ndi_id="19" />
  <column name="input21" index="20" on_pgm="false" on_prev="false" ndi_id="20" />
  <column name="input22" index="21" on_pgm="false" on_prev="false" ndi_id="21" />
  <column name="input23" index="22" on_pgm="false" on_prev="false" ndi_id="22" />
  <column name="input24" index="23" on_pgm="false" on_prev="false" ndi_id="23" />
  <column name="input25" index="24" on_pgm="false" on_prev="false" ndi_id="24" />
  <column name="input26" index="25" on_pgm="false" on_prev="false" ndi_id="25" />
  <column name="input27" index="26" on_pgm="false" on_prev="false" ndi_id="26" />
  <column name="input28" index="27" on_pgm="false" on_prev="false" ndi_id="27" />
  <column name="input29" index="28" on_pgm="false" on_prev="false" ndi_id="28" />
  <column name="input30" index="29" on_pgm="false" on_prev="false" ndi_id="29" />
  <column name="input31" index="30" on_pgm="false" on_prev="false" ndi_id="30" />
  <column name="input32" index="31" on_pgm="false" on_prev="false" ndi_id="31" />
  <column name="input33" index="32" on_pgm="false" on_prev="false" ndi_id="32" />
  <column name="input34" index="33" on_pgm="false" on_prev="false" ndi_id="33" />
  <column name="input35" index="34" on_pgm="false" on_prev="false" ndi_id="34" />
  <column name="input36" index="35" on_pgm="false" on_prev="false" ndi_id="35" />
  <column name="input37" index="36" on_pgm="false" on_prev="false" ndi_id="36" />
  <column name="input38" index="37" on_pgm="false" on_prev="false" ndi_id="37" />
  <column name="input39" index="38" on_pgm="false" on_prev="false" ndi_id="38" />
  <column name="input40" index="39" on_pgm="false" on_prev="false" ndi_id="39" />
  <column name="input41" index="40" on_pgm="false" on_prev="false" ndi_id="40" />
  <column name="input42" index="41" on_pgm="false" on_prev="false" ndi_id="41" />
  <column name="input43" index="42" on_pgm="false" on_prev="false" ndi_id="42" />
  <column name="input44" index="43" on_pgm="false" on_prev="false" ndi_id="43" />
  <column name="bfr1" index="44" on_pgm="false" on_prev="false" />
  <column name="bfr2" index="45" on_pgm="false" on_prev="false" />
  <column name="bfr3" index="46" on_pgm="false" on_prev="false" />
  <column name="bfr4" index="47" on_pgm="false" on_prev="false" />
  <column name="bfr5" index="48" on_pgm="false" on_prev="false" />
  <column name="bfr6" index="49" on_pgm="false" on_prev="false" />
  <column name="bfr7" index="50" on_pgm="false" on_prev="false" />
  <column name="bfr8" index="51" on_pgm="false" on_prev="false" />
  <column name="bfr9" index="52" on_pgm="false" on_prev="false" />
  <column name="bfr10" index="53" on_pgm="false" on_prev="false" />
  <column name="bfr11" index="54" on_pgm="false" on_prev="false" />
  <column name="bfr12" index="55" on_pgm="false" on_prev="false" />
  <column name="bfr13" index="56" on_pgm="false" on_prev="false" />
  <column name="bfr14" index="57" on_pgm="false" on_prev="false" />
  <column name="bfr15" index="58" on_pgm="false" on_prev="false" />
  <column name="ddr1_a" index="59" on_pgm="false" on_prev="false" />
  <column name="ddr1_b" index="60" on_pgm="false" on_prev="false" />
  <column name="ddr2_a" index="61" on_pgm="false" on_prev="false" />
  <column name="ddr2_b" index="62" on_pgm="false" on_prev="false" />
  <column name="ddr3_a" index="63" on_pgm="false" on_prev="false" />
  <column name="ddr3_b" index="64" on_pgm="false" on_prev="false" />
  <column name="ddr4_a" index="65" on_pgm="false" on_prev="false" />
  <column name="ddr4_b" index="66" on_pgm="false" on_prev="false" />
  <column name="ddr1" index="67" on_pgm="false" on_prev="false" />
  <column name="ddr2" index="68" on_pgm="false" on_prev="false" />
  <column name="ddr3" index="69" on_pgm="false" on_prev="false" />
  <column name="ddr4" index="70" on_pgm="false" on_prev="false" />
  <column name="v1" index="71" on_pgm="false" on_prev="false" />
  <column name="v2" index="72" on_pgm="false" on_prev="false" />
  <column name="v3" index="73" on_pgm="false" on_prev="false" />
  <column name="v4" index="74" on_pgm="false" on_prev="false" />
  <column name="v5" index="75" on_pgm="false" on_prev="false" />
  <column name="v6" index="76" on_pgm="false" on_prev="false" />
  <column name="v7" index="77" on_pgm="false" on_prev="false" />
  <column name="v8" index="78" on_pgm="false" on_prev="false" />
  <column name="preview" index="79" on_pgm="false" on_prev="false" />
  <column name="me_preview" index="80" on_pgm="false" on_prev="false" />
  <column name="me_follow" index="81" on_pgm="false" on_prev="false" />
  <column name="previz" index="82" on_pgm="false" on_prev="false" />
  <column name="web_follow" index="83" on_pgm="false" on_prev="false" />
  <column name="sound" index="-2" on_pgm="false" on_prev="false" />
  <column name="black" index="-1" on_pgm="false" on_prev="false" />
</tally>* abort upload
* shutting down connection #1
```


## Step 2 - Cerebrum


In Cerebrum, you will need to use the following setup;<br>
Device: raw http request client<br>
IP: {VECTAR-IP}<br>
Port: 80<br>

Path:
```bash
/v1/dictionary?key=tally
```

Header:
```bash
Authorization: Digest username="{VECTAR-USERNAME}", realm="", nonce="{NONCE-VALUE}", uri="/v1/dictionary?key=tally", cnonce="{CNONCE-VALUE}", nc=00000001, response="{RESPONSE-VALUE}", qop="auth"
```

Use the 'GET' function from 'raw http client' device to obtain the tally values.
