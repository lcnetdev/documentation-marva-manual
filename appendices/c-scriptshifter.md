# Appendix C: ScriptShifter

## About ScriptShifter

ScriptShifter is an open source tool that is used in Marva to romanize non-Latin script according to the ALA/LC Romanization Tables, and to generate non-Latin scripts from data romanized according to the ALA/LC Romanization Tables.

ScriptShifter uses AI and user input to improve its responsiveness. Anyone working with ScriptShifter in Marva is welcome to provide feedback to the developers on ScriptShifter.

## Setting ScriptShifter Scripts and Script Options

Access ScriptShifter under Preferences in the Navigation Bar in Marva.

![Preferences menu with ScriptShifter highlighted, along with Diacritic Macros and Text Macros](../images/page121_img01.png)

In the pop-up box, you will see multiple options for selecting Scripts and Actions.

![ScriptShifter configuration panel showing language list with Script to Roman and Roman to Script checkboxes](../images/page121_img02.png)

Visit [bibframe.org/scriptshifter](https://bibframe.org/scriptshifter) to test these languages.

**Capitalize first letter of transliteration** is "off" by default. If the script and language you are working with uses capitalization, you can click on this box so ScriptShifter will capitalize the first letter of the text that is generated.

In the Name, Script to Roman, and Roman to Script columns, you can select the languages and scripts that you will be working with in Marva from the A-Z list.

For most languages and scripts, ScriptShifter offers both transliteration from non-Latin script to romanized script, and the generation of non-Latin script from romanized script. Check the appropriate boxes. There is no limit on the number of boxes you can check.

For some languages and scripts, ScriptShifter does not offer both transliteration from non-Latin script to romanized script, and the generation of non-Latin script from romanized script. For these scripts, one of the boxes will be greyed-out, meaning that the option is not available in ScriptShifter. For example, ScriptShifter does not have an option to generate Korean script from romanized Korean script, and ScriptShifter does not have an option to romanize Kurdish script.

![Korean and Kurdish script options showing greyed-out unavailable conversion directions](../images/page122_img01.png)

## Using ScriptShifter in Marva

### Script to Roman

Set the value in ScriptShifter. Click the Esc button to exit the ScriptShifter panel.

![Russian language with Script to Roman and Roman to Script both checked](../images/page122_img02.png)

In Marva, the options that you selected in the ScriptShifter panel will be visible in the Lightning Bolt feature for each literal component.

![Lightning Bolt menu showing Russian S2R and Russian R2S options](../images/page123_img01.png)

In a Literal field, key in or paste Russian script. If you are using the MARC Preview Panel, you will see that the Russian title in Cyrillic script shows up in the MARC 245 field.

![Title information field with Russian Cyrillic text and MARC preview showing 245 field](../images/page123_img02.png)

Click on the Lightning Bolt and select the **Russian S2R** option.

![Lightning Bolt menu with Russian S2R highlighted](../images/page124_img01.png)

The romanized title will be added to a second Preferred title for Work in the Marva Title information component, and the values in the MARC Preview will reflect current cataloging policy, with the romanized title in the 245 field, and the Russian Cyrillic script title in the corresponding 880 field. The non-Latin title and the romanized title will be connected with a bracket in Marva.

![Title information showing both Cyrillic and romanized titles with language tags, and MARC preview showing 245 and 880 fields](../images/page124_img02.png)

### Roman to Script

Set the value in ScriptShifter. Click the Esc button to exit the ScriptShifter panel.

![Russian language with both Script to Roman and Roman to Script checked, arrow pointing to Roman to Script](../images/page124_img03.png)

In Marva, the options that you selected in the ScriptShifter panel will be visible in the Lightning Bolt feature for each literal component.

![Lightning Bolt menu showing Russian R2S option highlighted](../images/page123_img01.png)

In a Literal field, key in or paste romanized Russian script. If you are using the MARC Preview Panel, you will see that the romanized Russian title shows up in the MARC 245 field.

![Title information with romanized Russian text and MARC preview](../images/page125_img02.png)

Click on the Lightning Bolt and select the **Russian R2S** option.

![Lightning Bolt menu with Russian R2S highlighted](../images/page125_img03.png)

The Russian script title will be added to a second Preferred title for Work in the Marva Title information component, and the values in the MARC Preview will reflect current cataloging policy, with the romanized title in the 245 field, and the Russian Cyrillic script title in the corresponding 880 field. The non-Latin title and the romanized title will be connected with a bracket in Marva.

![Title information showing both romanized and Cyrillic titles with MARC preview](../images/page126_img01.png)

## Language and Script Tags

### Component Level

When ScriptShifter is used in Marva, language and script tags are added by default to both romanized text and text in Non-Latin script.

![Title information showing romanized title tagged ru-Latn and Cyrillic title tagged ru-Cyrl, with MARC preview showing 245 and 880 fields](../images/page126_img02.png)

These values can be changed if needed by clicking on the Lightning Bolt and selecting Set Language.

![Lightning Bolt menu showing Set Language option along with Russian S2R and Russian R2S](../images/page126_img03.png)

Under each literal value, there will be a Language tag and a Script tag. Use the dropdown lists under Language and Script to change the values.

![Language and Script tag editing interface showing Script dropdown with various script options, and Language dropdown with language options](../images/page127_img01.png)

![Set Language interface showing Russian/Latin for romanized text and Russian/Cyrillic for non-Latin text with Done button](../images/page127_img02.png)
![Set Language interface showing Russian/Latin for romanized text and Russian/Cyrillic for non-Latin text with Done button](../images/page127_img03.png)


### Global Level

You can select Language and Script tags for all literal values in a description by clicking on Tools --> Non-Latin Literals in the Navigation Bar.

![Tools menu showing Non-Latin Literals option highlighted](../images/page125_img01.png)

This will open a box that will show all non-Latin Literal values in the description and you can manage all of them in one screen.

![Non-Latin literals management dialog showing all non-Latin literal values with Set individually options and Add Language Option](../images/page125_img02.png)

## Non-Latin Agents

![Tools menu showing Non-Latin Agents option highlighted](../images/page125_img03.png)

Non-Latin Agents (Tools --> Non-Latin Agents) allows you to manage access points in Non-Latin scripts. This feature works with non-Latin variant access points in authority records.

When a name authority has multiple Non-Latin authorized labels. For example: [n2010057779](http://id.loc.gov/authorities/names/n2010057779):

![Name authority record showing Hyon, Mu-am, 1969- with Chinese characters and Korean script variants](../images/page126_img01.png)

(id.loc.gov is "selecting" a Non-Latin variant label to be the "authorized" label for that script)

When added to Marva the editor will try to select which Non-Latin authorized label to use to build an 880 field. It does this by looking at the language tags set for the literals in the record. It selects the most common one and then chooses that language + script combination to build the 880. This works fine if there is only one Non-Latin authorized label to select. But if there are multiple it could potentially select the incorrect one to use. This modal window allows you to overwrite that logic and force Marva to use a specific script to build the 880. After I added this name authority, and a Non-Latin title, and went to Tools -> Non-Latin Agents I see this:

![Non-Latin Agents dialog showing script selection with Hani selected for bf:contribution access point](../images/page126_img02.png)

For this name it has selected the Hani script to build the 880. I can force it however to use the Hang script instead:

![Non-Latin Agents dialog showing dropdown to change from Hani to Hang script](../images/page126_img03.png)

This will force the conversion to use the Hang script label when building the 880 in the MARC output. To summarize you will likely never need to modify these selections as Marva should pick the best fit. But if it doesn't this is how you can overwrite it.

---

[Back to Table of Contents](../index.md)
