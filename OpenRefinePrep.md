# Capstone Exercise Fail Log

## Transcription and TEI

Changed the two title tags – watched [youtube video](https://www.youtube.com/watch?v=BujLy71JY1k), realized different ways of writing your xsl will produce different formatting results so I should apply the code from the exercise b/c I want the same result

Took out the tags about publication altogether bc don’t have that info

Put my own name in the transcribed by field

Put “1-80” where I had previously put the page number I was transcribing – biblScope

Marked all headings and paragraphs with ```<p>``` and ```</p>``` tags, then I pasted the entire thing in between the body tags

Then went into xsl and opened in TextEdit, took out, under ```<ul>``` the tags that had to do with individuals and claims, and under ```<xsl:template>``` took out the information about people and claims, leaving everything about place names
    
I wondered if I should distinguish between physical places and entities (like if someone was recruited from a battalion) but decided not to because I’m trying to show the interconnectedness throughout the war – I googled battalions and whatever else to determine what place I could peg them too

When looking up in GeoHack, I learned from the TEI exercise to add a minus sign in front of the W coordinate for it to give me north America – idk why this works but I remembered to do it this time

Two people were struck of the strength to the H.M.A.T Araguaya – this is a boat, so I left it out, can’t pin it to a location

Finished tagging all the places and it doesn’t work
	Could be a problem with xsl since I don’t know how to do that but I’m first going to make sure it’s not a problem with my tags
	Replaced all & with &amp; - didn’t help
	Found 2 “placeNames” and fixed it
	Found a missing quotation mark in buxton
	Found a </placeName without the >

Tried again and got error message saying instead of ```</p>``` it expected to see ```</unreadable>``` - realized in spots where I couldn’t make out words I had written ```<unreadable>``` - forgot this was tag format. Took them out and replaced with [unreadable]

Now getting error that instead of ```</body>``` ```</p>``` is expected. No clue why --> used find to see how many ```<p>``` and ```</p>``` I have and have 118 ```<p>``` and 115 ```</p>``` --> went through with find and check all ```<p>``` and found the problems and fixed

Learned it would have been better to do maybe 20 tags at a time, check to see if this works, and continue, since it’s easier to find a problem if there’s only 20 tags as opposed to 831

I didn’t realize that enter-separated sentences would stay connected when transferred to Firefox since there’s no <p> and </p> around each of them. By the time I got it working it was necessary that I just accept this and continue with the assignment, because it would take way too long to go through adding those tags everywhere, plus I already had problems with them – but I know now that if I need things to stay separate that’s how it has to be done

## CSV Chart

Leaving “taken on the strength” so I can replace in DHBox with nothing and same with “on transfer” take “proceeded” out too
Leaving “from” to replace with comma as well
Months will need to be replaced by numbers – august with 8, September 9, October 10

### Commands in DHBox - cleaning with Regex
   
    1  sudo apt-get install nano
    2  nano War-Diaries-OpenRefine.txt
    3  sed -r -i.bak s/(\b to \b)/,/g' War-Diaries-OpenRefine.txt
    4  nano War-Diaries-OpenRefine.txt
    5  sed -r -i.bak 's/(\b to \b)/,/g' War-Diaries-OpenRefine.txt
    6  nano War-Diaries-OpenRefine.txt
    7  sed -r -i.bak 's/proceeding//g' War-Diaries-OpenRefine.txt
    8  nano War-Diaries-OpenRefine.txt
    9  sed -r -i.bak 's/proceeded//g' War-Diaries-OpenRefine.txt
   10  nano War-Diaries-OpenRefine.txt
   
   11  sed -r -i.bak 's/taken on the strength//g' War-Diaries-OpenRefine.txt
   
   12  nano War-Diaries-OpenRefine.txt
   
   13  sed -r -i.bak 's/on transfer//g' War-Diaries-OpenRefine.txt
   
   14  nano War-Diaries-OpenRefine.txt
   
   15  sed -r -i.bak 's/taken on strength//g' War-Diaries-OpenRefine.txt
   
   16  nano War-Diaries-OpenRefine.txt
   
   17  sed -r -i.bak 's/struck off the strength//g' War-Diaries-OpenRefine.txt
   
   18  nano War-Diaries-OpenRefine.txt
   
   19  sed -r -i.bak 's/struck off strength//g' War-Diaries-OpenRefine.txt
   
   20  nano War-Diaries-OpenRefine.txt
   
   21  sed -r -i.bak 's(\b from \b)/,/g' War-Diaries-OpenRefine.txt
   
   22  sed -r -i.bak 's/(\b from \b)/,/g' War-Diaries-OpenRefine.txt
   
   23  nano War-Diaries-OpenRefine.txt
   
   24  sed -r -i.bak 's/taken on the Strength//g' War-Diaries-OpenRefine.txt
   
   25  nano War-Diaries-OpenRefine.txt
   
   26  sed -r -i.bak 's/(\b to \b)/,/g' War-Diaries-OpenRefine
   
   27  sed -r -i.bak 's/(\b to \b)/,/g' War-Diaries-OpenRefine.txt
   
   28  nano War-Diaries-OpenRefine.txt
   
   29  sed -r -i.bak 's/(\b  to \b)/,/g' War-Diaries-OpenRefine.txt
   
   30  nano War-Diaries-OpenRefine.txt
   
   31  sed -r -i.bak 's/August/8/g' War-Diaries-OpenRefine.txt
   
   32  nano War-Diaries-OpenRefine.txt
   
   33  sed -r -i.bak 's/September/9/g' War-Diaries-OpenRefine.txt
   
   34  nano War-Diaries-OpenRefine.txt
   
   35  sed -r -i.bak 's/October/10/g' War-Diaries-OpenRefine.txt
   
   36  nano War-Diaries-OpenRefine.txt
   
   37  sed -r -i.bak 's/(\b  from \b)/,/g' War-Diaries-OpenRefine.txt
   
   38  nano War-Diaries-OpenRefine.txt
   
   39  clear
   
   40  history
   
   41  history > OpenRefinePrep.md
   
   Remember: check to see if there’s more than 4 commas in a line
   
   If it wasn’t clear where they were taken on the strength to, I added this while I still knew where each part happened
   
Got through every line, cleared out a very large amount of stuff, logged into DHBox and saw -1 weeks and 6 days left so I asked what that meant in slack and was told to make a new DHBox and download all my files from my old one.

Did so, uploaded my text file as well, installed Nano, tried to open my text file and nothing is in it
	I think it might be because I didn’t upload the file into my “davidovic” folder and I’m in the davidovic directory
	Have moved it, will see if this fixes it
		This fixed it

sed -r -i.bak ‘s/(\b to \b)/,/g’ War-Diaries-OpenRefine.txt
-	Missed first ‘ when doing this command, redid it and was successful
-	Did same with from, missed s/ slash there

Forgot .txt in a command
Replacing to with commas second time around didn’t work? Not sure why
sed -r -i.bak ‘s/(\b to \b)/8/g’ War-Diaries-OpenRefine.txt
	wrote that didn’t work
sed -r -i.bak ‘s/(\b  to \b)/8/g’ War-Diaries-OpenRefine.txt
	added extra space before to b/c that’s how they were in the doc and it did work

Sometimes more than one person was listed as going somewhere in the same entry, but I couldn’t have more than 4 commas so I indicated they were together with plus signs

When I fixed all the comma issues, I realized there were a lot of things I had thought I had fully removed with regex that were still in there, like a lot left b/c upper case or extra space or something and didn’t recognize
	Like taken on the strength
	So I used regexr to locate every keyword I didn’t want that I could think of and fixed them
	Also many tos and froms that had not been changed to commas, fixed those

Looking at place name clusters in OpenRefine in the To category and I see I missed some “from”s – realized I can look at those clusters more closely so I did, to see if I can just edit them
	Was able to and fixed them
	Edited a few

When I was getting no more (useful) clusters I exported my document as a CSV and opened it on my computer to quickly glance through it again
	Found some areas where still more froms and tos had been missed, fixed those, easier to tell when it’s in a table
