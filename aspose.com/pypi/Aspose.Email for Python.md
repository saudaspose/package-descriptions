# Python Email API

Aspose.Email for Python via .NET is a suite of flexible and easy to use class libraries brought together to produce the most powerful Email Programming Component available today. The Python Email API implements a number of network protocols including SMTP, MIME, POP3, IMAP for creating, sending & receiving messages without needing to have any other component. It can also manipulate, extract & convert message files & message archives.

Aspose.Email for Python via .NET also provides classes and algorithms that are useful for time-oriented recurrence patterns, or schedules. The central concepts are coherent with the iCalendar RFC (2445), so it is easy to incorporate iCalendar features into your own python applications.

## Email Features

- Open or save emails in a variety of formats.
- Parse, read and save Microsoft Outlook messages and message archives.
- Comprehensive Object Model for MIME messages.
- Embed objects to email messages.
- Send individual or bulk emails.
- Create emails using Mail Merge while incorporating data from different types of sources.
- Crease & consume iCalendar compliant recurrence patterns.
- [Connect to POP3 server for message management](https://docs.aspose.com/display/emailpythonnet/Connect+to+POP3+Server).
- [Access and manage emails, folders & filters using IMAP](https://docs.aspose.com/display/emailpythonnet/Connecting+to+IMAP+Server).
- [Send or forward messages via SMTP](https://docs.aspose.com/display/emailpythonnet/Sending+and+Forwarding+Messages).
- Verify email addresses, processing bounced messages, analyze spam via Bayesian & more.


## Read & Write Email Formats

**Microsoft Outlook:** MSG, PST, OST, OFT
**Email:** EML, EMLX, MBOX
**Others:** ICS, HTML, MHTML

## Getting Started with Aspose.Email for Python via .NET

Are you ready to give Aspose.Email for Python via .NET a try? Simply execute `pip install Aspose.Email-for-Python-via-NET` to get the latest version & try any of the following code snippets. You may also check the detailed [Developer's Guide](https://docs.aspose.com/display/emailpythonnet/Developer+Guide) for all possible usage scenarios.

## Inspect PST Structure & Items via Python

```python
personalStorage = PersonalStorage.from_file(dataDir + "template.pst")
folderInfoCollection = personalStorage.root_folder.get_sub_folders()
for folderInfo in folderInfoCollection:
	print("Folder: " + folderInfo.display_name)
	print("Total Items: " + str(folderInfo.content_count))
	print("Total Unread Items: " + str(folderInfo.content_unread_count))
	print("----------------------")
```

## Send Bulk Emails via SMTP using Python

```python
message1 = MailMessage("from@gmail.com", "to@gmail.com", "Sending Bulk Emails using Aspose.Email", "message1, how are you?")
message2 = MailMessage("from@gmail.com", "to@gmail.com", "Sending Bulk Emails using Aspose.Email", "message2, how are you?")
message3 = MailMessage("from@gmail.com", "to@gmail.com", "Sending Bulk Emails using Aspose.Email", "message3, how are you?")

manyMsg =  MailMessageCollection()
manyMsg.append(message1)
manyMsg.append(message2)
manyMsg.append(message3)

#Send using Smtp Client
client = SmtpClient("smtp.gmail.com", 995, "username", "password")
client.security_options = SecurityOptions.AUTO

client.send(manyMsg)
```

## Read Messages from Thunderbird's MBOX

```python
reader = MboxrdStorageReader(dataDir + "ExampleMbox.mbox", False)

eml = reader.read_next_message()
while (eml is not None):
    print("Subject: " + eml.subject)
    # save this message in EML or MSG format
    eml.save(eml.subject + "_out.eml", aspose.email.SaveOptions.default_eml)
    eml.save(eml.subject + "_out.msg", aspose.email.SaveOptions.default_msg_unicode)

    eml = reader.read_next_message();

reader.dispose();
```

[Product Page](https://products.aspose.com/email/python-net) | [Docs](https://docs.aspose.com/display/emailpythonnet/Home) | [API Reference](https://apireference.aspose.com/net/email) | [Examples](https://github.com/aspose-email/aspose-email-python-dotnet) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) | [Temporary License](https://purchase.aspose.com/temporary-license)
