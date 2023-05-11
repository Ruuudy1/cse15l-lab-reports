<h1>Grep Commands!<h1>
<h2> (found grep commands information on https://www.geeksforgeeks.org/grep-command-in-unixlinux/)<h2>

<h3> The grep command is one of the most useful commands in bash. What the grep command does is find 
all the times the character of your choice is found in a .txt file. For example, in the ./technical directory used during last week's skill demo, 
we can use the following command on any file within it: <h3>

<h4>Example:
          
          $ grep "definition" biomed/1468-6708-3-1.txt
          
          drawback of this simple definition of 'healthy' is that
          report results using only the simpler definition.
          
<h3>as we can see, this outputed the 2 lines that contain the characters "definition" which in this case it is seen in 2 times in this .txt file.
but there is other functionalities to the grep command.<h3>

<h2>-c command<h2>

<h3>For example if we arent interested on the whole line were the characters are included but rather just to count how many times the word appears we can add "-c"
right after grep.

When using this on the previous example we get:

<h4>     
Example 1 (1/2):
          
          $ grep -c "definition" biomed/1468-6708-3-1.txt
          
          2 
<h4>
          
this is as we expected since we saw previously that "definition" was only in this specific file twice which is why in this case we got the number 2. 
This command will come in handy when we have a very long output and rather of us counting the iines ourselves we only get the number of lines.<h3>

<h4>Example 1 (2/2):
Another useful way of using grep is by pairing it with the * in the filename/filetype to output exactly how mnay times that string appears in each file inside that folder:

without "-c":
          
          $ grep "risks" government/Alcohol_Problems/*.txt
          
          government/Alcohol_Problems/Session3-PDF.txt:range from minimal to very sizeable reduction in risks that have
          government/Alcohol_Problems/Session3-PDF.txt:settings to reduce drinking and alcohol related risks. The first
          government/Alcohol_Problems/Session3-PDF.txt:multiple health risks (e.g., smoking, alcohol use, seat belt use),
          

with "-c":
          
          $ grep -c "risks" government/Alcohol_Problems/*.txt
          
          government/Alcohol_Problems/DraftRecom-PDF.txt:0
          government/Alcohol_Problems/Session2-PDF.txt:0
          government/Alcohol_Problems/Session3-PDF.txt:3
          government/Alcohol_Problems/Session4-PDF.txt:0 
          
<h4>
          
          
<h2>-h command<h2>

<h3>at first I did not think this command did much as when I tried:<h3

          <h4>$ grep -h "definition" biomed/1468-6708-3-1.txt
          
          drawback of this simple definition of 'healthy' is that
          report results using only the simpler definition.

          $ grep "definition" biomed/1468-6708-3-1.txt
          
          drawback of this simple definition of 'healthy' is that
          report results using only the simpler definition.

<h4>
          
<h3> both commands seemed to produce the same output. Yet this command is really usefull paired with the "*" in the filename or filetype, 
As now we can look through ALL the files type .txt in biomed or any other folder without getting the file it is from in our output. <h3>


Example 2 (1/2):
(for the sake of fitting the whole output in one page I will use a different folder within ./terminal) 
         
<h4> without "-h" command:
          
          $ grep "definition" government/About_LSC/*.txt
          
          government/About_LSC/commission_report.txt:Furthermore, H-2A workers by definition are physically present in
          government/About_LSC/commission_report.txt:Furthermore, H-2A workers by definition are physically present in
          government/About_LSC/commission_report.txt:definition are required to leave the United States within a year,
          government/About_LSC/diversity_priorities.txt:and new definitions of diversity and leadership will be crafted. We
          government/About_LSC/diversity_priorities.txt:boards of Directors, new definitions of leadership --will be
          government/About_LSC/diversity_priorities.txt:Lack of a common definition/vision of
          government/About_LSC/diversity_priorities.txt:definition and vision of diversity and earmarking resources so that
          government/About_LSC/diversity_priorities.txt:Conferees found that programs lacked a common definition and
          government/About_LSC/diversity_priorities.txt:based on an expanded definition of advocacy, moving beyond
          government/About_LSC/diversity_priorities.txt:A common definition of diversity is developed. It is informed by
          government/About_LSC/LegalServCorp_v_VelazquezOpinion.txt:definition of its program in every case, lest the First Amendment
          government/About_LSC/reporting_system.txt:! Clarification of definitions. For example, "web hits" were
          government/About_LSC/Special_report_to_congress.txt:definition of a "case." However clear and meaningful the definition
          government/About_LSC/Special_report_to_congress.txt:definition had not kept pace with the changes in the service
          government/About_LSC/Special_report_to_congress.txt:not meet the definition of a "closed case," as previously detailed.
          government/About_LSC/Special_report_to_congress.txt:simple cost-per-case analysis, without further definition, would
          government/About_LSC/Special_report_to_congress.txt:very important activities that do not fall within the definition of
          government/About_LSC/Special_report_to_congress.txt:definition of a case.
          
<h4>

<h4> with "-h" command:
          
          $ grep -h "definition" government/About_LSC/*.txt
          
          Furthermore, H-2A workers by definition are physically present in
          Furthermore, H-2A workers by definition are physically present in
          definition are required to leave the United States within a year,
          and new definitions of diversity and leadership will be crafted. We
          boards of Directors, new definitions of leadership --will be
          Lack of a common definition/vision of
          definition and vision of diversity and earmarking resources so that
          Conferees found that programs lacked a common definition and
          based on an expanded definition of advocacy, moving beyond
          A common definition of diversity is developed. It is informed by
          definition of its program in every case, lest the First Amendment
          ! Clarification of definitions. For example, "web hits" were
          definition of a "case." However clear and meaningful the definition
          definition had not kept pace with the changes in the service
          not meet the definition of a "closed case," as previously detailed.
          simple cost-per-case analysis, without further definition, would
          very important activities that do not fall within the definition of
          definition of a case. 
          
<h4>


<h3> This is very useful when we want to quickly find/copy-paste over a line(s) a character is found at without having to take the time
to erase the path of every single one at a time. It also makes it slighty easier to read. <h3>
          
Example 2 (2/2):
          
without "-h" command:   
          
          $ grep "phosphocellulos" biomed/*.txt
          
          biomed/1471-2091-3-18.txt:          enzyme was purified using the phosphocellulose and
          biomed/bcr631.txt:          addition of a final phosphocellulose chromatography step
          biomed/bcr631.txt:        saline; PC-tubulin = MAP-free phosphocellulose-purified
          
with "-h" command:    
          
          $ grep -h "phosphocellulos" biomed/*.txt

          enzyme was purified using the phosphocellulose and
          addition of a final phosphocellulose chromatography step
          saline; PC-tubulin = MAP-free phosphocellulose-purified
          
<h3>
          
<h2>-i command<h2>
          
<h3>Another useful command to truly get all outputs of a string of characters is "-i". This command does not take Capitalization (lowercase/undercase) into consideration 
when searching for a string. This is really usefull to truly find all words that match that character as many times some words inside the .txt file could be Capitalized (Hello) 
or in all Caps (HELLO) and normal grep will not find there if you only give write grep "hello" ... <h3>
          
<h4>Example 3 (1/2):
          
without "-i":  
          
          $ grep "america" biomed/1472-6882-1-10.txt
          
          Mazama americana trinitatis ), lappe
          Solanum americanum leaf decoction
          Solanum americanum leaf extracts
          
with "-i": 
          
          $ grep -i "america" biomed/1472-6882-1-10.txt
          
          Mazama americana trinitatis ), lappe
          use are very similar to those of the South American
          related to those previously practiced in South America.
          native South American groups.
          There are indications that South American Amerindians
          America also believed that deer had an inoffensive body
          is of the closely related South American and Caribbean
          Studies in South America detail the pain and oedema at
          America and the Caribbean). All folk-medicinal uses are
          Indies, Venezuela, South and Central America against
          American rattlesnake (
          America and the Caribbean [ 52 86 ] . Poultices are used
          Throughout tropical Central and South America, leaves
          In South America leaves are used for inflammatory
          general cure-all in Latin America and the Caribbean [ 16
          noted in the meticulous data compiled on Middle America [
          Solanum americanum leaf decoction
          Solanum americanum leaf extracts

<h4>
          
<h3> As we can see far more outputs appeared since in a lo of cases throughout this file "america" is capitalized. <h3>  
          
<h4>Example 3 (2/2):
          
without "-i": 
          
          $ grep "xiphidium" biomed/1472-6882-1-10.txt

with "-i": 
          
          $ grep -i "xIpHidIuM" biomed/1472-6882-1-10.txt
          
          Xiphidium caeruleum leaves were
          Xiphidium caeruleum ground stem
          Xiphidium caeruleum [ 107 129 ]
          
<h4>

          
<h2>-C(#) command<h2>

<h3>Finally, in my opinion the most useful command to use with grep is -C (capital C.) This command is really useful with grep
as when you see the lines before and after a string of characters of you choice giving you more context of what is going on when that word is mentioned. 
This is extremely essential as it lets you skim the text where you found that word quickly and efficiently as it separates the times the characters were found with "--"
and also very versatile as you get to pick how many lines foward and back from the string of characters you want to output.
          
<h3>

Example 4 (1/2):

<h4>Without -C(#):
          
          $ grep "definition" biomed/1468-6708-3-1.txt
          
          drawback of this simple definition of 'healthy' is that
          report results using only the simpler definition.
          
<h4>

<h4>With -C(#):
          
          $ grep -C2 "definition" biomed/1468-6708-3-1.txt
          
          throughout). Since people reported their health every 6
          months, YHL has a reasonably continuous distribution. A
          drawback of this simple definition of 'healthy' is that
          it does not distinguish between fair or poor health and
          death, since all are considered 'not healthy'. We also
--
          value to each level of EVGFP [ 19 ] . Preliminary results
          were similar for the two approaches, however, and we
          report results using only the simpler definition.
          The calculations had to be modified to include the 438
          persons in the second African American cohort, who have 
          
<h4>

Example 4 (2/2):
          
<h4>Without -C(#):
          
          $ grep "QALY" biomed/1468-6708-3-1.txt
          
          QALY Quality-adjusted life years  
          
With -C(#):          
          $ grep -C1 "QALY" biomed/1468-6708-3-1.txt
          
          poor?
          QALY Quality-adjusted life years
          YHL Years of healthy life
          
<h4>

This command is a mix of -A (output lines after the line were the string of characters was found) and 
-B (output lines beforethe line were the string of characters was found) yet it provides the best of both commands. <h3>
