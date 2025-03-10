# Hash Table
This project demonstrates a simple has table with an unordered map. It also computes the hash value of a string key with the default hash function.
## Number 1
```c++
    // the following array would take O(N) or O(logN) steps to search using linear or binary search, respectively
    // int numbers[5] = {200, 400, 100, 50, 350};
    // let's use an unordered map, which can potentially cut the efficiency down to O(1).
    // We'll use a string key to store each number
    unordered_map<string, int> ints_map =
    {{"number1", 200},{"number2", 400},{"number3", 100},{"number4", 50},{"number5", 350}};
    // now we can search for and access an element immediately using its key.
    // Assuming the element was able to be placed in the correct computed index (no collision occurred), then this will result in an efficiency of O(1).
    // all you have to do is change the key below and it will return the value
    const auto desired_number = ints_map.find("number2");
    if (desired_number != ints_map.end()) {
        cout << desired_number->first << " is " << desired_number->second << endl;
    } else {
        cout << "The key was not found.\n";
    }
```
## Number 2
```c++
    // Now let's use the default hash function to compute the hash value of my name as a key
    // store my name as a string, to be used as the key pass to the hash function object
    string key = "Mikaela";
    // create a hash function object that is optimized for string data type
    hash<string> hash_object;
    // create an unsigned integer type to store the hash value in bytes; passing the key to the hash function object
    size_t hash_value = hash_object(key);
    // output the hash value
    cout << "The hash value of my name - " << key << " - is: " << hash_value << endl;
```
## Number 3
Here is my diagram of how tombstones create inefficiencies in PDF and rendered HTML:
[Lab 5.pdf](https://github.com/user-attachments/files/19153593/Lab.5.pdf)
<html xmlns:v="urn:schemas-microsoft-com:vml"
xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:w="urn:schemas-microsoft-com:office:word"
xmlns:m="http://schemas.microsoft.com/office/2004/12/omml"
xmlns="http://www.w3.org/TR/REC-html40">

<head>
<meta http-equiv=Content-Type content="text/html; charset=utf-8">
<meta name=ProgId content=Word.Document>
<meta name=Generator content="Microsoft Word 15">
<meta name=Originator content="Microsoft Word 15">
<link rel=File-List href="Lab%205.fld/filelist.xml">
<link rel=Edit-Time-Data href="Lab%205.fld/editdata.mso">
<!--[if !mso]>
<style>
v\:* {behavior:url(#default#VML);}
o\:* {behavior:url(#default#VML);}
w\:* {behavior:url(#default#VML);}
.shape {behavior:url(#default#VML);}
</style>
<![endif]--><!--[if gte mso 9]><xml>
 <o:DocumentProperties>
  <o:Author>Mikaela Rhoads</o:Author>
  <o:LastAuthor>Mikaela Rhoads</o:LastAuthor>
  <o:Revision>2</o:Revision>
  <o:TotalTime>3</o:TotalTime>
  <o:Created>2025-03-10T00:48:00Z</o:Created>
  <o:LastSaved>2025-03-10T00:48:00Z</o:LastSaved>
  <o:Pages>2</o:Pages>
  <o:Words>281</o:Words>
  <o:Characters>1604</o:Characters>
  <o:Lines>13</o:Lines>
  <o:Paragraphs>3</o:Paragraphs>
  <o:CharactersWithSpaces>1882</o:CharactersWithSpaces>
  <o:Version>16.00</o:Version>
 </o:DocumentProperties>
 <o:OfficeDocumentSettings>
  <o:AllowPNG/>
 </o:OfficeDocumentSettings>
</xml><![endif]-->
<link rel=themeData href="Lab%205.fld/themedata.thmx">
<link rel=colorSchemeMapping href="Lab%205.fld/colorschememapping.xml">
<!--[if gte mso 9]><xml>
 <w:WordDocument>
  <w:SpellingState>Clean</w:SpellingState>
  <w:GrammarState>Clean</w:GrammarState>
  <w:TrackMoves>false</w:TrackMoves>
  <w:TrackFormatting/>
  <w:PunctuationKerning/>
  <w:ValidateAgainstSchemas/>
  <w:SaveIfXMLInvalid>false</w:SaveIfXMLInvalid>
  <w:IgnoreMixedContent>false</w:IgnoreMixedContent>
  <w:AlwaysShowPlaceholderText>false</w:AlwaysShowPlaceholderText>
  <w:DoNotPromoteQF/>
  <w:LidThemeOther>EN-US</w:LidThemeOther>
  <w:LidThemeAsian>X-NONE</w:LidThemeAsian>
  <w:LidThemeComplexScript>X-NONE</w:LidThemeComplexScript>
  <w:Compatibility>
   <w:BreakWrappedTables/>
   <w:SnapToGridInCell/>
   <w:WrapTextWithPunct/>
   <w:UseAsianBreakRules/>
   <w:DontGrowAutofit/>
   <w:SplitPgBreakAndParaMark/>
   <w:EnableOpenTypeKerning/>
   <w:DontFlipMirrorIndents/>
   <w:OverrideTableStyleHps/>
  </w:Compatibility>
  <m:mathPr>
   <m:mathFont m:val="Cambria Math"/>
   <m:brkBin m:val="before"/>
   <m:brkBinSub m:val="&#45;-"/>
   <m:smallFrac m:val="off"/>
   <m:dispDef/>
   <m:lMargin m:val="0"/>
   <m:rMargin m:val="0"/>
   <m:defJc m:val="centerGroup"/>
   <m:wrapIndent m:val="1440"/>
   <m:intLim m:val="subSup"/>
   <m:naryLim m:val="undOvr"/>
  </m:mathPr></w:WordDocument>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <w:LatentStyles DefLockedState="false" DefUnhideWhenUsed="false"
  DefSemiHidden="false" DefQFormat="false" DefPriority="99"
  LatentStyleCount="376">
  <w:LsdException Locked="false" Priority="0" QFormat="true" Name="Normal"/>
  <w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 1"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 2"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 3"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 4"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 5"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 6"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 7"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 8"/>
  <w:LsdException Locked="false" Priority="9" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="heading 9"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index 9"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 1"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 2"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 3"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 4"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 5"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 6"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 7"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 8"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" Name="toc 9"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footnote text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="header"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footer"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="index heading"/>
  <w:LsdException Locked="false" Priority="35" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="caption"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="table of figures"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="envelope address"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="envelope return"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="footnote reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="line number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="page number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="endnote reference"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="endnote text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="table of authorities"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="macro"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="toa heading"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Bullet 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Number 5"/>
  <w:LsdException Locked="false" Priority="10" QFormat="true" Name="Title"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Closing"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Signature"/>
  <w:LsdException Locked="false" Priority="1" SemiHidden="true"
   UnhideWhenUsed="true" Name="Default Paragraph Font"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="List Continue 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Message Header"/>
  <w:LsdException Locked="false" Priority="11" QFormat="true" Name="Subtitle"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Salutation"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Date"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text First Indent"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text First Indent 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Note Heading"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Body Text Indent 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Block Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Hyperlink"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="FollowedHyperlink"/>
  <w:LsdException Locked="false" Priority="22" QFormat="true" Name="Strong"/>
  <w:LsdException Locked="false" Priority="20" QFormat="true" Name="Emphasis"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Document Map"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Plain Text"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="E-mail Signature"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Top of Form"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Bottom of Form"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal (Web)"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Acronym"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Address"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Cite"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Code"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Definition"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Keyboard"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Preformatted"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Sample"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Typewriter"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="HTML Variable"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Normal Table"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="annotation subject"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="No List"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Outline List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Simple 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Classic 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Colorful 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Columns 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Grid 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 4"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 5"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 7"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table List 8"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table 3D effects 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Contemporary"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Elegant"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Professional"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Subtle 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Subtle 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 1"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 2"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Web 3"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Balloon Text"/>
  <w:LsdException Locked="false" Priority="39" Name="Table Grid"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Table Theme"/>
  <w:LsdException Locked="false" SemiHidden="true" Name="Placeholder Text"/>
  <w:LsdException Locked="false" Priority="1" QFormat="true" Name="No Spacing"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 1"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 1"/>
  <w:LsdException Locked="false" SemiHidden="true" Name="Revision"/>
  <w:LsdException Locked="false" Priority="34" QFormat="true"
   Name="List Paragraph"/>
  <w:LsdException Locked="false" Priority="29" QFormat="true" Name="Quote"/>
  <w:LsdException Locked="false" Priority="30" QFormat="true"
   Name="Intense Quote"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 1"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 1"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 1"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 1"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 1"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 2"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 2"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 2"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 2"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 2"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 2"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 3"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 3"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 3"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 3"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 3"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 3"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 4"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 4"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 4"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 4"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 4"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 4"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 5"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 5"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 5"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 5"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 5"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 5"/>
  <w:LsdException Locked="false" Priority="60" Name="Light Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="61" Name="Light List Accent 6"/>
  <w:LsdException Locked="false" Priority="62" Name="Light Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="63" Name="Medium Shading 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="64" Name="Medium Shading 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="65" Name="Medium List 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="66" Name="Medium List 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="67" Name="Medium Grid 1 Accent 6"/>
  <w:LsdException Locked="false" Priority="68" Name="Medium Grid 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="69" Name="Medium Grid 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="70" Name="Dark List Accent 6"/>
  <w:LsdException Locked="false" Priority="71" Name="Colorful Shading Accent 6"/>
  <w:LsdException Locked="false" Priority="72" Name="Colorful List Accent 6"/>
  <w:LsdException Locked="false" Priority="73" Name="Colorful Grid Accent 6"/>
  <w:LsdException Locked="false" Priority="19" QFormat="true"
   Name="Subtle Emphasis"/>
  <w:LsdException Locked="false" Priority="21" QFormat="true"
   Name="Intense Emphasis"/>
  <w:LsdException Locked="false" Priority="31" QFormat="true"
   Name="Subtle Reference"/>
  <w:LsdException Locked="false" Priority="32" QFormat="true"
   Name="Intense Reference"/>
  <w:LsdException Locked="false" Priority="33" QFormat="true" Name="Book Title"/>
  <w:LsdException Locked="false" Priority="37" SemiHidden="true"
   UnhideWhenUsed="true" Name="Bibliography"/>
  <w:LsdException Locked="false" Priority="39" SemiHidden="true"
   UnhideWhenUsed="true" QFormat="true" Name="TOC Heading"/>
  <w:LsdException Locked="false" Priority="41" Name="Plain Table 1"/>
  <w:LsdException Locked="false" Priority="42" Name="Plain Table 2"/>
  <w:LsdException Locked="false" Priority="43" Name="Plain Table 3"/>
  <w:LsdException Locked="false" Priority="44" Name="Plain Table 4"/>
  <w:LsdException Locked="false" Priority="45" Name="Plain Table 5"/>
  <w:LsdException Locked="false" Priority="40" Name="Grid Table Light"/>
  <w:LsdException Locked="false" Priority="46" Name="Grid Table 1 Light"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark"/>
  <w:LsdException Locked="false" Priority="51" Name="Grid Table 6 Colorful"/>
  <w:LsdException Locked="false" Priority="52" Name="Grid Table 7 Colorful"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 1"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 1"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 1"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 2"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 2"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 2"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 3"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 3"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 3"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 4"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 4"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 4"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 5"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 5"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 5"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="46"
   Name="Grid Table 1 Light Accent 6"/>
  <w:LsdException Locked="false" Priority="47" Name="Grid Table 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="48" Name="Grid Table 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="49" Name="Grid Table 4 Accent 6"/>
  <w:LsdException Locked="false" Priority="50" Name="Grid Table 5 Dark Accent 6"/>
  <w:LsdException Locked="false" Priority="51"
   Name="Grid Table 6 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="52"
   Name="Grid Table 7 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="46" Name="List Table 1 Light"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark"/>
  <w:LsdException Locked="false" Priority="51" Name="List Table 6 Colorful"/>
  <w:LsdException Locked="false" Priority="52" Name="List Table 7 Colorful"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 1"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 1"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 1"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 1"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 1"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 1"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 2"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 2"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 2"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 2"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 2"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 2"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 3"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 3"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 3"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 3"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 3"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 3"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 4"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 4"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 4"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 4"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 4"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 4"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 5"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 5"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 5"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 5"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 5"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 5"/>
  <w:LsdException Locked="false" Priority="46"
   Name="List Table 1 Light Accent 6"/>
  <w:LsdException Locked="false" Priority="47" Name="List Table 2 Accent 6"/>
  <w:LsdException Locked="false" Priority="48" Name="List Table 3 Accent 6"/>
  <w:LsdException Locked="false" Priority="49" Name="List Table 4 Accent 6"/>
  <w:LsdException Locked="false" Priority="50" Name="List Table 5 Dark Accent 6"/>
  <w:LsdException Locked="false" Priority="51"
   Name="List Table 6 Colorful Accent 6"/>
  <w:LsdException Locked="false" Priority="52"
   Name="List Table 7 Colorful Accent 6"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Mention"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Smart Hyperlink"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Hashtag"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Unresolved Mention"/>
  <w:LsdException Locked="false" SemiHidden="true" UnhideWhenUsed="true"
   Name="Smart Link"/>
 </w:LatentStyles>
</xml><![endif]-->

<![endif]--><!--[if gte mso 9]><xml>
 <o:shapedefaults v:ext="edit" spidmax="1026"/>
</xml><![endif]--><!--[if gte mso 9]><xml>
 <o:shapelayout v:ext="edit">
  <o:idmap v:ext="edit" data="1"/>
 </o:shapelayout></xml><![endif]-->
</head>

<body lang=EN-US style='tab-interval:.5in;word-wrap:break-word'>

<div class=WordSection1>

<p class=MsoNormal>3) Tombstones create inefficiencies because they leave a
marked gap where a deleted element used to reside. This can make searching or
deleting a different element less efficient because it creates extra
unnecessary space between the home position that the element should have been
placed in (per the hash function and the computed hash value). Because C++ will
always start at the home position, tombstones that exist between the home
position and the position where the element was ultimately placed cause
iteration to take longer because it <span class=GramE>has to</span> go through
the empty tombstones. The figure below demonstrates:</p>

<p class=MsoNormal>If we have the following keys stored in the applicable
cells/hash values:</p>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0in 5.4pt 0in 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033335<span
  style='background:red;mso-highlight:red'><o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;mso-yfti-lastrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1</p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18</p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19</p>
  </td>
 </tr>
</table>

<p class=MsoNormal>Now let’s say we try to add 0024333 (h(k) = 15. Because cell
15 is occupied, it would be placed at the first open cell (19).</p>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0in 5.4pt 0in 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033335<span
  style='background:red;mso-highlight:red'><o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><span
  style='background:lime;mso-highlight:lime'>0024333</span><o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1;mso-yfti-lastrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
</table>

<p class=MsoNormal>Now let’s say we delete 003335 in cell 17. We will have a
tombstone.</p>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0in 5.4pt 0in 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><s><span
  style='background:red;mso-highlight:red'>0033335<o:p></o:p></span></s></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3;mso-yfti-lastrow:yes'>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.4pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-top-alt:solid windowtext .5pt;
  mso-border-right-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
</table>

<p class=MsoNormal><o:p>&nbsp;</o:p></p>

<p class=MsoNormal>Finally, if we now want to search for the element we added before
(0024333), the complexity takes an unnecessary step because C++ will start
where it should have been placed (cell 15) and it must traverse over the empty
tombstone that will never yield the result. </p>

<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0
 style='margin-left:.75pt;border-collapse:collapse;border:none;mso-border-alt:
 solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:0in 5.4pt 0in 5.4pt'>
 <tr style='mso-yfti-irow:0;mso-yfti-firstrow:yes'>
  <td width=77 valign=top style='width:58.1pt;border:solid windowtext 1.0pt;
  border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:accent6;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:solid windowtext 1.0pt;
  border-left:none;border-bottom:solid #70AD47 1.0pt;mso-border-bottom-themecolor:
  accent6;border-right:solid windowtext 1.0pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:1'>
  <td width=77 valign=top style='width:58.1pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid #70AD47 .5pt;mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:2'>
  <td width=77 valign=top style='width:58.1pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='mso-no-proof:yes'><!--[if gte vml 1]><v:shapetype
   id="_x0000_t75" coordsize="21600,21600" o:spt="75" o:preferrelative="t"
   path="m@4@5l@4@11@9@11@9@5xe" filled="f" stroked="f">
   <v:stroke joinstyle="miter"/>
   <v:formulas>
    <v:f eqn="if lineDrawn pixelLineWidth 0"/>
    <v:f eqn="sum @0 1 0"/>
    <v:f eqn="sum 0 0 @1"/>
    <v:f eqn="prod @2 1 2"/>
    <v:f eqn="prod @3 21600 pixelWidth"/>
    <v:f eqn="prod @3 21600 pixelHeight"/>
    <v:f eqn="sum @0 0 1"/>
    <v:f eqn="prod @6 1 2"/>
    <v:f eqn="prod @7 21600 pixelWidth"/>
    <v:f eqn="sum @8 21600 0"/>
    <v:f eqn="prod @7 21600 pixelHeight"/>
    <v:f eqn="sum @10 21600 0"/>
   </v:formulas>
   <v:path o:extrusionok="f" gradientshapeok="t" o:connecttype="rect"/>
   <o:lock v:ext="edit" aspectratio="t"/>
  </v:shapetype><v:shape id="_x0000_i1029" type="#_x0000_t75" alt="Arrow Up with solid fill"
   style='width:22pt;height:23pt;visibility:visible' o:gfxdata="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
X7zZ6j8nEdqxYgIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIE
CBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAg
QIAAgV4J/B/2498rVrERPgAAAABJRU5ErkJgglBLAwQKAAAAAAAAACEAZ8ts5KYDAACmAwAAFAAA
AGRycy9tZWRpYS9pbWFnZTIuc3ZnPHN2ZyB2aWV3Qm94PSIwIDAgOTYgOTYiIHhtbG5zPSJodHRw
Oi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5
OTkveGxpbmsiIGlkPSJJY29uc19BcnJvd1VwIiBvdmVyZmxvdz0iaGlkZGVuIj48c3R5bGU+DQou
TXNmdE9mY1RobV9BY2NlbnQ2X0ZpbGxfdjIgew0KIGZpbGw6IzcwQUQ0NzsgDQp9DQo8L3N0eWxl
Pg0KPHBhdGggZD0iTTUxLjAzMSA4OC45NTEgNTEuMDMxIDE0LjE5MiA1OS45MzEgMjMuMDkyQzYx
LjA5MDggMjQuMjUxOCA2Mi45NzEyIDI0LjI1MTggNjQuMTMxIDIzLjA5MiA2NS4yOTA4IDIxLjkz
MjIgNjUuMjkwOCAyMC4wNTE4IDY0LjEzMSAxOC44OTJMNTAuMTMxIDQuOUM0OS4wMjY0IDMuNzQw
MiA0Ny4xOTA4IDMuNjk1NDMgNDYuMDMxIDQuOCA0NS45OTY5IDQuODMyNTIgNDUuOTYzNSA0Ljg2
NTg2IDQ1LjkzMSA0LjlMMzEuOTQxIDE4Ljg5QzMwLjc4MTIgMTkuOTk0NiAzMC43MzY0IDIxLjgz
MDIgMzEuODQxIDIyLjk5IDMxLjg3MzUgMjMuMDI0MSAzMS45MDY5IDIzLjA1NzUgMzEuOTQxIDIz
LjA5IDMzLjA0NTYgMjQuMjQ5OCAzNC44ODEyIDI0LjI5NDYgMzYuMDQxIDIzLjE5IDM2LjA3NTEg
MjMuMTU3NSAzNi4xMDg1IDIzLjEyNDEgMzYuMTQxIDIzLjA5TDQ1LjAzNiAxNC4xOTUgNDUuMDM2
IDg4Ljk1MUM0NS4wMzYgOTAuNjA3OCA0Ni4zNzkxIDkxLjk1MSA0OC4wMzYgOTEuOTUxIDQ5LjY5
MjkgOTEuOTUxIDUxLjAzNiA5MC42MDc4IDUxLjAzNiA4OC45NTFaIiBjbGFzcz0iTXNmdE9mY1Ro
bV9BY2NlbnQ2X0ZpbGxfdjIiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBzdHJva2Ut
bGluZWNhcD0iYnV0dCIgc3Ryb2tlLWxpbmVqb2luPSJtaXRlciIgc3Ryb2tlLW1pdGVybGltaXQ9
IjQiIGZpbGw9IiM3MEFENDciIGZpbGwtb3BhY2l0eT0iMSIvPjwvc3ZnPlBLAwQUAAYACAAAACEA
MUku9t0AAAAIAQAADwAAAGRycy9kb3ducmV2LnhtbEyPzWrDMBCE74W+g9hCb42c2DipYzmElkKh
UMjPA8jWVjaxVsZSEvftu+2lucyyDDs7X7mZXC8uOIbOk4L5LAGB1HjTkVVwPLw9rUCEqMno3hMq
+MYAm+r+rtSF8Vfa4WUfreAQCoVW0MY4FFKGpkWnw8wPSOx9+dHpyOtopRn1lcNdLxdJkkunO+IP
rR7wpcXmtD87BafkcEzpPcOdzT7tMrUfdZPXSj0+TK9rlu0aRMQp/l/ALwP3h4qL1f5MJoheAdPE
P2UvS59B1DzzOciqlLcA1Q8AAAD//wMAUEsDBBQABgAIAAAAIQAiVg7uxwAAAKUBAAAZAAAAZHJz
L19yZWxzL2Uyb0RvYy54bWwucmVsc7yQsWoDMQyG90LewWjv+e6GUkp8WUoha0gfQNg6n8lZNpYb
mrePaZYGAt06SuL//g9td99xVWcqEhIbGLoeFLFNLrA38Hn8eH4FJRXZ4ZqYDFxIYDdtnrYHWrG2
kCwhi2oUFgNLrflNa7ELRZQuZeJ2mVOJWNtYvM5oT+hJj33/ostvBkx3TLV3BsrejaCOl9ya/2an
eQ6W3pP9isT1QYUOsXU3IBZP1UAkF/C2HDs5e9CPHYb/cRi6zD8O+u650xUAAP//AwBQSwECLQAU
AAYACAAAACEAqNbHqBMBAABJAgAAEwAAAAAAAAAAAAAAAAAAAAAAW0NvbnRlbnRfVHlwZXNdLnht
bFBLAQItABQABgAIAAAAIQA4/SH/1gAAAJQBAAALAAAAAAAAAAAAAAAAAEQBAABfcmVscy8ucmVs
c1BLAQItABQABgAIAAAAIQDjA8PHzgEAANkDAAAOAAAAAAAAAAAAAAAAAEMCAABkcnMvZTJvRG9j
LnhtbFBLAQItAAoAAAAAAAAAIQDauwIznxgAAJ8YAAAUAAAAAAAAAAAAAAAAAD0EAABkcnMvbWVk
aWEvaW1hZ2UxLnBuZ1BLAQItAAoAAAAAAAAAIQBny2zkpgMAAKYDAAAUAAAAAAAAAAAAAAAAAA4d
AABkcnMvbWVkaWEvaW1hZ2UyLnN2Z1BLAQItABQABgAIAAAAIQAxSS723QAAAAgBAAAPAAAAAAAA
AAAAAAAAAOYgAABkcnMvZG93bnJldi54bWxQSwECLQAUAAYACAAAACEAIlYO7scAAAClAQAAGQAA
AAAAAAAAAAAAAADwIQAAZHJzL19yZWxzL2Uyb0RvYy54bWwucmVsc1BLBQYAAAAABwAHAL4BAADu
IgAAAAA=
">
   <v:imagedata src="Lab%205.fld/image001.png" o:title="" cropleft="-39322f"
    cropright="-38666f"/>
  </v:shape><![endif]--><![if !vml]><img width=22 height=23
  src="Lab%205.fld/image002.png" alt="Arrow Up with solid fill" v:shapes="_x0000_i1029"><![endif]></span><o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid #70AD47 1.0pt;
  mso-border-bottom-themecolor:accent6;mso-border-bottom-alt:solid #70AD47 .5pt;
  mso-border-bottom-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:3'>
  <td width=77 valign=top style='width:58.1pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:
  accent6;mso-border-alt:solid windowtext .5pt;mso-border-top-alt:solid #70AD47 .5pt;
  mso-border-top-themecolor:accent6;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  mso-border-left-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  mso-border-top-alt:solid #70AD47 .5pt;mso-border-top-themecolor:accent6;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:4'>
  <td width=77 valign=top style='width:58.1pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:5'>
  <td width=77 valign=top style='width:58.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='mso-no-proof:yes'><!--[if gte vml 1]><v:shape
   id="_x0000_i1028" type="#_x0000_t75" alt="Arrow Up with solid fill" style='width:22pt;
   height:23pt;visibility:visible' o:gfxdata="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
X7zZ6j8nEdqxYgIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIE
CBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAg
QIAAgV4J/B/2498rVrERPgAAAABJRU5ErkJgglBLAwQKAAAAAAAAACEAZ8ts5KYDAACmAwAAFAAA
AGRycy9tZWRpYS9pbWFnZTIuc3ZnPHN2ZyB2aWV3Qm94PSIwIDAgOTYgOTYiIHhtbG5zPSJodHRw
Oi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5
OTkveGxpbmsiIGlkPSJJY29uc19BcnJvd1VwIiBvdmVyZmxvdz0iaGlkZGVuIj48c3R5bGU+DQou
TXNmdE9mY1RobV9BY2NlbnQ2X0ZpbGxfdjIgew0KIGZpbGw6IzcwQUQ0NzsgDQp9DQo8L3N0eWxl
Pg0KPHBhdGggZD0iTTUxLjAzMSA4OC45NTEgNTEuMDMxIDE0LjE5MiA1OS45MzEgMjMuMDkyQzYx
LjA5MDggMjQuMjUxOCA2Mi45NzEyIDI0LjI1MTggNjQuMTMxIDIzLjA5MiA2NS4yOTA4IDIxLjkz
MjIgNjUuMjkwOCAyMC4wNTE4IDY0LjEzMSAxOC44OTJMNTAuMTMxIDQuOUM0OS4wMjY0IDMuNzQw
MiA0Ny4xOTA4IDMuNjk1NDMgNDYuMDMxIDQuOCA0NS45OTY5IDQuODMyNTIgNDUuOTYzNSA0Ljg2
NTg2IDQ1LjkzMSA0LjlMMzEuOTQxIDE4Ljg5QzMwLjc4MTIgMTkuOTk0NiAzMC43MzY0IDIxLjgz
MDIgMzEuODQxIDIyLjk5IDMxLjg3MzUgMjMuMDI0MSAzMS45MDY5IDIzLjA1NzUgMzEuOTQxIDIz
LjA5IDMzLjA0NTYgMjQuMjQ5OCAzNC44ODEyIDI0LjI5NDYgMzYuMDQxIDIzLjE5IDM2LjA3NTEg
MjMuMTU3NSAzNi4xMDg1IDIzLjEyNDEgMzYuMTQxIDIzLjA5TDQ1LjAzNiAxNC4xOTUgNDUuMDM2
IDg4Ljk1MUM0NS4wMzYgOTAuNjA3OCA0Ni4zNzkxIDkxLjk1MSA0OC4wMzYgOTEuOTUxIDQ5LjY5
MjkgOTEuOTUxIDUxLjAzNiA5MC42MDc4IDUxLjAzNiA4OC45NTFaIiBjbGFzcz0iTXNmdE9mY1Ro
bV9BY2NlbnQ2X0ZpbGxfdjIiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBzdHJva2Ut
bGluZWNhcD0iYnV0dCIgc3Ryb2tlLWxpbmVqb2luPSJtaXRlciIgc3Ryb2tlLW1pdGVybGltaXQ9
IjQiIGZpbGw9IiM3MEFENDciIGZpbGwtb3BhY2l0eT0iMSIvPjwvc3ZnPlBLAwQUAAYACAAAACEA
MUku9t0AAAAIAQAADwAAAGRycy9kb3ducmV2LnhtbEyPzWrDMBCE74W+g9hCb42c2DipYzmElkKh
UMjPA8jWVjaxVsZSEvftu+2lucyyDDs7X7mZXC8uOIbOk4L5LAGB1HjTkVVwPLw9rUCEqMno3hMq
+MYAm+r+rtSF8Vfa4WUfreAQCoVW0MY4FFKGpkWnw8wPSOx9+dHpyOtopRn1lcNdLxdJkkunO+IP
rR7wpcXmtD87BafkcEzpPcOdzT7tMrUfdZPXSj0+TK9rlu0aRMQp/l/ALwP3h4qL1f5MJoheAdPE
P2UvS59B1DzzOciqlLcA1Q8AAAD//wMAUEsDBBQABgAIAAAAIQAiVg7uxwAAAKUBAAAZAAAAZHJz
L19yZWxzL2Uyb0RvYy54bWwucmVsc7yQsWoDMQyG90LewWjv+e6GUkp8WUoha0gfQNg6n8lZNpYb
mrePaZYGAt06SuL//g9td99xVWcqEhIbGLoeFLFNLrA38Hn8eH4FJRXZ4ZqYDFxIYDdtnrYHWrG2
kCwhi2oUFgNLrflNa7ELRZQuZeJ2mVOJWNtYvM5oT+hJj33/ostvBkx3TLV3BsrejaCOl9ya/2an
eQ6W3pP9isT1QYUOsXU3IBZP1UAkF/C2HDs5e9CPHYb/cRi6zD8O+u650xUAAP//AwBQSwECLQAU
AAYACAAAACEAqNbHqBMBAABJAgAAEwAAAAAAAAAAAAAAAAAAAAAAW0NvbnRlbnRfVHlwZXNdLnht
bFBLAQItABQABgAIAAAAIQA4/SH/1gAAAJQBAAALAAAAAAAAAAAAAAAAAEQBAABfcmVscy8ucmVs
c1BLAQItABQABgAIAAAAIQDjA8PHzgEAANkDAAAOAAAAAAAAAAAAAAAAAEMCAABkcnMvZTJvRG9j
LnhtbFBLAQItAAoAAAAAAAAAIQDauwIznxgAAJ8YAAAUAAAAAAAAAAAAAAAAAD0EAABkcnMvbWVk
aWEvaW1hZ2UxLnBuZ1BLAQItAAoAAAAAAAAAIQBny2zkpgMAAKYDAAAUAAAAAAAAAAAAAAAAAA4d
AABkcnMvbWVkaWEvaW1hZ2UyLnN2Z1BLAQItABQABgAIAAAAIQAxSS723QAAAAgBAAAPAAAAAAAA
AAAAAAAAAOYgAABkcnMvZG93bnJldi54bWxQSwECLQAUAAYACAAAACEAIlYO7scAAAClAQAAGQAA
AAAAAAAAAAAAAADwIQAAZHJzL19yZWxzL2Uyb0RvYy54bWwucmVsc1BLBQYAAAAABwAHAL4BAADu
IgAAAAA=
">
   <v:imagedata src="Lab%205.fld/image001.png" o:title="" cropleft="-39322f"
    cropright="-38666f"/>
  </v:shape><![endif]--><![if !vml]><img width=22 height=23
  src="Lab%205.fld/image002.png" alt="Arrow Up with solid fill" v:shapes="_x0000_i1028"><![endif]></span></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:6'>
  <td width=77 valign=top style='width:58.1pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:7'>
  <td width=77 valign=top style='width:58.1pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:8'>
  <td width=77 valign=top style='width:58.1pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='mso-no-proof:yes'><!--[if gte vml 1]><v:shape
   id="_x0000_i1027" type="#_x0000_t75" alt="Arrow Up with solid fill" style='width:23pt;
   height:23pt;visibility:visible' o:gfxdata="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
X7zZ6j8nEdqxYgIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIE
CBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAgQIAAAQIECBAg
QIAAgV4J/B/2498rVrERPgAAAABJRU5ErkJgglBLAwQKAAAAAAAAACEAZ8ts5KYDAACmAwAAFAAA
AGRycy9tZWRpYS9pbWFnZTIuc3ZnPHN2ZyB2aWV3Qm94PSIwIDAgOTYgOTYiIHhtbG5zPSJodHRw
Oi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5
OTkveGxpbmsiIGlkPSJJY29uc19BcnJvd1VwIiBvdmVyZmxvdz0iaGlkZGVuIj48c3R5bGU+DQou
TXNmdE9mY1RobV9BY2NlbnQ2X0ZpbGxfdjIgew0KIGZpbGw6IzcwQUQ0NzsgDQp9DQo8L3N0eWxl
Pg0KPHBhdGggZD0iTTUxLjAzMSA4OC45NTEgNTEuMDMxIDE0LjE5MiA1OS45MzEgMjMuMDkyQzYx
LjA5MDggMjQuMjUxOCA2Mi45NzEyIDI0LjI1MTggNjQuMTMxIDIzLjA5MiA2NS4yOTA4IDIxLjkz
MjIgNjUuMjkwOCAyMC4wNTE4IDY0LjEzMSAxOC44OTJMNTAuMTMxIDQuOUM0OS4wMjY0IDMuNzQw
MiA0Ny4xOTA4IDMuNjk1NDMgNDYuMDMxIDQuOCA0NS45OTY5IDQuODMyNTIgNDUuOTYzNSA0Ljg2
NTg2IDQ1LjkzMSA0LjlMMzEuOTQxIDE4Ljg5QzMwLjc4MTIgMTkuOTk0NiAzMC43MzY0IDIxLjgz
MDIgMzEuODQxIDIyLjk5IDMxLjg3MzUgMjMuMDI0MSAzMS45MDY5IDIzLjA1NzUgMzEuOTQxIDIz
LjA5IDMzLjA0NTYgMjQuMjQ5OCAzNC44ODEyIDI0LjI5NDYgMzYuMDQxIDIzLjE5IDM2LjA3NTEg
MjMuMTU3NSAzNi4xMDg1IDIzLjEyNDEgMzYuMTQxIDIzLjA5TDQ1LjAzNiAxNC4xOTUgNDUuMDM2
IDg4Ljk1MUM0NS4wMzYgOTAuNjA3OCA0Ni4zNzkxIDkxLjk1MSA0OC4wMzYgOTEuOTUxIDQ5LjY5
MjkgOTEuOTUxIDUxLjAzNiA5MC42MDc4IDUxLjAzNiA4OC45NTFaIiBjbGFzcz0iTXNmdE9mY1Ro
bV9BY2NlbnQ2X0ZpbGxfdjIiIHN0cm9rZT0ibm9uZSIgc3Ryb2tlLXdpZHRoPSIxIiBzdHJva2Ut
bGluZWNhcD0iYnV0dCIgc3Ryb2tlLWxpbmVqb2luPSJtaXRlciIgc3Ryb2tlLW1pdGVybGltaXQ9
IjQiIGZpbGw9IiM3MEFENDciIGZpbGwtb3BhY2l0eT0iMSIvPjwvc3ZnPlBLAwQUAAYACAAAACEA
sCOwPN4AAAAIAQAADwAAAGRycy9kb3ducmV2LnhtbEyPQU/CQBCF7yb+h82QeDGyhViipVuiooEY
OIh4X7pD29idbXYXqP+e0Ytc3mTyMm/el89624oj+tA4UjAaJiCQSmcaqhRsP9/uHkCEqMno1hEq
+MEAs+L6KteZcSf6wOMmVoJDKGRaQR1jl0kZyhqtDkPXIbG3d97qyKuvpPH6xOG2leMkmUirG+IP
te7wpcbye3OwCm63yWKepunjwq/Wz1+r8fL1HZdK3Qz6+ZTlaQoiYh//L+CXgftDwcV27kAmiFYB
08Q/Ze8+ZZQdz8kIZJHLS4DiDAAA//8DAFBLAwQUAAYACAAAACEAIlYO7scAAAClAQAAGQAAAGRy
cy9fcmVscy9lMm9Eb2MueG1sLnJlbHO8kLFqAzEMhvdC3sFo7/nuhlJKfFlKIWtIH0DYOp/JWTaW
G5q3j2mWBgLdOkri//4PbXffcVVnKhISGxi6HhSxTS6wN/B5/Hh+BSUV2eGamAxcSGA3bZ62B1qx
tpAsIYtqFBYDS635TWuxC0WULmXidplTiVjbWLzOaE/oSY99/6LLbwZMd0y1dwbK3o2gjpfcmv9m
p3kOlt6T/YrE9UGFDrF1NyAWT9VAJBfwthw7OXvQjx2G/3EYusw/DvruudMVAAD//wMAUEsBAi0A
FAAGAAgAAAAhAKjWx6gTAQAASQIAABMAAAAAAAAAAAAAAAAAAAAAAFtDb250ZW50X1R5cGVzXS54
bWxQSwECLQAUAAYACAAAACEAOP0h/9YAAACUAQAACwAAAAAAAAAAAAAAAABEAQAAX3JlbHMvLnJl
bHNQSwECLQAUAAYACAAAACEAE3low84BAADYAwAADgAAAAAAAAAAAAAAAABDAgAAZHJzL2Uyb0Rv
Yy54bWxQSwECLQAKAAAAAAAAACEA2rsCM58YAACfGAAAFAAAAAAAAAAAAAAAAAA9BAAAZHJzL21l
ZGlhL2ltYWdlMS5wbmdQSwECLQAKAAAAAAAAACEAZ8ts5KYDAACmAwAAFAAAAAAAAAAAAAAAAAAO
HQAAZHJzL21lZGlhL2ltYWdlMi5zdmdQSwECLQAUAAYACAAAACEAsCOwPN4AAAAIAQAADwAAAAAA
AAAAAAAAAADmIAAAZHJzL2Rvd25yZXYueG1sUEsBAi0AFAAGAAgAAAAhACJWDu7HAAAApQEAABkA
AAAAAAAAAAAAAAAA8SEAAGRycy9fcmVscy9lMm9Eb2MueG1sLnJlbHNQSwUGAAAAAAcABwC+AQAA
7yIAAAAA
">
   <v:imagedata src="Lab%205.fld/image003.png" o:title="" cropleft="-39322f"
    cropright="-44892f"/>
  </v:shape><![endif]--><![if !vml]><img width=23 height=23
  src="Lab%205.fld/image004.png" alt="Arrow Up with solid fill" v:shapes="_x0000_i1027"><![endif]></span><o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid windowtext 1.0pt;
  mso-border-bottom-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:9'>
  <td width=77 valign=top style='width:58.1pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:10'>
  <td width=77 valign=top style='width:58.1pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid windowtext .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:11'>
  <td width=77 valign=top style='width:58.1pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='mso-no-proof:yes'><!--[if gte vml 1]><v:shape
   id="_x0000_i1026" type="#_x0000_t75" alt="Arrow Up with solid fill" style='width:22pt;
   height:23pt;visibility:visible' o:gfxdata="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
qV+82eo/JxHasWICBAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQIECAAAEC
BAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQIECAAAECBAgQ
IECAAIFeCfwf9uPfK1axET4AAAAASUVORK5CYIJQSwMECgAAAAAAAAAhAGfLbOSmAwAApgMAABQA
AABkcnMvbWVkaWEvaW1hZ2UyLnN2Zzxzdmcgdmlld0JveD0iMCAwIDk2IDk2IiB4bWxucz0iaHR0
cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8x
OTk5L3hsaW5rIiBpZD0iSWNvbnNfQXJyb3dVcCIgb3ZlcmZsb3c9ImhpZGRlbiI+PHN0eWxlPg0K
Lk1zZnRPZmNUaG1fQWNjZW50Nl9GaWxsX3YyIHsNCiBmaWxsOiM3MEFENDc7IA0KfQ0KPC9zdHls
ZT4NCjxwYXRoIGQ9Ik01MS4wMzEgODguOTUxIDUxLjAzMSAxNC4xOTIgNTkuOTMxIDIzLjA5MkM2
MS4wOTA4IDI0LjI1MTggNjIuOTcxMiAyNC4yNTE4IDY0LjEzMSAyMy4wOTIgNjUuMjkwOCAyMS45
MzIyIDY1LjI5MDggMjAuMDUxOCA2NC4xMzEgMTguODkyTDUwLjEzMSA0LjlDNDkuMDI2NCAzLjc0
MDIgNDcuMTkwOCAzLjY5NTQzIDQ2LjAzMSA0LjggNDUuOTk2OSA0LjgzMjUyIDQ1Ljk2MzUgNC44
NjU4NiA0NS45MzEgNC45TDMxLjk0MSAxOC44OUMzMC43ODEyIDE5Ljk5NDYgMzAuNzM2NCAyMS44
MzAyIDMxLjg0MSAyMi45OSAzMS44NzM1IDIzLjAyNDEgMzEuOTA2OSAyMy4wNTc1IDMxLjk0MSAy
My4wOSAzMy4wNDU2IDI0LjI0OTggMzQuODgxMiAyNC4yOTQ2IDM2LjA0MSAyMy4xOSAzNi4wNzUx
IDIzLjE1NzUgMzYuMTA4NSAyMy4xMjQxIDM2LjE0MSAyMy4wOUw0NS4wMzYgMTQuMTk1IDQ1LjAz
NiA4OC45NTFDNDUuMDM2IDkwLjYwNzggNDYuMzc5MSA5MS45NTEgNDguMDM2IDkxLjk1MSA0OS42
OTI5IDkxLjk1MSA1MS4wMzYgOTAuNjA3OCA1MS4wMzYgODguOTUxWiIgY2xhc3M9Ik1zZnRPZmNU
aG1fQWNjZW50Nl9GaWxsX3YyIiBzdHJva2U9Im5vbmUiIHN0cm9rZS13aWR0aD0iMSIgc3Ryb2tl
LWxpbmVjYXA9ImJ1dHQiIHN0cm9rZS1saW5lam9pbj0ibWl0ZXIiIHN0cm9rZS1taXRlcmxpbWl0
PSI0IiBmaWxsPSIjNzBBRDQ3IiBmaWxsLW9wYWNpdHk9IjEiLz48L3N2Zz5QSwMEFAAGAAgAAAAh
AM20v3LZAAAACAEAAA8AAABkcnMvZG93bnJldi54bWxMj09Lw0AQxe+C32EZwZvdKCVImk2RSryK
VWiP0+zkD2Znw+62id/e0Yte3jA85s37ldvFjepCIQ6eDdyvMlDEjbcDdwY+3uu7R1AxIVscPZOB
L4qwra6vSiysn/mNLvvUKQnhWKCBPqWp0Do2PTmMKz8Ri9f64DDJGjptA84S7kb9kGW5djiwfOhx
ol1Pzef+7AzUqeXdyysH63Ce21ofD3l2NOb2ZnneiDxtQCVa0t8F/DBIf6ik2Mmf2UY1GhCa9Kvi
rdeCcpKZZ6CrUv8HqL4BAAD//wMAUEsDBBQABgAIAAAAIQAiVg7uxwAAAKUBAAAZAAAAZHJzL19y
ZWxzL2Uyb0RvYy54bWwucmVsc7yQsWoDMQyG90LewWjv+e6GUkp8WUoha0gfQNg6n8lZNpYbmreP
aZYGAt06SuL//g9td99xVWcqEhIbGLoeFLFNLrA38Hn8eH4FJRXZ4ZqYDFxIYDdtnrYHWrG2kCwh
i2oUFgNLrflNa7ELRZQuZeJ2mVOJWNtYvM5oT+hJj33/ostvBkx3TLV3BsrejaCOl9ya/2aneQ6W
3pP9isT1QYUOsXU3IBZP1UAkF/C2HDs5e9CPHYb/cRi6zD8O+u650xUAAP//AwBQSwECLQAUAAYA
CAAAACEAqNbHqBMBAABJAgAAEwAAAAAAAAAAAAAAAAAAAAAAW0NvbnRlbnRfVHlwZXNdLnhtbFBL
AQItABQABgAIAAAAIQA4/SH/1gAAAJQBAAALAAAAAAAAAAAAAAAAAEQBAABfcmVscy8ucmVsc1BL
AQItABQABgAIAAAAIQBgRsPtzwEAANgDAAAOAAAAAAAAAAAAAAAAAEMCAABkcnMvZTJvRG9jLnht
bFBLAQItAAoAAAAAAAAAIQDauwIznxgAAJ8YAAAUAAAAAAAAAAAAAAAAAD4EAABkcnMvbWVkaWEv
aW1hZ2UxLnBuZ1BLAQItAAoAAAAAAAAAIQBny2zkpgMAAKYDAAAUAAAAAAAAAAAAAAAAAA8dAABk
cnMvbWVkaWEvaW1hZ2UyLnN2Z1BLAQItABQABgAIAAAAIQDNtL9y2QAAAAgBAAAPAAAAAAAAAAAA
AAAAAOcgAABkcnMvZG93bnJldi54bWxQSwECLQAUAAYACAAAACEAIlYO7scAAAClAQAAGQAAAAAA
AAAAAAAAAADtIQAAZHJzL19yZWxzL2Uyb0RvYy54bWwucmVsc1BLBQYAAAAABwAHAL4BAADrIgAA
AAA=
">
   <v:imagedata src="Lab%205.fld/image005.png" o:title="" cropleft="-39322f"
    cropright="-41943f"/>
  </v:shape><![endif]--><![if !vml]><img width=22 height=23
  src="Lab%205.fld/image006.png" alt="Arrow Up with solid fill" v:shapes="_x0000_i1026"><![endif]></span><o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;border-bottom:solid black 1.0pt;
  mso-border-bottom-themecolor:text1;mso-border-bottom-alt:solid black .5pt;
  mso-border-bottom-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:12'>
  <td width=77 valign=top style='width:58.1pt;border-top:none;border-left:solid windowtext 1.0pt;
  border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-top-alt:black;mso-border-top-themecolor:
  text1;mso-border-left-alt:windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:
  text1;mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border-top:none;border-left:none;
  border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033333<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033334<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='background:red;mso-highlight:red'>mark<o:p></o:p></span></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0033336<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border-top:none;border-left:
  none;border-bottom:solid black 1.0pt;mso-border-bottom-themecolor:text1;
  border-right:solid windowtext 1.0pt;mso-border-top-alt:solid black .5pt;
  mso-border-top-themecolor:text1;mso-border-left-alt:solid windowtext .5pt;
  mso-border-top-alt:black;mso-border-top-themecolor:text1;mso-border-left-alt:
  windowtext;mso-border-bottom-alt:black;mso-border-bottom-themecolor:text1;
  mso-border-right-alt:windowtext;mso-border-style-alt:solid;mso-border-width-alt:
  .5pt;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;line-height:normal'>0024333<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:13'>
  <td width=77 valign=top style='width:58.1pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>1<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>2<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>…<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>15<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>16<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>17<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>18<o:p></o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;mso-border-top-alt:
  solid black .5pt;mso-border-top-themecolor:text1;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'>19<o:p></o:p></p>
  </td>
 </tr>
 <tr style='mso-yfti-irow:14;mso-yfti-lastrow:yes'>
  <td width=77 valign=top style='width:58.1pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.2pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.3pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.35pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><o:p>&nbsp;</o:p></p>
  </td>
  <td width=78 valign=top style='width:58.45pt;border:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal align=center style='margin-bottom:0in;text-align:center;
  line-height:normal'><span style='mso-no-proof:yes'><!--[if gte vml 1]><v:shape
   id="Graphic_x0020_1" o:spid="_x0000_i1025" type="#_x0000_t75" alt="Arrow Up with solid fill"
   style='width:21pt;height:22pt;visibility:visible' o:gfxdata="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
9alfvNnqPycR2rFiAgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQIECBAgAAB
AgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQIECBAgAABAgQI
ECBAgACBXgn8H/bj3ytWsRE+AAAAAElFTkSuQmCCUEsDBAoAAAAAAAAAIQBny2zkpgMAAKYDAAAU
AAAAZHJzL21lZGlhL2ltYWdlMi5zdmc8c3ZnIHZpZXdCb3g9IjAgMCA5NiA5NiIgeG1sbnM9Imh0
dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcv
MTk5OS94bGluayIgaWQ9Ikljb25zX0Fycm93VXAiIG92ZXJmbG93PSJoaWRkZW4iPjxzdHlsZT4N
Ci5Nc2Z0T2ZjVGhtX0FjY2VudDZfRmlsbF92MiB7DQogZmlsbDojNzBBRDQ3OyANCn0NCjwvc3R5
bGU+DQo8cGF0aCBkPSJNNTEuMDMxIDg4Ljk1MSA1MS4wMzEgMTQuMTkyIDU5LjkzMSAyMy4wOTJD
NjEuMDkwOCAyNC4yNTE4IDYyLjk3MTIgMjQuMjUxOCA2NC4xMzEgMjMuMDkyIDY1LjI5MDggMjEu
OTMyMiA2NS4yOTA4IDIwLjA1MTggNjQuMTMxIDE4Ljg5Mkw1MC4xMzEgNC45QzQ5LjAyNjQgMy43
NDAyIDQ3LjE5MDggMy42OTU0MyA0Ni4wMzEgNC44IDQ1Ljk5NjkgNC44MzI1MiA0NS45NjM1IDQu
ODY1ODYgNDUuOTMxIDQuOUwzMS45NDEgMTguODlDMzAuNzgxMiAxOS45OTQ2IDMwLjczNjQgMjEu
ODMwMiAzMS44NDEgMjIuOTkgMzEuODczNSAyMy4wMjQxIDMxLjkwNjkgMjMuMDU3NSAzMS45NDEg
MjMuMDkgMzMuMDQ1NiAyNC4yNDk4IDM0Ljg4MTIgMjQuMjk0NiAzNi4wNDEgMjMuMTkgMzYuMDc1
MSAyMy4xNTc1IDM2LjEwODUgMjMuMTI0MSAzNi4xNDEgMjMuMDlMNDUuMDM2IDE0LjE5NSA0NS4w
MzYgODguOTUxQzQ1LjAzNiA5MC42MDc4IDQ2LjM3OTEgOTEuOTUxIDQ4LjAzNiA5MS45NTEgNDku
NjkyOSA5MS45NTEgNTEuMDM2IDkwLjYwNzggNTEuMDM2IDg4Ljk1MVoiIGNsYXNzPSJNc2Z0T2Zj
VGhtX0FjY2VudDZfRmlsbF92MiIgc3Ryb2tlPSJub25lIiBzdHJva2Utd2lkdGg9IjEiIHN0cm9r
ZS1saW5lY2FwPSJidXR0IiBzdHJva2UtbGluZWpvaW49Im1pdGVyIiBzdHJva2UtbWl0ZXJsaW1p
dD0iNCIgZmlsbD0iIzcwQUQ0NyIgZmlsbC1vcGFjaXR5PSIxIi8+PC9zdmc+UEsDBBQABgAIAAAA
IQA2eoK23wAAAAgBAAAPAAAAZHJzL2Rvd25yZXYueG1sTI9BS8NAEIXvgv9hGcGb3bUGadNsSqkE
PQhiq4K3bXaahGZnY3bbRn+9Yy/18obhMW/el80H14oD9qHxpOF2pEAgld42VGl4Wxc3ExAhGrKm
9YQavjHAPL+8yExq/ZFe8bCKleAQCqnRUMfYpVKGskZnwsh3SOxtfe9M5LWvpO3NkcNdK8dK3Utn
GuIPtelwWWO5W+2dhruXn3dVfEy2u/i4nhZf9PScfCZaX18NDzOWxQxExCGeL+CPgftDzsU2fk82
iFYD08STspeMpyA2PBMFMs/kf4D8FwAA//8DAFBLAwQUAAYACAAAACEAIlYO7scAAAClAQAAGQAA
AGRycy9fcmVscy9lMm9Eb2MueG1sLnJlbHO8kLFqAzEMhvdC3sFo7/nuhlJKfFlKIWtIH0DYOp/J
WTaWG5q3j2mWBgLdOkri//4PbXffcVVnKhISGxi6HhSxTS6wN/B5/Hh+BSUV2eGamAxcSGA3bZ62
B1qxtpAsIYtqFBYDS635TWuxC0WULmXidplTiVjbWLzOaE/oSY99/6LLbwZMd0y1dwbK3o2gjpfc
mv9mp3kOlt6T/YrE9UGFDrF1NyAWT9VAJBfwthw7OXvQjx2G/3EYusw/DvruudMVAAD//wMAUEsB
Ai0AFAAGAAgAAAAhAKjWx6gTAQAASQIAABMAAAAAAAAAAAAAAAAAAAAAAFtDb250ZW50X1R5cGVz
XS54bWxQSwECLQAUAAYACAAAACEAOP0h/9YAAACUAQAACwAAAAAAAAAAAAAAAABEAQAAX3JlbHMv
LnJlbHNQSwECLQAUAAYACAAAACEAzGqgidABAADYAwAADgAAAAAAAAAAAAAAAABDAgAAZHJzL2Uy
b0RvYy54bWxQSwECLQAKAAAAAAAAACEA2rsCM58YAACfGAAAFAAAAAAAAAAAAAAAAAA/BAAAZHJz
L21lZGlhL2ltYWdlMS5wbmdQSwECLQAKAAAAAAAAACEAZ8ts5KYDAACmAwAAFAAAAAAAAAAAAAAA
AAAQHQAAZHJzL21lZGlhL2ltYWdlMi5zdmdQSwECLQAUAAYACAAAACEANnqCtt8AAAAIAQAADwAA
AAAAAAAAAAAAAADoIAAAZHJzL2Rvd25yZXYueG1sUEsBAi0AFAAGAAgAAAAhACJWDu7HAAAApQEA
ABkAAAAAAAAAAAAAAAAA9CEAAGRycy9fcmVscy9lMm9Eb2MueG1sLnJlbHNQSwUGAAAAAAcABwC+
AQAA8iIAAAAA
">
   <v:imagedata src="Lab%205.fld/image007.png" o:title="" cropleft="-43691f"
    cropright="-46968f"/>
  </v:shape><![endif]--><![if !vml]><img width=21 height=22
  src="Lab%205.fld/image008.png" alt="Arrow Up with solid fill" v:shapes="Graphic_x0020_1"><![endif]></span><o:p></o:p></p>
  </td>
 </tr>
</table>

<p class=MsoNormal>This is why re-hashing a has table periodically to eliminate
tombstones is crucial for efficiency.</p>

</div>

</body>

</html>

