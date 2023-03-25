# Prayer API Documentation

## *This API is in development as of March 2023. Contact the author for more information or to contribute information to the prayer index.*

## Definition of Prayer
Keach's Catechism (1677) and other reputable catechisms ask the question, "What is Prayer?" The answer from Keach: "Prayer is an offering up of our desires to God, for things agreeable to His will, in the name of Christ, with confession of our sins and thankful acknowledgment of His mercies" (1 John 5:14; 1 John 1:9; Phil. 4:6; Ps. 10:17; 145:19; John 14:13,14).  
For the purposes of this project, "prayer" is additionally defined as: ***A human being addressing God who is in the heavens.*** This supplementary understanding of prayer in the Bible is necessary to explain why conversations with God such as Genesis 3:9-13 and Genesis 4:9 & 13-14 are omitted from the index.  
Finally, what is understood to constitute a prayer instance is based on the author's reading of the English Standard Version.

## The Purpose of the Prayer Index  
This index of ***every single prayer in the Bible*** and API are being produced in the hopes that developers will use it to create free or pay-what-you-will programs and applications saints use to foster deeper and more meaningful prayer lives. Whether for more actionable reminders or lists of prayer topics, this index and API can facilitate prayers that remain fresh and are grounded in God's Word.  
Please see Dr. Donald Whitney's book *Praying the Bible* to better understand why this index is so important and might help many saints and churches as they seek stronger prayer lives.

## Metadata  
    "updated":"2023-03-25",
    "categories":
	    ["confession", "exhortation", "imprecation", "intercession", "lament", "praise", "repentance", "supplication", "thanksgiving", "unknown"],
    "types":
	    ["command", "direct", "instruction", "reported"],
	"total-prayers":"20"

## Object Keys & Values  
1. **Identification Number - "id"**  
The first two numbers identify the book (e.g., "01" for Genesis and "66" for Revelation), then a hyphen "-" and three numbers follow to indicate the next prayer sequentially ("01-016" is the id for the last prayer in Genesis).
2. **Category - "category"**  
An array of values containing one or more of the following:
    - ***"confession"***  
    Confessing or repenting of sin(s).
    - ***"consecration"***  
    Dedicating for worship, for divine purposes.
    - ***"imprecation"***  
    Asking God to deliver judgement and recompense to His enemies.
    - ***"intercession"***  
    Interceding on behalf of another.
    - ***"lament"***
    Crying out to God in sorrow, always accompanied by trust that He hears, knows, and will make all things right.
    - ***"praise"***  
    Worshipping God with adoration for who He is and what He has done.
    - ***"supplication"***  
    Asking God for means, healing, rescue, fruit of the Spirit, aid, etc.
    - ***"thanksgiving"***  
    Showing gratitude to God for His bountiful blessings.
    - ***"unknown"***  
    Typically used when a prayer is reported but not described.
3. **Type - "type"**  
An array of values containing one or more of the following: 
    - ***"command"***  
    An imperative to pray in a certain manner or for certain things.
    - ***"direct"***  
    The exact, quoted words of a prayer.
    - ***"instruction"***  
    An exhortation to pray in a certain manner or for certain things.
    - ***"reported"***  
    An indirect reference to a prayer or habit of praying.
4. **Chapter - "chapter"**
    - The chapter containing the prayer.
5. **Verse(s) - "verse"**
    - The verse (e.g., *12*) or verses (e.g., *12-14*) containing the prayer.
6. **Verse Count - "verse-count"**
    - The total number of verses containing the prayer.
7. **Emulate? - "emulate"**
    - A boolean that is ***"true"*** when the prayer is a good example set for saints to emulate.
8. **Person - "person"**  
    - ***"first-s"***: first-person singular (I, my, *individual*)
    - ***"first-p"***: first-person plural (we, our, *corporate*)
    - ***"third-s"***: third-person singular (he, she)
    - ***"third-p"***: third-person plural (they)
9. **Comment(s) - "comment"**
    - Any extra information the author finds helpful.

## Example Response  
    {  
        "id":"64-001",
        "category":["intercession"],  
        "type":["reported"],  
        "chapter":"1",  
        "verse":"2",  
        "verse-count":"1",  
        "emulate":"true",  
        "person": "first-s",  
        "comment": "Translations are not in agreement as to whether this should be considered a prayer. Several translate the Greek 'euchomai' (Strong's 2172) to 'wish' or 'hope' instead of 'prayer.'"   
    }

## A Note About the Dividing Continuous Prayer  
To increase usability and profitability of the index, the author may choose to separate an unbroken prayer into smaller parts. This is typically done when there are distinct style shifts (category of prayer or from poetry to prose), person shifts ("I" to "we" or vice-versa), or translator's paragraph breaks. Breaks are obviously necessary in passaged like Psalm 119: aside from verses 1-3 and 115, the psalmist addresses God in prayer for the entire Psalm--172 verses worth! This Psalm is broken up in the prayer index by its section titles that correspond to the Hebrew acrostic poetry structure.  
When such divisions or translator headings do not clearly separate large passages of prayer, the author typically limits index entries to no more than 8 verses.

## About the Author

Ryan Cornett is a bi-vocational elder serving as Assistant Pastor of Manchester Baptist Church in Manchester, KY--a confessional Southern Baptist church that subscribes to the Philadelphia Confession of Faith.