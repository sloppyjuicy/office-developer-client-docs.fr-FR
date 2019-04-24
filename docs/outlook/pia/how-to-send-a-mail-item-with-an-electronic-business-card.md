---
title: Envoi d’un élément de courrier avec une carte de visite électronique
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25809fc0d1726c9f56be417ae53fadecc831d62f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331149"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a><span data-ttu-id="e4268-102">Envoi d’un élément de courrier avec une carte de visite électronique</span><span class="sxs-lookup"><span data-stu-id="e4268-102">Send a mail item with an electronic business card</span></span>

<span data-ttu-id="e4268-103">Cet exemple crée un élément de courrier, recherche une carte de visite électronique et, s’il en trouve une, l’insère dans l’élément de courrier.</span><span class="sxs-lookup"><span data-stu-id="e4268-103">This example creates a mail item, looks for an electronic business card, and if it finds one, inserts the electronic business card into the mail item.</span></span>

## <a name="example"></a><span data-ttu-id="e4268-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4268-104">Example</span></span>

<span data-ttu-id="e4268-105">Pour insérer une carte de visite électronique, vous pouvez appeler la méthode [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) sur l’objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="e4268-105">To insert an electronic business card, you can call [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) on the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="e4268-106">Cette méthode prend une chaîne représentant une adresse e-mail et essaie de trouver un [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) avec cette adresse dans le dossier Contacts par défaut.</span><span class="sxs-lookup"><span data-stu-id="e4268-106">This method takes a string representing an email address and attempts to find a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) with that address in the default Contacts folder.</span></span> <span data-ttu-id="e4268-107">Un **ContactItem** peut avoir jusqu’à trois adresses e-mail.</span><span class="sxs-lookup"><span data-stu-id="e4268-107">A **ContactItem** can have as many as three email addresses.</span></span> <span data-ttu-id="e4268-108">Si un contact est trouvé, l’exemple appelle la méthode **AddBusinessCard**, puis présente le message à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e4268-108">If the contact is found, the example calls the **AddBusinessCard** method, and then displays the message to the user.</span></span>

<span data-ttu-id="e4268-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="e4268-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="e4268-110">L'instruction **Importer** ou **utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="e4268-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="e4268-111">Les lignes de code suivantes montrent comment effectuer l’importation et l’affectation dans Visual Basic et dans C\#.</span><span class="sxs-lookup"><span data-stu-id="e4268-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub AddBusinessCard(ByVal eMailAddress As String)
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML
    Dim contact As Outlook.ContactItem = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find( _
        "[Email1Address]='" & eMailAddress & "'" & " OR " & _
        "[Email2Address]='" & eMailAddress & "'" + " OR " & _
        "[Email3Address]='" & eMailAddress & "'") _
        , Outlook.ContactItem)
    If (contact Is Nothing) Then
        Return
    End If
    mail.AddBusinessCard(contact)
    mail.Display(False)
End Sub
```


```csharp
private void AddBusinessCard(string eMailAddress)
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML;
    Outlook.ContactItem contact = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Email1Address]='" + eMailAddress + "'" + " OR " +
        "[Email2Address]='" + eMailAddress + "'" + " OR " +
        "[Email3Address]='" + eMailAddress + "'")
        as Outlook.ContactItem;
    if (contact == null)
    {
        return;
    }
    mail.AddBusinessCard(contact);
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="e4268-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4268-112">See also</span></span>

- [<span data-ttu-id="e4268-113">Cartes de visite électroniques</span><span class="sxs-lookup"><span data-stu-id="e4268-113">Electronic business cards</span></span>](electronic-business-cards.md)

