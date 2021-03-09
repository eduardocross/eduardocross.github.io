---
title: Message Files

Id: amfMessageFiles
TocParent: amfASNAMonarchFrameworkConceptsMain
TocOrder: 190

keywords: message files, about
keywords: concepts, ASNA Monarch Framework, message files
keywords: ASNA Monarch, message files
keywords: ASNA Monarch, program support facilities
keywords: message files, concepts
keywords: message files, managing
keywords: message files, XML file components, msgid
keywords: message files, XML file components, severity
keywords: message files, XML file components, text
keywords: message files, XML file components, seclvl
keywords: message files, XML file components, datacount
keywords: message files, XML file components, placeholder number
keywords: XML files, stores Monarch message files
keywords: OS400 concepts, message queues
keywords: OS400 concepts, message files

---

#### About Message Files
A message is a communication sent from one user, program, or procedure to another. Most data processing systems provide communications between the system and the operator to handle errors and other conditions that occur during processing. There are two types of messages: Immediate messages and Predefined messages.

Immediate messages are created by the program or system user when they are sent and are not permanently stored in the system. Predefined messages are created before they are used. These messages are placed in a message file when they are created and retrieved from it when they are used.

The following concepts of message handling are important to application development:

1. Messages can be defined in messages files, which are
        outside the programs that use them, and variable
        information can be provided in the message text when a
        message is sent. Because messages are defined outside the
        programs, the programs do not have to be changed when the
        messages are changed.
2. Messages are sent to and received from message queues,
        which are separate objects on the system. A message sent to
        a queue can remain on the queue until it is explicitly
        received by a program or workstation user.
3. A program can send messages to a user who requested the
        program regardless of which workstation that user has signed
        on to. Messages do not have to be sent to a specific
        device.  One program can be used from different work
        stations without change.

A message description defines a message. The message description contains the text of the message and information about replacement variables, and can include variable data that is provided by the message sender when the message is sent. Each description must have an identifier that is unique within the file. When a message is sent, the message file and the message identifier tell the system which message description is to be used.

When a message is sent to a procedure, a program, or a system user, it is placed on a message queue associated with that procedure, program, or user. The procedure, program, or user sees the message by receiving it from the queue. There are message queues for each workstation on the system, each user enrolled on the system, the system operator, and the system history log. Messages sent to message queues are kept, so the receiver of the message does not need to process the message immediately.

#### Monarch Message Files
Under Monarch, messages are used mostly to communicate to the user. The main purpose is to define, in a single place, the text and optional replacement value placeholders. Messages are defined in message files. Currently, Monarch only provides one implementation of message files in the form of XML files.

Each message has 6 components:

- MSGID &#8211; a unique identifier for the message.
- SEVERITY &#8211; optionally the severity level of the message
        as appropriate.
- TEXT &#8211; defines the text to be displayed to the user.
        May contain up to 9 placeholders in the form '&amp;x' where
        x is a number between 1 and 9.
- SECLVL &#8211; contains the second level of message text. May
        also contain placeholders as noted above.
- DATACOUNT &#8211; contains the number of placeholders.
- Placeholder Data Definitions &#8211; TYPEx, LENx, and DECx
        where x represents the placeholder number. A placeholder
        data definition is needed for each placeholder defined in
        TEXT and SECLVL.

Here is an example of a message to notify the user that a customer has been added. One placeholder is included for the customer number.
<pre class="syntax">&lt;MSG MSGID="CUST0001" SEVERITY="0" DATACOUNT="1" TEXT="Customer &amp;1 has been added"
      SECLVL= "" TYPE1="*CHAR" LEN1="9" DEC1="0"&gt;</pre>

Here is another example of a message to notify the user that a library was not available. Three placeholders are included for the *library* (&amp;1), *reason* (&amp;2), and *program* (&amp;3) executing when the error occurred.
<pre class="syntax">
&lt;MSG MSGID="CUST0002" SEVERITY="20" DATACOUNT="3" TEXT="Library &amp;1 is not available." 
SECLVL="The system returned an error &amp;2 when trying to execute &amp;3 on library &amp;1."
<br />TYPE1="*CHAR" LEN1="10" DEC1="0" TYPE2="*CHAR"
LEN2="7" DEC2="0" TYPE3="*CHAR" LEN3="20" DEC3="0"&gt;</pre>

#### Monarch Program Support
ASNA Monarch provides the following facilities to manage messages. There are also numerous methods, properties, and fields that deal with creating and maintaining messages in the controls.

- [
        MessageTypes](amfMessageTypesEnumeration.html) enumeration to define the type of message
        (informational, inquiry, request, etc.).
- [Message
        Constructors](amfMessageClassMessageConstructors.html) to add messages to the message file: 
        <ul><li> **Message** (string 
 *text* , MessageTypes 
 *type* )
- **Message** (string 
 *id* , string 
 *data* , string 
 *file* , MessageTypes 
 *type)*

</li>
        <li>
          [
        MessageFormatter.FormatMessage](amfMessageFormatterClassFormatMessageMethod.html) to format a message
        (convert to string). 
- string 
 **FormatMessage** (string 
 *msgFilePath* , Message 
 *message* )

</li>
        <li>
          [
        Program](amfProgramClassMembers.html) class methods (refer to the members pages for a
        list) 
- void 
 **RemoveMessage** (string 
 *messageKey* )
- void 
 **RemoveMessage** (string 
 *pgmQ*  string 
 *messageKey* )
- string 
 **SendExternalMessage** (string 
 *id* , string 
 *file* , string 
 *data* , MessageTypes 
 *type* )
- string 
 **SendProgramMessage** (string 
 *text* )
- string 
 **SendProgramMessage** (string 
 *id* , string 
 *file* , string 
 *data* )
- string 
 **SendProgramMessage** (string 
 *text* , string 
 *pgmQ* , MessageTypes 
 *type* )
- string 
 **SendProgramMessage** (string 
 *id* , string 
 *file* , string 
 *data,*  string 
 *pgmQ* )
- string 
 **SendProgramMessage** (string 
 *id* , string 
 *file* , string 
 *data* , MessageTypes 
 *type* )

</li>
      </ul>

**Note** When the substitution variable can be a variable length, the length of the variable must be included in any *data* parameters when constructing or sending messages i.e. "{23}Invalid employee number". 

#### Next: [SQL Migration Overview and Examples](amfconSQLStatementExamples.html)

#### Previous: [Moving Data between Workstation File and Display File](amfconFrameworkASPXSessionMovingData.html)

#### See Also
<dl>
        <dd>[What's New](amfWhatsNewin72.html)</dd>
       <dd>[Reference
        Library](amfReferenceMain.html)</dd>
       <dd>[
        MessageTypes Enumeration](amfMessageTypesEnumeration.html)</dd>
       <dd>[Program
        Class Members](amfProgramClassMembers.html)</dd>
</dl>

