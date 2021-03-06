# Install application
1) Use npm install 
2) Type "npx ts-node parserxmlfile" in console where this file is stored
(alternative : npm start)

# How it works ?
1) Application takes xml file and creates valid copy
2) Application check if offer is avialable in current hour (no timezone) and adds to offer "is_active" attribute (boolean value)

# Result
1) In console you should be able to see two console logs (Offers which are active and inactive)
2) You should be able to see and open file "feed_out.xml" in catalog where .ts file is stored


## Examples

Example XML node in input file:
```
<offer>
        <id><![CDATA[7684]]></id>
        <name><![CDATA[Incredible Frozen Pants]]></name>
        <category><![CDATA[Tasty]]></category>
        <description><![CDATA[Atque delectus consequatur quod tempore et est sapiente et quia odio possimus eius ut et similique vero ipsam velit debitis ipsa optio sequi aliquam eius dolorum aut autem error tenetur et mollitia excepturi nihil facilis tempora ipsum sunt dignissimos natus molestiae veritatis velit eaque impedit quibusdam nesciunt sunt non laborum eos est aliquam porro fuga omnis qui explicabo vero rerum debitis perferendis in ut quis quia eveniet cum et nisi eveniet et unde nesciunt ratione qui asperiores soluta voluptatem possimus et ratione eum et cupiditate asperiores voluptatem quam id corporis natus ut eligendi consequuntur vel sunt fugit temporibus dolor iusto cumque repudiandae illum fugiat dignissimos sapiente esse cumque commodi repellendus vel et officiis animi iusto aliquam officiis qui quos doloremque dicta ab quia debitis ut dolores eaque hic dolorum rerum ut esse odit quo quia dolorem facere non non dolorum qui excepturi voluptatem totam minus reprehenderit ipsa rem et et nihil sunt repellat quo voluptatibus impedit in quod quis et natus cum ea officia sed ratione explicabo id atque aliquid cumque est voluptatibus cupiditate unde natus quia ut voluptatibus et consectetur libero saepe numquam amet eligendi qui vero mollitia est exercitationem quas nihil quas nihil debitis laboriosam totam reiciendis aut.]]></description>
        <price><![CDATA[331.69 EUR]]></price>
        <url><![CDATA[https://example.com/product/7684]]></url>
        <image_url><![CDATA[http://lorempixel.com/640/480]]></image_url>
        <opening_times><![CDATA[{"1":[{"opening":"10:00","closing":"21:00"}],"2":[{"opening":"10:00","closing":"21:00"},{"opening":"10:00","closing":"21:00"}],"3":[{"opening":"10:00","closing":"21:00"}],"4":[{"opening":"10:00","closing":"21:00"}],"5":[{"opening":"10:00","closing":"21:00"}],"6":[{"opening":"10:00","closing":"21:00"}],"7":[{"opening":"11:00","closing":"20:00"}],"timezone":"Europe/Warsaw"}]]></opening_times>
</offer>
```

Example XML node in output file:
```
<offer>
        <id><![CDATA[7684]]></id>
        <name><![CDATA[Incredible Frozen Pants]]></name>
        <category><![CDATA[Tasty]]></category>
        <description><![CDATA[Atque delectus consequatur quod tempore et est sapiente et quia odio possimus eius ut et similique vero ipsam velit debitis ipsa optio sequi aliquam eius dolorum aut autem error tenetur et mollitia excepturi nihil facilis tempora ipsum sunt dignissimos natus molestiae veritatis velit eaque impedit quibusdam nesciunt sunt non laborum eos est aliquam porro fuga omnis qui explicabo vero rerum debitis perferendis in ut quis quia eveniet cum et nisi eveniet et unde nesciunt ratione qui asperiores soluta voluptatem possimus et ratione eum et cupiditate asperiores voluptatem quam id corporis natus ut eligendi consequuntur vel sunt fugit temporibus dolor iusto cumque repudiandae illum fugiat dignissimos sapiente esse cumque commodi repellendus vel et officiis animi iusto aliquam officiis qui quos doloremque dicta ab quia debitis ut dolores eaque hic dolorum rerum ut esse odit quo quia dolorem facere non non dolorum qui excepturi voluptatem totam minus reprehenderit ipsa rem et et nihil sunt repellat quo voluptatibus impedit in quod quis et natus cum ea officia sed ratione explicabo id atque aliquid cumque est voluptatibus cupiditate unde natus quia ut voluptatibus et consectetur libero saepe numquam amet eligendi qui vero mollitia est exercitationem quas nihil quas nihil debitis laboriosam totam reiciendis aut.]]></description>
        <price><![CDATA[331.69 EUR]]></price>
        <url><![CDATA[https://example.com/product/7684]]></url>
        <image_url><![CDATA[http://lorempixel.com/640/480]]></image_url>
        <opening_times><![CDATA[{"1":[{"opening":"10:00","closing":"21:00"}],"2":[{"opening":"10:00","closing":"21:00"},{"opening":"10:00","closing":"21:00"}],"3":[{"opening":"10:00","closing":"21:00"}],"4":[{"opening":"10:00","closing":"21:00"}],"5":[{"opening":"10:00","closing":"21:00"}],"6":[{"opening":"10:00","closing":"21:00"}],"7":[{"opening":"11:00","closing":"20:00"}],"timezone":"Europe/Warsaw"}]]></opening_times>
        <is_active><![CDATA[true]]></is_active>
</offer>
```
