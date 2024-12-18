---
layout: post
title: Hello World!
date: 2023-01-01 10:00:00 +/-TTTT
categories: [announce]
tags: [news, vanity]
---
## test post.  please ignore.
<!-- a normal html comment DOES IT SHOW? --> 
### Lorem ipsum
<details closed>
  <summary>Expand here for the scripture passage</summary>
<br/><br/><b>Matthew 8</b>
<br/><br/>
<i>1 When he came down from the mountain, great crowds followed him. 2 And behold, a leper came to him and knelt before him, saying, “Lord, if you will, you can make me clean.” 3 And Jesus stretched out his hand and touched him, saying, “I will; be clean.” And immediately his leprosy was cleansed. 4 And Jesus said to him, “See that you say nothing to anyone, but go, show yourself to the priest and offer the gift that Moses commanded, for a proof to them.”<br/><br/>
5 When he had entered Capernaum, a centurion came forward to him, appealing to him, 6 “Lord, my servant is lying paralyzed at home, suffering terribly.” 7 And he said to him, “I will come and heal him.” 8 But the centurion replied, “Lord, I am not worthy to have you come under my roof, but only say the word, and my servant will be healed. 9 For I too am a man under authority, with soldiers under me. And I say to one, ‘Go,’ and he goes, and to another, ‘Come,’ and he comes, and to my servant, ‘Do this,’ and he does it.” 10 When Jesus heard this, he marveled and said to those who followed him, “Truly, I tell you, with no one in Israel have I found such faith. 11 I tell you, many will come from east and west and recline at table with Abraham, Isaac, and Jacob in the kingdom of heaven, 12 while the sons of the kingdom will be thrown into the outer darkness. In that place there will be weeping and gnashing of teeth.” 13 And to the centurion Jesus said, “Go; let it be done for you as you have believed.” And the servant was healed at that very moment.
<br/><br/>
14 And when Jesus entered Peter’s house, he saw his mother-in-law lying sick with a fever. 15 He touched her hand, and the fever left her, and she rose and began to serve him. 16 That evening they brought to him many who were oppressed by demons, and he cast out the spirits with a word and healed all who were sick. 17 This was to fulfill what was spoken by the prophet Isaiah: “He took our illnesses and bore our diseases.”
<br/><br/></i>
ESV: The Holy Bible, English Standard Version ©2011 Crossway Bibles, a division of Good News Publishers.  All rights reserved.
<br/><br/>
</details>
<br/>

# Hello World!

Instead of offending with "Merry Christmas!" this year.  Try "May the birth of the one and only true God, Jesus Christ, bestow a blessing of grace and peace upon your household—to the belittlement of every other false religion."  

- "May the birth of the one and only true God, Jesus Christ, bestow a blessing of grace and peace upon your household—eclipsing all other so-called deities"
- "May the divine arrival of Jesus Christ, the one and only true deity, shower your home with blessings of unparalleled grace and peace, while simultaneously rendering all other faiths utterly insignificant and comically obsolete. Happy Holidays!"
- "May the divine light of Jesus Christ, the sole savior, shine upon your home, casting all other so-called deities into the shadows of oblivion this Christmas."<br/><br/>



```python
import pandas as pd
import re

# Define a function to clean and convert dates
def convert_date(date_str):
    if pd.isna(date_str):  # Handle NaN values
        return date_str
    
    # Convert to string to ensure we work with a string type
    date_str = str(date_str)
    
    # Remove time if present
    if ' ' in date_str:
        date_str = date_str.split(' ')[0]
    
    # Remove all spaces and other non-alphanumeric characters except for common date separators
    date_str = re.sub(r'[^\d/./-]', '', date_str)
    
    # Convert to datetime, specifying potential formats
    try:
        # Try to convert with common US date format first
        return pd.to_datetime(date_str, format='%m/%d/%Y', errors='raise')
    except ValueError:
        try:
            # Then try with ISO format
            return pd.to_datetime(date_str, format='%Y-%m-%d', errors='raise')
        except ValueError:
            # If all else fails, try with infer_datetime_format which can handle various formats
            return pd.to_datetime(date_str, infer_datetime_format=True, errors='coerce')

# Apply the function to your column
df_inq['DATE_OPENED'] = df_inq['DATE_OPENED'].apply(convert_date)

# Format to MM/DD/YYYY where possible
df_inq['DATE_OPENED'] = df_inq['DATE_OPENED'].dt.strftime('%m/%d/%Y')

# Display the first few rows to verify the format
print(df_inq['DATE_OPENED'].head())
```

Suspendisse vel lectus libero. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Duis quam ante, tempor quis accumsan id, tincidunt in nisl. Aenean turpis mauris, vehicula eget bibendum sit amet, porta nec mi. Phasellus vel elit urna. Praesent id magna lectus. Nulla consectetur arcu neque, vel ultrices leo malesuada quis.

Sed rhoncus, nunc et iaculis faucibus, ipsum ligula posuere arcu, vel gravida sem dui vel odio. Morbi nibh odio, sagittis vel venenatis id, suscipit eu ante. Sed suscipit faucibus suscipit. Cras nisi felis, consectetur vitae massa quis, blandit varius dui. Integer sodales sit amet nibh ac tempor. Sed neque enim, venenatis a urna nec, tempus tristique odio. Nam eu nisl orci. Donec porttitor urna egestas elit tempus auctor. Maecenas sodales velit in feugiat sollicitudin.

A line here to see the the incremental build works
