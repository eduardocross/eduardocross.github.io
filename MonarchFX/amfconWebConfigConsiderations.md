---
title: Web.Config Considerations

Id: amfconWebConfigConsiderations
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 100

keywords: web.config, considerations
keywords: considerations for web.config
keywords: ASNA.Monarch, web.config considerations
keywords: concepts, ASNA.Monarch, Web.Config
keywords: ASNA.Monarch, configuration files
keywords: appsettings.config, considerations
keywords: considerations, web.config
keywords: considerations, appsettings.config
keywords: concepts, ASNA.Monarch appSettings.Config
keywords: concepts, ASNA.Monarch DDS configuration files
keywords: concepts, ASNA.Monarch applying text values to DDS buttons
keywords: applying text values to DDS buttons
keywords: function keys, concepts
keywords: function keys, about
keywords: function keys, displaying text
keywords: function keys, using configuration files
keywords: attention keys, concepts
keywords: attention keys, about
keywords: attention keys, displaying text
keywords: attention keys, using configuration files
keywords: aid keys, concepts
keywords: aid keys, about
keywords: aid keys, displaying text
keywords: aid keys, using configuration files
keywords: configuration files, using for DDS button values
keywords: web.config
keywords: web.config, processing rules
keywords: web.config, example of
keywords: web.config, modifying
keywords: appsettings.config, example of
keywords: appsettings.config, modifying
keywords: appsettings.config, processing rules
keywords: processing rules of web.config
keywords: OS400 concepts, displaying DDS button values

---

As part of the Monarch Framework, there are two configuration files that enable applying text values to the DDS button labels on a global basis. Although [DdsFile](amfDdsFilClass.html) provides some properties for setting these values at design time, the **Web.config** file and the **AppSettings.config** file provide a method to establish these values definitively.

The display text for function keys can be provided in two separate places: the **Web.config** file and the [ FuncKeys](amfDdsFileClassFuncKeysProperty.html) property on DdsFile. Note that even if the key is not enabled (no <code> **Response:Option Indicator** </code> is provided), the Text entered will be used as the default label for that Display file. This label takes precedence over whatever is found in **Web.config** .

Each record format also provides <code> **FuncKeys** </code> and <code>[ AttnKeys](amfDdsFileClassAttnKeysProperty.html)</code> properties where text can be entered for individual keys. Their property values text is only used if the record format enables that key. There is no real mechanism to provide text for "enter" and "reset" because these keys cannot be "enabled" by a record format (or file). The <code>[ EnterText](amfDdsFileClassEnterTextProperty.html)</code> and <code>[ ResetText](amfDdsFileClassResetTextProperty.html)</code> properties have been provided to allow text values to be established for these two keys. In addition, the <code>[ CssEnterClass](amfDdsFileClassCssEnterClassProperty.html)</code> property can be used to contain the name of the cascading style sheet class that controls the appearance of these keys. You can also set the <code>[ BannerStyle](amfDdsFileClassBannerStyleProperty.html)</code> property to <code> **Hidden** </code> to hide all functions keys **except** "enter" and "reset". 

Under all conditions, if the property is set, the value entered will be used. If not, the **Web.Config** file is checked and any value found for the button will be used; otherwise English labels will be used.

#### Processing Rules
During internal migration and within Visual Studio, the following rules apply:

- The 
 **Web.config**  file contains a <code>"file="</code>
        attribute on the 
        <code> **appSettings** </code> section that is a relative path
        (migrated to the same folder as 
 **Web.config** ).
- If the Migrator removes **AppSettings.config**  provided as
        a template, then Cocoon does not insert the <code>"file="</code>
        attribute on the 
 **appSettings**  section of 
 **Web.config** .
- The setting for 
        <code> **key="MonarchMessageFileFolder"** </code> (generated
        by Monarch if the Website uses at least one Message file), is
        added to the 
 **appSettings**  section directly into 
 **Web.config** (as opposed to the external file

 **AppSettings.config** ). **Note:**  The value for 
        <code> **"MonarchMessageFileFolder"** </code>
          allows the use of the symbol "<code>~</code>", as
          in <code><span style="background: #ffffcc">
        value="~\Monarch MsgFiles\"</span></code> to specify the website "root" and make this a
          relative reference instead of an absolute path
          location.
- When the Website runs, any settings in 
 **Web.config**  are merged with the settings defined in
 **AppSettings.config** .
- If there are duplicate keys (i.e. in 
 **Web.config**  and
 **AppSettings.config** ), the Website will
        throw an exception during startup and will not run until
        fixed.
- If 
 **Web.config**  is modified while the Website
        runs, the Website is re-started automatically.
- If 
 **AppSettings.config**  is modified while the
        Website runs, the Website does not automatically restart; changes in the settings take effect 
 ** *after* **  the Website is re-started by any means.

#### Web.config File
A partial sample of a Web.config File is provided below as it pertains to this topic:
<pre class="example">
   &lt;configuration&gt;
       &lt;configSections&gt;
           . . .
       &lt;/configSections&gt;
       &lt;appSettings **<span style="COLOR: red"> file="AppSettings.config"</span>** &gt;
            &lt;add key="MonarchMessageFileFolder" value="~\Monarch MsgFiles\" /&gt;
       &lt;/appSettings&gt;   
       &lt;MonarchFileOverrides&gt;
            . . .   
      &lt;/MonarchFileOverrides&gt;
      &lt;system.web&gt;
           &lt;compilation debug="true" &gt;
                &lt;assemblies&gt;
                  . . .                     
               &lt;/assemblies&gt; 
          &lt;/compilation&gt;
        &lt;/system.web&gt;
   &lt;/configuration&gt;</pre>

#### appSettings.config File
A sample of an appSettings.config File is provided below containing **only** the basic instructions to establish the key values and general guidelines to assess the values settings within your code. This file is provided as a template at **$InstalDir\Templates\AspWebApp** .
<pre class="example">&lt;
&lt;appSettings&gt;
    !-- DISPLAY FILE CUSTOMIZATION.
        To change the text to be displayed for function keys and other DdsRecord buttons,
        add entries using the following format: 
          &lt;add key="KEYNAME" value="KEYTEXT"/&gt;
        where KEYNAME has the format: MonarchKeyXXXXX (case sensitive)
          and XXXX is F1...F24, Clear, Enter, Help, PageUp, PageDown, Print, or Reset.
      Examples:      
       &lt;add key="MonarchKeyF1"  value="PF1"/&gt;
        ...
       &lt;add key="MonarchKeyF24"      value="PF24"/&gt;
       &lt;add key="MonarchKeyClear"    value="CLR"/&gt;
       &lt;add key="MonarchKeyEnter"    value="Submit"/&gt;
       &lt;add key="MonarchKeyHelp"     value=" ? "/&gt;
       &lt;add key="MonarchKeyPageUp"   value="Roll Down"/&gt;
       &lt;add key="MonarchKeyPageDown" value="Roll Up"/&gt;
       &lt;add key="MonarchKeyPrint"    value="PRT"/&gt;
       &lt;add key="MonarchKeyReset"    value="RST"/&gt; 
   --&gt;
   &lt;!--  YOUR APPLICATIONSETTINGS GO HERE. Note: the key name is case-sensitive.
       &lt;add key="MySetting" value="The value of MySetting" /&gt; 
 &lt;/appSettings&gt;</pre>

In your code, you can retrieve the setting using the following system class. 
<pre class="example">DclFld appSettings Type(System.Configuration.AppSettingsReader)        
DclFld mySetting Type(*String)
 // Instantiate application settings reader class (do it only once in your application)                
   appSettings = *new System.Configuration.AppSettingsReader()  
 // Using the applications settings reader object, get the value of the key configured.
   mySetting = appSettings.GetValue( "MySetting" , *TypeOf(*String)) *As *String </pre>

#### Next: [Adding Web.Config Manually](amfconWebConfigMissingInstructions.html)

#### Previous: [Display File Overview](amfconDisplayFiles.html)

#### See Also
<dl>
        <dd>[DdsFile Class](amfDdsFileClass.html)</dd>
       <dd>[AttnKeys Property](amfDdsFileClassAttnKeysProperty.html)</dd>
      <dd>[FuncKeys Property](amfDdsFileClassFuncKeysProperty.html)</dd>
      <dd>[Overview of Aid Keys](amfconOverviewofAidKeys.html)</dd>
      <dd>[Instructions to Add Web.config Manually](amfconWebConfigMissingInstructions.html)</dd>
</dl>

