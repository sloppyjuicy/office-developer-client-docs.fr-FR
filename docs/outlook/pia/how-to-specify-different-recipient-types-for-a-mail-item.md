---
title: Spécifier différents types de destinataires pour un élément de messagerie
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335510"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="6198b-102">Spécifier différents types de destinataires pour un élément de messagerie</span><span class="sxs-lookup"><span data-stu-id="6198b-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="6198b-103">Cet exemple montre comment définir par programmation différents types de destinataires (À, Cc ou Cci) pour un élément de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6198b-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="6198b-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="6198b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6198b-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="6198b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="6198b-106">L’exemple de code suivant illustre comment spécifier si un destinataire d’un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) est un destinataire de type À, Cc ou Cci.</span><span class="sxs-lookup"><span data-stu-id="6198b-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="6198b-107">SetRecipientTypeForMail crée un objet **MailItem**, ajoute trois objets [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) à la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de **MailItem**, puis affecte à la propriété [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de chaque objet **Recipient** une valeur de l’énumération [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="6198b-107">SetRecipientTypeForMail creates a **MailItem** object, adds three [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) objects to the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection of the **MailItem**, and then sets the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of each **Recipient** object to a value from the [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="6198b-108">La propriété **Type** de l’objet **Recipient** est un type int et n’est en corrélation avec aucune énumération de type de destinataire spécifique.</span><span class="sxs-lookup"><span data-stu-id="6198b-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="6198b-109">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="6198b-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="6198b-110">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="6198b-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="6198b-111">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="6198b-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="6198b-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6198b-112">See also</span></span>

- [<span data-ttu-id="6198b-113">Courrier</span><span class="sxs-lookup"><span data-stu-id="6198b-113">Mail</span></span>](mail.md)

