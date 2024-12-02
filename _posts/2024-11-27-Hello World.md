---
layout: post
title: Hello World!
date: 2024-12-02 10:00:00 +/-TTTT
categories: [Announcements]
tags: [news, vanity]
---


## This is my first post.

### Lorem ipsum

<details closed>
  <summary>Passage</summary>
Matthew 8
<br/><br/>
1 When he came down from the mountain, great crowds followed him. 2 And behold, a leper came to him and knelt before him, saying, “Lord, if you will, you can make me clean.” 3 And Jesus stretched out his hand and touched him, saying, “I will; be clean.” And immediately his leprosy was cleansed. 4 And Jesus said to him, “See that you say nothing to anyone, but go, show yourself to the priest and offer the gift that Moses commanded, for a proof to them.”<br/><br/>
5 When he had entered Capernaum, a centurion came forward to him, appealing to him, 6 “Lord, my servant is lying paralyzed at home, suffering terribly.” 7 And he said to him, “I will come and heal him.” 8 But the centurion replied, “Lord, I am not worthy to have you come under my roof, but only say the word, and my servant will be healed. 9 For I too am a man under authority, with soldiers under me. And I say to one, ‘Go,’ and he goes, and to another, ‘Come,’ and he comes, and to my servant, ‘Do this,’ and he does it.” 10 When Jesus heard this, he marveled and said to those who followed him, “Truly, I tell you, with no one in Israel have I found such faith. 11 I tell you, many will come from east and west and recline at table with Abraham, Isaac, and Jacob in the kingdom of heaven, 12 while the sons of the kingdom will be thrown into the outer darkness. In that place there will be weeping and gnashing of teeth.” 13 And to the centurion Jesus said, “Go; let it be done for you as you have believed.” And the servant was healed at that very moment.
<br/><br/>
14 And when Jesus entered Peter’s house, he saw his mother-in-law lying sick with a fever. 15 He touched her hand, and the fever left her, and she rose and began to serve him. 16 That evening they brought to him many who were oppressed by demons, and he cast out the spirits with a word and healed all who were sick. 17 This was to fulfill what was spoken by the prophet Isaiah: “He took our illnesses and bore our diseases.”

ESV: The Holy Bible, English Standard Version ©2011 Crossway Bibles, a division of Good News Publishers.  All rights reserved.
___
</details>

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi dui augue, convallis eget dui vitae, dignissim tincidunt purus. Mauris a efficitur dui. Ut nec finibus tellus. Donec eu est et odio elementum semper in eget turpis. Phasellus eget porta lacus. Nulla cursus lectus quis bibendum feugiat. Nam varius enim vel mi tempor hendrerit. Cras commodo tincidunt orci sed cursus. Suspendisse non varius dui, non sollicitudin quam.

### [Link Test](https://github.com/jobian-ai/LHP-Sermons/tree/17743a2fdbf663aae26fce92de47bcdde298ac2a/sermons/24-01-14)

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

Curabitur rutrum at neque vel ultrices. Ut quis molestie magna. Vivamus non lacus sem. Integer ut ex nec leo hendrerit finibus eget vel magna. Donec eu eros sed nulla imperdiet rhoncus. Maecenas est ante, condimentum vitae justo sed, mollis laoreet mi. Phasellus eleifend tellus ipsum, in interdum nisl varius et. Aliquam orci orci, euismod sit amet viverra eget, bibendum eget tellus. Nullam bibendum mi ornare ligula accumsan condimentum. Nullam malesuada et ante in euismod. Curabitur maximus lobortis biblendum.

Curabitur venenatis dui varius turpis fermentum porttitor. Vivamus hendrerit augue sed mauris facilisis placerat. Morbi in dapibus eros. Ut odio urna, tempor quis quam eu, sodales dapibus nunc. Mauris porttitor arcu a mauris pulvinar, ut aliquam quam luctus. Curabitur sodales metus dui, et lobortis ex varius et. Suspendisse ultricies mi velit, in ullamcorper justo vestibulum et. Quisque lobortis sed urna vitae hendrerit. Donec suscipit quam ex, sit amet lacinia magna volutpat ut. Nam molestie malesuada vulputate. Pellentesque non erat eu lacus dignissim ultricies sit amet quis dui. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Aenean enim metus, sodales ut lacinia eu, condimentum eu arcu. Fusce eu nulla ut velit sollicitudin auctor vitae in metus. Duis quis est.

A line here to see the the incremental build works
