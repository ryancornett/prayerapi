# Prayer API Documentation

## *This API is in development as of March 2023. Contact the author for more information.*

## Definition of Prayer
Keach's Catechism (1677) and other reputable catechisms ask the question, "What is Prayer?" The answer from Keach: "Prayer is an offering up of our desires to God, for things agreeable to His will, in the name of Christ, with confession of our sins and thankful acknowledgment of His mercies" (1 John 5:14; 1 John 1:9; Phil. 4:6; Ps. 10:17; 145:19; John 14:13,14). For the purposes of this project, "prayer" is additionally defined as: ***A human being addressing God who is in the heavens.*** This supplementary understanding of prayer in the Bible is necessary to explain why conversations with God such as Genesis 3:9-13 and Genesis 4:9 & 13-14 are omitted from the index.

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
2. **First Category - "category-1"**  
    - ***"confession"***
    - ***"exhortation"***
    - ***"imprecation"***
    - ***"intercession"***
    - ***"lament"***
    - ***"other"***
    - ***"praise"***
    - ***"repentance"***
    - ***"supplication"***
    - ***"thanksgiving"***
3. **Second Category - "category-2"**  
*If necessary*
4. **Third category - "category-3"**  
*If necessary*
5. **First Type - "type-1"**  
    - ***"command"***  
    An imperative to pray in a certain manner or for certain things.
    - ***"direct"***  
    The exact, quoted words of a prayer.
    - ***"instruction"***  
    An exhortation to pray in a certain manner or for certain things.
    - ***"reported"***  
    An indirect reference to a prayer or habit of praying.
6. **Second Type - "type-2"**  
*If necessary*
7. **Testament - "testament"**  
    - ***"old"*** or ***"new"***
8. **Title - "title"**
    - Typically ***"null"***; used if the prayer has a traditional (e.g., *The Lord's Prayer*) or translator-assigned title (e.g., *The Prayer of Agur*).
9. **Book - "book"**
    - The book containing the prayer. Book names are in the typical short, reference form (e.g., *Luke* instead of *The Gospel According to Luke* and *Acts* as opposed to *The Acts of the Apostles*); for the sake of easy reference, *Psalm* is used instead of the plural *Psalms* referring to the collection.
10. **Chapter - "chapter"**
    - The chapter containing the prayer.
11. **Verse(s) - "verse"**
    - The verse (e.g., *12*) or verses (e.g., *12-14*) containing the prayer.
12. **Verse Count - "verse-count"**
    - The total number of verses containing the prayer.
13. **Reference - "reference"**
    - The full scripture reference (e.g., *Matthew 6:9-13*)
14. **American Standard Version Text - "asv"**
    - The full text of the referenced prayer from this public domain translation.
15. **ASV length - "asv-length"**
    - The number of words contained in the prayer + any text that breaks up the prayer.
16. **King James Version text - "kjv"**
    - The full text of the referenced prayer from this public domain translation.
17. **KJV length - "kjv-length"**
    - The number of words contained in the prayer + any text that breaks up the prayer.
18. **Related - "related"**
    - An array of full references to related scriptures, typically NT quotes of OT texts and OT texts quoted/referenced in the NT.
19. **Context - "context"**
    - A complete sentence providing the context of the prayer when the API author deems it necessary.
20. **Break - "break"**
    - A boolean value that is ***"true"*** when the prayer is suspended by non-prayer text.
21. **Emulate? - "emulate"**
    - A boolean value that is ***"true"*** when the prayer is a good example set for saints to emulate.
22. **Person - "person"**  
    - ***"first-s"***: first-person singular (I, my, *individual*)
    - ***"first-p"***: first-person plural (we, our, *corporate*)
23. **Next Prayer - "next"**
    - The identification number (as a string) of the next prayer occurrence.
24. **Previous Prayer - "previous"**
    - The identification number (as a string) of the previous prayer occurrence.
25. **Comment(s) - "comment"**
    - Any extra information the author finds helpful.

## Example Response  
    {  
        "id":"632",  
        "category-1":"intercession",  
        "category-2":"null",  
        "category-3":"null",  
        "type-1":"reported",  
        "type-2":"null",  
        "testament":"new",  
        "title":"null",  
        "book":"3 John",  
        "chapter":"1",  
        "verse":"2",  
        "verse-count":"1",  
        "reference":"3 John 1:2",  
        "asv":"Beloved, I pray that in all things thou mayest prosper and be in health, even as thy soul prospereth.",  
        "asv-length":"19",  
        "kjv":"Beloved, I wish above all things that thou mayest prosper and be in health, even as thy soul prospereth.",  
        "kjv-length":"19",  
        "related": "null",  
        "context": "null",  
        "break":"false",  
        "emulate":"true",  
        "person": "first-s",  
        "next": "633",  
        "previous": "631",  
        "comment": "null"  
    }

## About the Author

Ryan Cornett is a bi-vocational elder serving as Assistant Pastor of Manchester Baptist Church in Manchester, KY--a confessional Southern Baptist church that subscribes to the Philadelphia Confession of Faith.