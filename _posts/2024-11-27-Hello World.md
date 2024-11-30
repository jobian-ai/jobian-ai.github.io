---
layout: post
title: Hello World!
date: 27 11 2024
categories: [Announcements]
tags: [news, vanity]
---


## This is my first post.

### Lorem ipsum

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
