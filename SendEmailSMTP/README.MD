---
page_type: sample
languages:
- csharp
products:
- azure
- azure-communication-services
---

# Email Sample

This sample sends an email to the selected recipients of any domain using an [Email Communication Services resource](https://docs.microsoft.com/azure/communication-services/quickstarts/email/create-email-communication-resource) with SMTP.

Additional documentation for this sample can be found on [Microsoft Docs](https://learn.microsoft.com/en-us/azure/communication-services/quickstarts/email/send-email-smtp/send-email-smtp?pivots=smtp-method-smtpclient).

## Prerequisites

- Create an Azure account with an active subscription. For details, see [Create an account for free](https://azure.microsoft.com/free/).
- [Visual Studio (2019 and above)](https://visualstudio.microsoft.com/vs/).
- [.NET 6.0](https://dotnet.microsoft.com/download/dotnet/6.0) (Make sure to install version that corresponds with your Visual Studio instance, 32 vs 64 bit).
- Create an Azure Communication Services resource. For details, see [Create an Azure Communication Resource](https://docs.microsoft.com/azure/communication-services/quickstarts/create-communication-resource).
- Create an [Azure Email Communication Services resource](https://docs.microsoft.com/azure/communication-services/quickstarts/email/create-email-communication-resource) to start sending emails.

> Note: We can send an email from our own verified domain also [Add custom verified domains to Email Communication Service](https://docs.microsoft.com/azure/communication-services/quickstarts/email/add-custom-verified-domains).

## Code structure

- ./SendEmailSMTP/SendEmailSMTP/Program.cs: Entry point for sending email.

## Before running the sample for the first time

1. Open an instance of PowerShell, Windows Terminal, Command Prompt or equivalent program and navigate to the directory that you'd like to clone the sample to.
2. `git clone https://github.com/Azure-Samples/communication-services-dotnet-quickstarts.git`

### Locally configuring the application

1. Navigate to the SendEmailSMTP folder and open the `SendEmailSMTP.sln` solution in Visual Studio.
2. Open the program.cs file to configure the following settings:

- ` smtpAuthUsername`: Replace `<Azure Communication Services Resource name>|<Entra Application Id>|<Entra Application Tenant Id>` as mentioned. For more details please refer:[Microsoft Docs](https://learn.microsoft.com/en-us/azure/communication-services/quickstarts/email/send-email-smtp/smtp-authentication).
- ` smtpAuthPassword`: Replace `<Entra Application Client Secret>` which is your Microsoft Entra Application Secret. 
- `sender`: Replace `<SENDER_EMAIL>` with the sender email obtained from Azure Communication Service.
- `recipient`: Replace `<RECIPIENT_EMAIL>` with the recipient email.
- The body and message can be added as per your wish. The parameters such as hostname, port, should be kept intact. 

1. Run `SendEmail` project.
