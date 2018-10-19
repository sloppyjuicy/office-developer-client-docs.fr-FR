---
title: Envoi d’un e-mail d’après l’adresse SMTP d’un compte
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01eef87c70e27425182b8a2f9f849c9736d43a31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406392"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a><span data-ttu-id="ccdda-102">Envoi d’un e-mail d’après l’adresse SMTP d’un compte</span><span class="sxs-lookup"><span data-stu-id="ccdda-102">Send an E-mail Given the SMTP Address of an Account</span></span>

<span data-ttu-id="ccdda-103">Cette rubrique montre comment créer un message électronique et l’envoyer à partir d’un compte Microsoft Outlook, l’adresse SMTP (Simple Mail Transfer Protocol) de ce compte étant donnée.</span><span class="sxs-lookup"><span data-stu-id="ccdda-103">This topic shows how to create an e-mail and send it from a Microsoft Outlook account, given the Simple Mail Transfer Protocol (SMTP) address of that account.</span></span>

## <a name="example"></a><span data-ttu-id="ccdda-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="ccdda-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ccdda-105">Helmut Obertanner a fourni les exemples de code suivants.</span><span class="sxs-lookup"><span data-stu-id="ccdda-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="ccdda-106">L’expertise de Helmut se trouve dans les outils de développement Office pour Visual Studio et Outlook.</span><span class="sxs-lookup"><span data-stu-id="ccdda-106">Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook.</span></span> 


<span data-ttu-id="ccdda-107">Les exemples de code suivants contiennent les méthodes SendEmailFromAccount et GetAccountForEmailAddress de la classe Sample, implémentée dans le cadre d’un projet de complément Outlook.</span><span class="sxs-lookup"><span data-stu-id="ccdda-107">The following code examples contain the   and   methods of the   class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="ccdda-108">Chaque projet ajoute une référence à l’assembly PIA (Primary Interop Assembly) Outlook, qui est basé sur l’espace de noms [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ccdda-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span> <span data-ttu-id="ccdda-109">La méthode SendEmailFromAccount accepte comme arguments d’entrée un objet [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) approuvé et des chaînes qui représentent l’objet du message, son corps, une liste de destinataires délimités par des points-virgules et l’adresse SMTP d’un compte de messagerie.</span><span class="sxs-lookup"><span data-stu-id="ccdda-109">The   method accepts as input arguments a trusted Application object, and strings that represent the subject, body, a semicolon-delimited list of recipients, and the SMTP address of an e-mail account.</span></span> <span data-ttu-id="ccdda-110">SendEmailFromAccount crée un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) et initialise les propriétés [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) et [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) avec les arguments fournis.</span><span class="sxs-lookup"><span data-stu-id="ccdda-110"> creates a MailItem object and initializes the To , Subject , and Body properties with the given arguments.</span></span> <span data-ttu-id="ccdda-111">Pour trouver l’objet [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) à partir duquel envoyer le message électronique, SendEmailFromAccount appelle la méthode GetAccountForEmailAddress, qui compare l’adresse SMTP donnée à la propriété [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) de chaque compte du profil actuel.</span><span class="sxs-lookup"><span data-stu-id="ccdda-111">To find the Account object from which to send the e-mail,   calls the   method, which matches the given SMTP address with the SmtpAddress property of each account for the current profile.</span></span> <span data-ttu-id="ccdda-112">L’objet **Account** correspondant est renvoyé à la méthode au SendEmailFromAccount, qui initialise la propriété [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) du **MailItem** avec cet objet **Account** et envoie le **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="ccdda-112">The matching Account object is returned to  , which then initializes the SendUsingAccount property of the MailItem with this Account object, and sends the MailItem.</span></span>

<span data-ttu-id="ccdda-113">L’exemple suivant est un exemple de code Visual Basic, suivi de l’exemple de code C\#.</span><span class="sxs-lookup"><span data-stu-id="ccdda-113">The following is the Visual Basic code example, followed by the C# code example.</span></span>

<span data-ttu-id="ccdda-114">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="ccdda-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ccdda-115">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="ccdda-115">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ccdda-116">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="ccdda-116">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

    End Class
End Namespace
```


```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="ccdda-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccdda-117">See also</span></span>

- [<span data-ttu-id="ccdda-118">Courrier</span><span class="sxs-lookup"><span data-stu-id="ccdda-118">Mail</span></span>](mail.md)

