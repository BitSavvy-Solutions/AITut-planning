Course: https://code-blossom.notion.site/Applied-AI-fcae558fdac94fb7a60940564d9e799e

Content : https://drive.google.com/file/d/1x_0ofXScXBBb1PeNtDDDa9HoQ20_AdO2/view?ts=67ad7d11&pli=1




| Timestamp | Message |
|-----------|---------|
| 160 | cool so for a quick recap what we did last |
| 3200 | time was uh we learned about something called vector embeddings |
| 7759 | and uh vector embeddings are a way to store the |
| 11280 | semantic knowledge about some text or something so like for |
| 15360 | example uh if if we say if we have three items we |
| 20000 | have cat dog and man uh and then we search like in |
| 24480 | traditional databases we search for uh when we search for cat we'll get cat as |
| 30480 | a something that returns and we won't get |
| 33040 | any other matches and if we search for animal we won't get |
| 36399 | any match because uh the traditional database rdbms they cannot do a fuzzy |
| 41040 | match that which is an animal which is a which is not an animal something like |
| 46559 | that so when we use vector embeddings we store the |
| 50480 | uh rather than storing the text we store |
| 53520 | the uh information about what that |
| 57360 | sentence or what that term means so if we have cat dog and man and if you |
| 62960 | search for animal we'll get a |
| 66240 | percentage matching on each of the for each of the items for example for cat it |
| 70080 | will be like cut 80 percent it matches for dog it will be |
| 73920 | like 80 percent it matches and then for man it will be like maybe uh |
| 78479 | 70 meters maybe we can do a quick experiment on |
| 82000 | that but basically let me see |
| 86720 | um so uh so basically uh |
| 90080 | uh vector embeddings allow us to do fuzzy matching and it helps us uh |
| 94479 | uh when even when we don't have the exact term it can help us match and |
| 98479 | retrieve items and the fuzzy matching and vector embeddings are very helpful |
| 103680 | when it comes to uh rag frameworks where like for example |
| 107920 | i have petabytes of data or i have uh like high caroline |
| 112799 | we are just doing recap on uh vector embeddings and what they do |
| 118560 | so so for example we have uh like |
| 122640 | if we have small amount of data for example we were taking the example of my |
| 126840 | resume so my resume would have uh like maybe |
| 132239 | a thousand thousand words or something like that so i can put the thousand |
| 135440 | words in the context window and then ask ai something that okay what is my |
| 140319 | experience in back and what is my experience in front end but if the |
| 144160 | if the document store is too big like maybe a gigabyte of data is there then |
| 148720 | we cannot fit all of that into the context window |
| 152000 | so what we do is like we generate the vector embeddings for each of the |
| 157040 | we break the documents into smaller small chunks and then we |
| 161599 | generate a vector embeddings and then we can do a fuzzy match to get the top 10 |
| 166080 | matches or something and then just pull the relevant information into the |
| 169200 | context window and then generate the answer so like in this form vector |
| 173840 | embeddings is used quite often in uh in in document retrieval and |
| 180800 | in agentic workflows |
| 184400 | uh so if you if you look at the video the previous video you will we talked |
| 188480 | about spots where embeddings dents and buildings uh but uh like for ai's uh |
| 194080 | purpose we mostly use uh dense embeddings so |
| 198720 | here we have a demo |
| 209280 | within the experience let's see if it works |
| 223120 | uh so what i am doing here let me see if i can reduce the size |
| 228319 | i don't know why this is not working but what i'm doing here is like uh first of |
| 232000 | all i entered uh like i broke my experience |
| 236239 | like first dummy for sample purposes i broke my resume into small json files |
| 243680 | uh then for each of the json file i |
| 246959 | like for each of the item i generated uh |
| 252879 | i did call process resume which |
| 256479 | will go through each of the experience and then |
| 259280 | uh generate embedding for each of the experience so once we generate the |
| 263520 | embedding we get something like uh like a series of numbers |
| 268560 | which looks something like uh |
| 272560 | something like this so we can define the the more uh like uh |
| 280000 | the more dimensions we have the more information we have about the |
| 283759 | about the semantic knowledge about |
| 286639 | the more information we have about the meaning of what we are trying to store |
| 290320 | so for example the text is here here we are using 1536 dimensions so |
| 296400 | you'll see that one 1536 numbers are there ranging between uh |
| 301120 | minus one to one so this is how the embeddings look like |
| 305120 | so we have uh like for each of the text we have an embedding |
| 310000 | oops for each of the text we have embeddings |
| 315039 | and uh we are storing it currently in the local file but we can also store it |
| 318800 | in databases we have mongodb we have postgrade database which all |
| 323440 | allow for storing the vector embeddings and then what we are doing is uh like |
| 327840 | once we stored stored the information in the in that file we can we create a |
| 333600 | function called calculate similarity and then we can uh search |
| 338400 | based we can issue a query like a backend and then it will generate an |
| 343039 | embedding for that back end and then it will match the |
| 347120 | closeness so it's like vectors if you uh like if you have worked on vectors |
| 351919 | vectors are like uh from if on the three axis from zero zero zero to |
| 357440 | like whatever the vector position is it this this direction is called a vector |
| 362080 | so uh it uh like when we issue our query it creates a vector dimension a vector |
| 368400 | for that and then it compares which which are the closest items |
| 374080 | uh for the for the issue the query that i am issuing |
| 378400 | so for example i can issue the query here as |
| 381520 | backend and uh what it does is like it uh fetch |
| 387680 | it we get uh we get based on the uh matching like how close it is to |
| 393039 | other vectors it gives us a uh |
| 396000 | ordered list of the results like for back end uh all of |
| 400639 | my experience has some back end stuff i guess so |
| 403759 | it is the this one has the most this one has a |
| 407360 | back-end term probably so it has it is having 29.55 percent this is having back |
| 412960 | dash end so it is having a bit less uh this one is having uh |
| 418240 | javascript web services so it is having a bit less things like that so what if |
| 423039 | if i do something like vector database uh if i search for vector database |
| 429280 | database so i see that like because here there's |
| 434560 | vector database mentioned so it has a very high relevance and then this these |
| 438479 | are like quite low like 12 anything between 20 bit below 20 is like uh |
| 444000 | probably it's not it's not there uh let's also search for aws or let's |
| 450240 | search for google cloud right let's see what happens google cloud |
| 455199 | services so |
| 459680 | because it's mentioning cloud and backend and stuff so it's uh like i'm |
| 463360 | getting a good match for all of all of my |
| 466560 | uh my results |
| 468479 | um so so this is one of the examples of how |
| 473280 | the how vector embeddings can be used uh and |
| 477039 | in today's session what we'll do is like we will extend this and uh we'll try to |
| 482160 | uh see how to power uh |
| 485120 | rag frameworks using vector embeddings so uh what we'll do is like we'll uh |
| 489680 | ingest the now we are getting we are able to get |
| 493120 | the vector matching with the embedding matching so we will build a system that |
| 497680 | injects the resume and then uh creates all the experiences generates the |
| 502879 | embeddings for that and then based on the job opening |
| 507759 | it can pull up the top experiences and help us |
| 511440 | create a resume that is relevant for the working session |
| 517599 | so uh any like any doubts anyone so far like what |
| 521760 | we have we have gone through around vector and printing and stuff yes |
| 528000 | so when you saw us so you made us see these results that are |
| 533360 | relevant to the query that you entered why not one of them is like 100 since |
| 539440 | the word is present over there but the relevance is still 39 30 and not why not |
| 544640 | hundred percent so it will be 100 if the text matches |
| 548560 | exactly so if i do like uh for example if i like the whole text |
| 554880 | yeah if i copy the whole text let's see what happens |
| 559040 | if i copy the whole text 300 results right |
| 565920 | so if i if i change if i remove for example |
| 569920 | java spring just remove this then it will drop a bit it becomes 99.38 and |
| 576160 | then if i change this to uh |
| 578959 | um let's call it python |
| 583279 | work so like earlier it was 99.38 now it |
| 587120 | should become even lesser so now earlier it was 97 point something |
| 599519 | now it becomes 96.92 so |
| 602640 | like based on how how well uh how |
| 606800 | so it's called semantic search so how well it is matching semantically uh |
| 612000 | meaning wise it uh we get a uh we get a hit hit or not so if i change |
| 619200 | for something if i want to just get python experience i can do like python |
| 622959 | and then wherever python is mentioned will come |
| 625600 | on the top so we have python here uh |
| 631040 | here we don't have python but maybe because uh vector database is |
| 635680 | related to python it's uh it's getting that and also you'll see that like to |
| 640399 | generate the embeddings we are using uh open ai uh so here this is a generate |
| 646079 | embedding generation so we are using open ai's text embedding |
| 650880 | three small so this this model is open ai model so |
| 655279 | we can generate embeddings using multiple models so there are some models |
| 659519 | that are local which have a small knowledge so it's not able to for |
| 662959 | example understand uh that like maybe it doesn't have knowledge about aws so if i |
| 668000 | say something like lambda if i uh so here |
| 672160 | we have do i have lambda is here |
| 676720 | so let's say something like api gateway so api gateway is related is an aws |
| 683360 | product but the a local model may not know that so when it generates when we |
| 688240 | are using the local model to generate the embedding we will not get a good |
| 692000 | match if we are using uh if we are querying first |
| 695360 | for api gateway api |
| 706160 | uh yeah we won't we won't get a good match if you are using a local matching |
| 710000 | but because we are using the llm to generate the embedding and llm has |
| 713600 | knowledge about all the aws and everything everything in the world uh so |
| 718000 | so the so it's able to understand that when we i'm using uh |
| 722320 | uh some term like api gateway it's related to it aws and whatever is |
| 728160 | having my experience around aws it's matching |
| 731040 | uh it's returning a good match for that so all of these have aw so that's why it |
| 737200 | returned a good match for that uh |
| 741920 | any any other questions uh if not then let's |
| 750800 | uh let's proceed and uh what i'll do is |
| 759519 | copyright path we have these |
| 794079 | files so what i want first is to so |
| 798959 | when uh like when we generate the embeddings the string size like we we |
| 804399 | have a limit on how many tokens can we input into it like for example uh when |
| 809600 | we are using the lms we have a limit of the context window which is like 128 000 |
| 814320 | or something but when we are using the these these tokens then uh |
| 819519 | the size is much smaller there was some place where there is a |
| 840000 | little more information about how many tokens |
| 843920 | are allowed so the pricing is quite affordable for |
| 856880 | generating the tokens uh one two one zero two for a million |
| 860959 | token and |
| 875839 | you will find the maximum number of buttons |
| 881040 | in the search hello my name is |
| 899839 | so it can only take eight thousand tokens which is around two thousand four |
| 903680 | thousand words and uh because the tokens uh the size the dimension size is always |
| 909040 | the same so whatever we input the number of outputs will |
| 912639 | always be one five three six numbers uh so so the more information we put in the |
| 919120 | uh more diluted it gets so if there's some if we for example just put cat it |
| 924560 | will get 1536 uh tokens and if you create a long statement about a cat then |
| 930160 | that will also get uh 1536 tokens so it's always uh |
| 934720 | like it's it's it's a |
| 938240 | what do we call it um trade-off we have to see how long we |
| 942880 | want the uh the document to be like if you make |
| 946000 | it too long then some of the finer details will be missed out if you make |
| 949759 | it too small then it's a wastage of space uh so generally what we do is like |
| 955120 | around we try to do around two thousand or three thousand tokens which is around |
| 958639 | thousand words uh something like that so in the document a pdf document for |
| 964160 | example will be like uh thousands tens of thousands of words so |
| 969360 | we need to break the document into smaller parts before being able to |
| 973199 | generate the embeddings for that so this process is called chunking |
| 977519 | so what we will do is uh first do chunking |
| 982160 | let me see i'll just pull my resume out again |
| 991759 | because i'm trying to apply for jobs and it's so difficult to |
| 996399 | modify for every every use case |
| 1000560 | so i like i thought that i'll just use use this for that as well |
| 1011279 | i want someone profiled so i'll copy this |
| 1032079 | and then we'll first do a chunking |
| 1046959 | so how this this is formatted is like uh |
| 1053120 | when we are when when we want to do the chunking we |
| 1056960 | want to like for example this may be each experience can be uh |
| 1062240 | like one chunk but what we also want is to |
| 1066240 | ensure that the company name and the the position is also part of each of the |
| 1071200 | experience if there are skills then these technologies this this is also |
| 1074799 | part of each of the experience so that when we are doing a vector search |
| 1078480 | the search is matching like for example if i search for amazon uh so like |
| 1083520 | because this experience in itself doesn't have the |
| 1086640 | uh information about amazon this will not come up as as well so when we are |
| 1092000 | doing the chunking we don't just want to add the |
| 1095600 | text we also want to add some more metadata to it to make it more uh |
| 1100160 | uh like to make this |
| 1103840 | search being more relevant basically |
| 1108640 | so uh let's try uh |
| 1112640 | try this um |
| 1115039 | i want to chunk this document |
| 1119919 | for vector |
| 1122640 | and buildings generation |
| 1129039 | i think what it would be good to create a csv create |
| 1133919 | a csv with |
| 1139600 | each experience |
| 1143200 | in our company gain its own |
| 1148840 | junk and the metadata |
| 1153280 | having the company name |
| 1157280 | the position the |
| 1162320 | period of work and |
| 1165600 | uh and |
| 1170320 | the skills and also i should ask it not to help |
| 1175600 | this network see me |
| 1180240 | if any questions i like |
| 1189120 | exactly this is gpt follower |
| 1203840 | so this is the problem with the if you if you are applying to jobs what |
| 1208000 | happens is like for each of the job opening they want |
| 1211760 | a resume tailored for that job they don't want if they are looking for |
| 1215840 | back-end they don't want to see any front-end experience |
| 1219039 | um so |
| 1222880 | pretty i think gt4o has much longer context window so that's why it's it's |
| 1238400 | what is it doing content company position period the |
| 1244240 | discuss again so it uh it |
| 1263520 | it didn't break the each of the experience into different lines so we'll |
| 1266960 | need to reprompt it |
| 1273840 | want it ps3 or psv |
| 1278480 | pipe so this is |
| 1280880 | this is called pipe and it's one of the cleaner ways to |
| 1284720 | separate because |
| 1286720 | csv like commas are commonly used so sometimes it gets confusing |
| 1291919 | pipes separated and i want each experience |
| 1299840 | in our company as its own |
| 1307520 | let's also give it an example oh |
| 1333679 | i want this and then i don't want all of this in the |
| 1345120 | and then this |
| 1382400 | again it did the same thing is it |
| 1401840 | um keeps doing the |
| 1405280 | same thing but it's okay let's not waste too much time on this |
| 1410480 | what we can do okay |
| 1424400 | i want to create all the individuals experiences individually so that we can |
| 1429840 | see the magic of vector embedding so otherwise if it's just five six |
| 1433039 | experiences we won't be able to see much so i'll |
| 1439679 | make it change it a bit so |
| 1444960 | let me get it let's |
| 1448720 | uh so i think um |
| 1469039 | this then later on we can |
| 1477039 | fix our |
| 1480640 | projects so now what we can do is |
| 1552640 | it's a bit of manual work i'm thinking if i should |
| 1556720 | just use ai to create a python script but |
| 1562320 | quickly operates it |
| 1583279 | why okay |
| 1618400 | welcome it's |
| 1655120 | okay hope this works |
| 1661360 | um uh |
| 1669120 | in this technique number seven |
| 1694840 | yeah yeah so fine now |
| 1701840 | so i'll put all of my experience in here |
| 1711840 | um good now we have a lot of text which |
| 1733200 | will be helpful to test it out |
| 1763600 | okay so now we have the initial psv now what |
| 1771520 | we want is to ingest this into uh |
| 1780240 | uh into in like generate basically generate the vector embeddings for this |
| 1785039 | uh so this is this is the code for uh |
| 1793919 | what we generated last time so we'll use this as a |
| 1796880 | sample or as an input |
| 1803200 | i have a file uh |
| 1808640 | or maybe ask for input uh ask for an input |
| 1814960 | of for |
| 1818399 | experiences and |
| 1821840 | output output of file |
| 1826159 | uh with |
| 1829200 | um with uh |
| 1833279 | vector embeddings |
| 1836799 | generated for each of the experience |
| 1849120 | separated by circulated by |
| 1852640 | new line let's see |
| 1890960 | um this is what file is it asking for a file |
| 1929840 | oh it's already expecting some file here so i'll |
| 1935360 | provide that and also see why this error is |
| 1958320 | um um copy relative path |
| 1970880 | and buildings generator then it looks like where is it |
| 1981120 | collecting the experiences from office |
| 2000000 | i use the experiences in the file |
| 2011360 | copy without this |
| 2016240 | it looks like it's some example of how the file looks like |
| 2023360 | so that it can it's only getting the |
| 2070000 | experience for column two but let's run this and then see what |
| 2080560 | we can modify it buildings |
| 2097200 | let's see waiting for zero experiences |
| 2125920 | this is saved is it reading the files correctly now we |
| 2145599 | have 15 or something left so the file is being read correctly |
| 2161119 | listed um |
| 2172960 | so it's reading this correctly um i don't want like let's just directly |
| 2179440 | generate the embedding and then is equal to |
| 2183520 | cells dot get building |
| 2188400 | online let's get them waiting for the full line and then print that |
| 2195520 | then and also let's change the |
| 2208079 | model from what it is using to the latest one |
| 2215040 | ada is a bit old we are embedding the response |
| 2241520 | this one very experienced |
| 2259200 | we have a big experience here and we have |
| 2263119 | embedding generator here response dot |
| 2276800 | ready okay now we are getting them buildings |
| 2288160 | correctly now |
| 2294240 | what we need to do once we get the embedding we need to |
| 2300960 | save it experiences start opened |
| 2334160 | so now we'll get the columns and then we should be able to put |
| 2343200 | that one yeah this should work let's see |
| 2351200 | so once we get the return experiences um |
| 2371760 | okay so now we should have 17 experiences in this file |
| 2376800 | so we have company period description under experience code |
| 2382880 | so now now that we have this file we should be able to use this file to do a |
| 2387920 | query so query experience |
| 2398079 | let's just run it most likely it will give us some error but |
| 2402400 | um so like the structure that was earlier |
| 2434240 | is different than this so we need to modify this a bit |
| 2439359 | and i have done this i'll take an example here |
| 2450880 | to show us how the structure looks like this is not |
| 2468000 | passing the file directly |
| 2473200 | the file looks like let's remove all these numbers |
| 2513920 | okay uh |
| 2555280 | let's see if it works where is it |
| 2573200 | minus this um |
| 2594960 | it's not storing the experience is it |
| 2603359 | description is this okay it's not starting the experience |
| 2607440 | uh so it's storing the tags the skills but it's not storing the experience we |
| 2611440 | need to see the experience as well um |
| 2616960 | hope to get to the rag stuff in this session |
| 2629520 | lips yes |
| 2649760 | description column 2 and |
| 2653599 | project launcher |
| 2664720 | column this i'll call it skills |
| 2702839 | um and then we'll have to update the query experience as well |
| 2725040 | exclusion project um |
| 2779200 | finished don't take that much time |
| 2828480 | let's give a reply but what is this |
| 2840400 | that similarity once minus one minus distance cosine |
| 2846000 | querying one experience in wedding let's try something else |
| 2857280 | uh let's try maybe aws okay now it's working better |
| 2874160 | so for example if i do back-end aws |
| 2880640 | mode uh |
| 2889599 | it's not very clear project let's just uh display the |
| 2897599 | let's remove the period and this display the project |
| 2903839 | um i have four minutes okay let's see more of this |
| 2921359 | and like we have something called like a top k so we can define how many |
| 2925839 | experiences how many matches we want so here we currently have four we can |
| 2930160 | change it to let's say 10 |
| 2933839 | 10 is a good experience to show so for example if i |
| 2938800 | query experience and say something like mentorship i should get code lost some |
| 2943359 | work there uh so cold blossom uh weekly mentorship |
| 2952640 | and amazon music mentorship mentored interns uh applied curriculum powering |
| 2958400 | uh so again code blossom so it's working and we see that on the |
| 2963599 | top we see like for uh |
| 2968240 | for the code blossom work it's having high percentages and like everything |
| 2973119 | else where there's no mentorship involved it's low low percentages so if |
| 2977839 | i say something like audio uh |
| 2981200 | audio technology |
| 2985599 | so i'll get music stuff on top so there's audio comparison then there |
| 2991200 | is vision audio ai applications using api in code blossom then we have amazon |
| 2997280 | music amazon music hackathon so so this way like we are able to get like |
| 3003680 | whatever turn we are looking for we will get |
| 3006960 | we can get top matches based on that so for example in |
| 3011119 | i have a lot of experience in amazon music so all of it is above 20 26. so |
| 3016559 | now we are able to fetch the information now i have two minutes to convert it |
| 3020319 | into a proper resume see if i can |
| 3027359 | if okay i can help me do that uh so |
| 3032240 | i want to uh |
| 3035520 | so once once |
| 3038839 | experiences are qualified |
| 3043520 | i want to generate a resume |
| 3048480 | using gpt |
| 3052160 | 400 using |
| 3058240 | using the quality file or let's instead of resume let's call it |
| 3065760 | cover letter format qualified |
| 3082559 | let's see so what i'll do here is i'll create |
| 3093680 | another file file |
| 3099599 | create cover |
| 3102559 | letter dot even we are on time so i'll just run this |
| 3118640 | it works it works if it doesn't i'll i have to do it i have to start |
| 3128079 | applying for jobs so i'll do it anyways and i'll share the code file with you |
| 3135040 | uh so let's see uh |
| 3139119 | generate please like |
| 3148079 | create uh so let's call it |
| 3156000 | music technology so it fetched the relevant experiences |
| 3164319 | and let's say yes software development |
| 3174079 | completions now |
| 3180480 | okay i know what's the issue |
| 3196880 | okay uh we are past time but if you need to drop off drop you can drop off |
| 3202800 | uh i'll just continue working on this |
| 3216960 | see and get cover letters change that |
| 3249440 | thanks for joining back alice i'm |
| 3252880 | we are almost there but still with the moment of truth let's |
| 3256800 | see uh |
| 3260000 | let's call it cloud okay |
| 3274240 | and then say yes so |
| 3278400 | yeah what |
| 3283760 | 100 what is this resume search bot has no attribute |
| 3293359 | oh i baron indentation guarantetion |
| 3299920 | right yeah |
| 3304079 | all of this is another time thanks for staying for long |
| 3310640 | i'll see you around let's see |
| 3318559 | after this i'm letting you guys know okay nevermind |
| 3324960 | uh will this work |
| 3334480 | music number three |
| 3338880 | and this okay never is |
| 3348480 | i'll fix it and i'll push in the code later |
| 3351440 | uh i think there is some minor issue chat |
| 3355119 | has no object created so i will continue fixing |
| 3359359 | this and i'll share it with you guys later |
| 3364240 | uh thanks anna thanks caroline thanks anna i'll |
| 3368480 | will continue on next monday and you have a |
| 3372640 | great rest of your week thank you so much |
| 3390400 | you |</div>
