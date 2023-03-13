# Prayer API Documentation

## *This API is in development as of March 2023. Contact the author for more information or to contribute information to the prayer index.*

## Definition of Prayer
Keach's Catechism (1677) and other reputable catechisms ask the question, "What is Prayer?" The answer from Keach: "Prayer is an offering up of our desires to God, for things agreeable to His will, in the name of Christ, with confession of our sins and thankful acknowledgment of His mercies" (1 John 5:14; 1 John 1:9; Phil. 4:6; Ps. 10:17; 145:19; John 14:13,14).  
For the purposes of this project, "prayer" is additionally defined as: ***A human being addressing God who is in the heavens.*** This supplementary understanding of prayer in the Bible is necessary to explain why conversations with God such as Genesis 3:9-13 and Genesis 4:9 & 13-14 are omitted from the index.

## The Purpose of the Prayer Index  
This index of ***every single prayer in the Bible*** and API are being produced in the hopes that developers will use it to create free or pay-what-you-will programs and applications saints use to foster deeper and more meaningful prayer lives. Whether for more actionable reminders or lists of prayer topics, this index and API can facilitate prayers that remain fresh and are grounded in God's Word.  
Please see Dr. Donald Whitney's book *Praying the Bible* to better understand why this index is so important and might help many saints and churches as they seek stronger prayer lives.

## Metadata  
    "updated":"2023-03-13T09:21:00.000Z",
    "categories":
	    ["confession", "exhortation", "imprecation", "intercession", "lament", "other", "praise", "repentance", "supplication", "thanksgiving"],
    "types":
	    ["command", "direct", "instruction", "reported"],
	"total-prayers":"1234567890"

## Object Keys & Values  
1. **Identification Number - "id"**  
Beginning with 101 in the Old Testament (OT) and 401 in the New Testament (NT), prayers are identified sequentially.
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
    - ***"other"***  
    Any prayer that does not fit neatly into another category.
    - ***"praise"***  
    Worshipping God with adoration for who He is and what He has done.
    - ***"supplication"***  
    Asking God for means, healing, rescue, fruit of the Spirit, aid, etc.
    - ***"thanksgiving"***  
    Showing gratitude to God for His bountiful blessings.
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
4. **Testament - "testament"**  
    - ***"old"*** or ***"new"***
5. **Title - "title"**
    - Typically ***"null"***; used if the prayer has a traditional (e.g., *The Lord's Prayer*) or translator-assigned title (e.g., *The Prayer of Agur*).
6. **Book - "book"**
    - The book containing the prayer. Book names are in the typical short, reference form (e.g., *Luke* instead of *The Gospel According to Luke* and *Acts* as opposed to *The Acts of the Apostles*); for the sake of easy reference, *Psalm* is used instead of the plural *Psalms* referring to the collection.
7. **Chapter - "chapter"**
    - The chapter containing the prayer.
8. **Verse(s) - "verse"**
    - The verse (e.g., *12*) or verses (e.g., *12-14*) containing the prayer.
9. **Verse Count - "verse-count"**
    - The total number of verses containing the prayer.
10. **Reference - "reference"**
    - The full scripture reference (e.g., *Matthew 6:9-13*)
11. **American Standard Version Text - "asv"**
    - The full text of the referenced prayer from this public domain translation.
12. **ASV length - "asv-length"**
    - The number of words contained in the prayer + any text that breaks up the prayer.
13. **King James Version text - "kjv"**
    - The full text of the referenced prayer from this public domain translation.
14. **KJV length - "kjv-length"**
    - The number of words contained in the prayer + any text that breaks up the prayer.
15. **Related - "related"**
    - An array of full references to related scriptures, typically NT quotes of OT texts and/or OT texts quoted/referenced in the NT.
16. **Context - "context"**
    - A complete sentence or sentences providing the context of the prayer when the API author deems it necessary.
17. **Break - "break"**
    - A boolean value that is ***"true"*** when the prayer is suspended by non-prayer text.
18. **Emulate? - "emulate"**
    - A boolean value that is ***"true"*** when the prayer is a good example set for saints to emulate.
19. **Person - "person"**  
    - ***"first-s"***: first-person singular (I, my, *individual*)
    - ***"first-p"***: first-person plural (we, our, *corporate*)
20. **Next Prayer - "next"**
    - The identification number (as a string) of the next prayer occurrence.
21. **Previous Prayer - "previous"**
    - The identification number (as a string) of the previous prayer occurrence.
22. **Comment(s) - "comment"**
    - Any extra information the author finds helpful.

## Example Response  
    {  
        "id": "632",  
        "category": ["intercession"],   
        "type": ["reported"],    
        "testament": "new",  
        "title": "null",  
        "book":" 3 John",  
        "chapter": "1",  
        "verse": "2",  
        "verse-count": "1",  
        "reference": "3 John 1:2",  
        "asv":"Beloved, I pray that in all things thou mayest prosper and be in health, even as thy soul prospereth.",  
        "asv-length":"19",  
        "kjv":"Beloved, I wish above all things that thou mayest prosper and be in health, even as thy soul prospereth.",  
        "kjv-length":"19",  
        "related": ["Matthew 9:12],  
        "context": "null",  
        "break":"false",  
        "emulate":"true",  
        "person": "first-s",  
        "next": "633",  
        "previous": "631",  
        "comment": "Translations are not in agreement as to whether this should be considered a prayer. Several translate the Greek 'euchomai' (Strong's 2172) to 'wish' or 'hope' instead of 'prayer.'"  
    }

## A Note About the Psalms  
By their very nature, the Psalms are typically prayers. To increase usability and profitability of the index, the author may choose to separate an unbroken prayer into smaller parts. A ready example is that of Psalm 119: aside from verses 1-3 and 115, the psalmist addresses God in prayer for the entire Psalm--172 verses worth! This Psalm is broken up in the prayer index by its section titles that correspond to the Hebrew acrostic poetry structure.  
When other such divisions and translator headings do not clearly separate large passages of prayer, the author typically limits index entries to no more than 8 verses.

## About the Author

Ryan Cornett is a bi-vocational elder serving as Assistant Pastor of Manchester Baptist Church in Manchester, KY--a confessional Southern Baptist church that subscribes to the Philadelphia Confession of Faith.