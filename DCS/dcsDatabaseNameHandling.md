---
title: Database Name Handling

Id: dcsDatabaseNameHandling
TocParent: dcsConnectingtoaDatabaseMain
TocOrder: 1

keywords: database names
keywords: database names, handling
keywords: database files, handling database names
keywords: handling database names
keywords: managing database connections, database name handling

---

DCS for Visual Studio 2019 is adept at handling the standard "database name" conventions familiar to AVR programmers and users of tools such as DataGate Database Manager. A database name is simply a shorthand notation, redirecting the client-side engine to a set of client/server database connection parameters stored in the system registry. These registry entries can be accessed and manipulated with the [ SourceProfile](dcsSourceProfileClass.html) object. **SourceProfile** provides the programmer with some of the functionality of DataGate Database Manager’s "Work with Database Names" option. The object constructor and methods [ Register](dcsSourceProfileClassRegisterMethod.html) and [Unregister](dcsSourceProfileClassUnregisterMethod.html) are used to retrieve, persist, and delete respectively, database name registry entries.

The following example retrieves a database name called "Asna 400 db" (in the process of constructing the SourceProfile object), changes the user and password, and then saves the changes by calling Register. 
<pre>
        <span class="lang">
 **[C#]** 
        </span>
  using ASNA.DataGate.Providers;
  SourceProfile AsnaDbName;
  AsnaDbName = new SourceProfile("Asna 400 db");
  AsnaDbName.User = "NewUser";
  AsnaDbName.Password = "NewPasswd";
  AsnaDbName.Register()</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Imports ASNA.DataGate.Providers
  Dim AsnaDbName As SourceProfile
  AsnaDbName = New SourceProfile("Asna 400 db")
  AsnaDbName.User = "NewUser"
  AsnaDbName.Password	= "NewPasswd"
  AsnaDbName.Register()</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
  Using ASNA.DataGate.Providers
  Dclfld Name(AsnaDbName) Type(SourceProfile
  AsnaDbName = *New ("Asna 400 db")
  AsnaDbName.User = "NewUser" 
  AsnaDbName.Password = "NewPasswd" 
  AsnaDbName.Register()
			</pre>

To discover the currently registered database names available for use in a program, use the [SourceProfile.GetNames](dcsSourceProfileClassGetNamesMethod.html) static method. This method returns an array of strings as shown in the following example. This snippet of AVR code will print "*PUBLIC" and "User" database names registered on the machine where the code runs. 
<pre>
        <span class="lang">
 **[C#]** 
        </span>
     Console.WriteLine( "*Public Database Names:" );
  Foreach Name(DbName) Collection([SourceProfile.GetNames](dcsSourceProfileClassGetNamesMethod.html)(*True)) 
				Type(*String);
     Console.WriteLine( "  *Public\" + DbName );
  Endfor;
     Console.WriteLine( "User Database Names:" );
  Foreach Name(DbName) Collection(SourceProfile.GetNames(*False)) 
				Type(*String);
  Console.WriteLine( "  " + DbName );
  Endfor;</pre>
      <pre>
        <span class="lang">
 **[Visual Basic]** 
        </span>
  Console.WriteLine( "*Public Database Names:" )
  For each Name(DbName) Collection([SourceProfile.GetNames](dcsSourceProfileClassGetNamesMethod.html)(*True)) 
				Type(*String)
     Console.WriteLine( "  *Public\" + DbName )
  End for
     Console.WriteLine( "User Database Names:" )
  For each Name(DbName) Collection(SourceProfile.GetNames(*False)) 
				Type(*String)
  Console.WriteLine( "  " + DbName )
  End for</pre>
      <pre class="prettyprint">
        <span class="lang">
 **[Visual RPG]** 
        </span>
     Console.WriteLine( "*Public Database Names:" )
  Foreach Name(DbName) Collection([SourceProfile.GetNames](dcsSourceProfileClassGetNamesMethod.html)(*True)) 
				Type(*String)
     Console.WriteLine( "  *Public\" + DbName )
  Endfor
     Console.WriteLine( "User Database Names:" )
  Foreach Name(DbName) Collection(SourceProfile.GetNames(*False)) Type(*String)</pre>

Console.WriteLine( " " + DbName ) Endfor <p> **SourceProfile** objects may be assigned to the [ AdgConnection.SourceProfile](dcsAdgConnectionClassSourceProfileProperty.html) property to force a subsequent call to [ AdgConnection.Open](dcsAdgConnectionClassOpenMethod.html) to use the SourceProfile’s connection parameters. Changing **AdgConnection.SourceProfile** has no effect on the database connection of an **AdgConnection** object in the *Open* state. Rather, **AdgConnection.SourceProfile** is used by the **AdgConnection.Open** method to initialize the database connection. 
See Also

<dl />[Database Name Handling](dcsDatabaseNameHandling.html)<br />[AdgConnection Class](dcsAdgConnectionClass.html)<br />[AdgConnection.Open Method](dcsAdgConnectionClassOpenMethod.html)<br />[AdgConnection.SourceProfile 
					Property](dcsAdgConnectionClassSourceProfileProperty.html)<br />[AdgConnection.State Property](dcsAdgConnectionClassStateProperty.html)<br />[SourceProfile Class](dcsSourceProfileClass.html)<br />[SourceProfile.Register 
					Method](dcsSourceProfileClassRegisterMethod.html)<br />[SourceProfile.GetNames 
					Method](dcsSourceProfileClassGetNamesMethod.html)<br />[SourceProfile.Unregister 
					Method](dcsSourceProfileClassUnregisterMethod.html)

