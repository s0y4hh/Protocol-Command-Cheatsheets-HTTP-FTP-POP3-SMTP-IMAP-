# Protocol Command Cheatsheets

This document provides a quick reference to common commands for several internet protocols: HTTP, FTP, POP3, SMTP, and IMAP.

## Table of Contents

* [HTTP Cheatsheet](#http-cheatsheet)
    * [Common HTTP Methods](#common-http-methods)
    * [Common HTTP Status Codes](#common-http-status-codes)
* [FTP Cheatsheet](#ftp-cheatsheet)
    * [Common FTP Commands](#common-ftp-commands)
* [POP3 Cheatsheet](#pop3-cheatsheet)
    * [Common POP3 Commands](#common-pop3-commands)
* [SMTP Cheatsheet](#smtp-cheatsheet)
    * [Common SMTP Commands](#common-smtp-commands)
* [IMAP Cheatsheet](#imap-cheatsheet)
    * [Common IMAP Commands](#common-imap-commands)

## HTTP Cheatsheet

HTTP (Hypertext Transfer Protocol) is used for communication between web browsers and servers.

### Common HTTP Methods

* **GET:** Retrieves data from a server.
* **POST:** Sends data to a server to create/update a resource.
* **PUT:** Sends data to a server to update a resource.  Idempotent.
* **DELETE:** Deletes a resource on a server.
* **PATCH:** Applies partial modifications to a resource.
* **HEAD:** Retrieves the headers of a resource without the body.
* **OPTIONS:** Describes the communication options for the target resource.
* **CONNECT:** Establishes a network connection to a server.
* **TRACE:** Performs a message loop-back test along the path to the target resource.

### Common HTTP Status Codes

* **1xx (Informational):** Request received, continuing process.
    * 100 Continue
    * 101 Switching Protocols
* **2xx (Success):** The action was successfully received, understood, and accepted.
    * 200 OK
    * 201 Created
    * 204 No Content
* **3xx (Redirection):** Further action needs to be taken in order to complete the request.
    * 301 Moved Permanently
    * 302 Found (Moved Temporarily)
    * 304 Not Modified
* **4xx (Client Error):** The request contains bad syntax or cannot be fulfilled.
    * 400 Bad Request
    * 401 Unauthorized
    * 403 Forbidden
    * 404 Not Found
* **5xx (Server Error):** The server failed to fulfill an apparently valid request.
    * 500 Internal Server Error
    * 502 Bad Gateway
    * 503 Service Unavailable

## FTP Cheatsheet

FTP (File Transfer Protocol) is used for transferring files between computers on a network.

### Common FTP Commands

* **USER:** Username to login.
* **PASS:** Password to login.
* **LIST (or LS):** Lists files in the current directory.
* **NLST:** Lists file names in the current directory.
* **CWD:** Changes the current directory.
* **PWD:** Prints the current directory.
* **RETR:** Retrieves (downloads) a file.
* **STOR:** Stores (uploads) a file.
* **APPE:** Appends a file to an existing file.
* **DELE:** Deletes a file.
* **MKD (or MD):** Creates a directory.
* **RMD (or RD):** Removes a directory.
* **RNFR:** Rename from.
* **RNTO:** Rename to.
* **ABOR:** Aborts the previous command.
* **QUIT (or BYE):** Terminates the FTP session.
* **PASV:** Enters passive mode.
* **PORT:** Specifies a port for the data connection.
* **TYPE:** Sets the transfer type (ASCII, Binary).
    * `TYPE A`: for ASCII mode
    * `TYPE I`: for Binary mode
* **HELP:** Displays help information.
* **NOOP:** Does nothing.  Used to keep the connection alive.

## POP3 Cheatsheet

POP3 (Post Office Protocol version 3) is used to retrieve email from a mail server.

### Common POP3 Commands

* **USER:** Username to login.
* **PASS:** Password to login.
* **STAT:** Gets mailbox status (number of messages, size).
* **LIST:** Lists messages and their sizes.
* **RETR:** Retrieves a message by number.
* **DELE:** Marks a message for deletion.
* **RSET:** Unmarks messages marked for deletion.
* **TOP:** Retrieves the headers and the first \*n\* lines of a message.
* **UIDL:** Lists message unique IDs.
* **QUIT:** Terminates the session and expunges (deletes) marked messages.
* **CAPA:** Lists the capabilities of the server.

## SMTP Cheatsheet

SMTP (Simple Mail Transfer Protocol) is used for sending email.

### Common SMTP Commands

* **HELO:** Introduces the client to the server (for the sender).
* **EHLO:** Extended HELO; introduces the client and requests extended features.
* **MAIL FROM:** Specifies the sender's email address.
* **RCPT TO:** Specifies the recipient's email address.
* **DATA:** Starts the email message data transmission.
* **VRFY:** Verifies that a mailbox exists (less common due to security).
* **EXPN:** Expands a mailing list (less common due to security).
* **HELP:** Displays help information.
* **NOOP:** Does nothing.  Used to keep the connection alive.
* **RSET:** Resets the current transaction.
* **QUIT:** Terminates the session.

## IMAP Cheatsheet

IMAP (Internet Message Access Protocol) is used to retrieve and manage email messages on a mail server.  It allows you to work with emails without downloading them.

### Common IMAP Commands

* **CAPABILITY:** Requests the capabilities of the server.
* **LOGIN:** Authenticates the client.
* **LOGOUT:** Closes the connection.
* **SELECT:** Selects a mailbox (e.g., INBOX).
* **EXAMINE:** Selects a mailbox in read-only mode.
* **CREATE:** Creates a new mailbox.
* **DELETE:** Deletes a mailbox.
* **RENAME:** Renames a mailbox.
* **SUBSCRIBE:** Adds a mailbox name to the active subscription list.
* **UNSUBSCRIBE:** Removes a mailbox name from the active subscription list.
* **LIST:** Returns the mailbox names that match the reference name argument.
* **LSUB:** Returns the subscribed mailbox names that match the reference name argument.
* **STATUS:** Requests the status of the mailbox.
* **APPEND:** Appends a message to the specified mailbox.
* **CHECK:** Performs a mailbox check.
* **CLOSE:** Closes the currently selected mailbox.
* **EXPUNGE:** Permanently removes all messages that are marked for deletion.
* **SEARCH:** Searches the mailbox for messages that match the given searching criteria.
* **FETCH:** Retrieves message data.
* **STORE:** Stores message data.
* **COPY:** Copies the specified message(s) to the specified destination mailbox.
* **MOVE:** Moves the specified message(s) to the specified destination mailbox.
* **UID:** Prefix for commands that operate on message UIDs rather than sequence numbers (e.g., UID FETCH).
