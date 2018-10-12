---
title: Ajouter une action personnalisée en guise de réponse à un élément de courrier
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1858372ec8283b1926e5ed82f2a511a97a8242ec
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406854"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="11982-102">Ajouter une action personnalisée en guise de réponse à un élément de courrier</span><span class="sxs-lookup"><span data-stu-id="11982-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="11982-103">Cet exemple montre comment ajouter des actions personnalisées à un élément de courrier électronique à l’aide de la méthode [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) de la collection [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="11982-103">This example shows how to add custom actions as a response to an e-mail item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="11982-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="11982-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="11982-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="11982-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="11982-106">Vous pouvez créer des actions personnalisées par programmation de façon à ce qu’elles apparaissent sur le ruban dans le groupe **Actions** de l’onglet **Message** dans une réponse de message électronique.</span><span class="sxs-lookup"><span data-stu-id="11982-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an e-mail response.</span></span> <span data-ttu-id="11982-107">Dans l’exemple de code suivant, ReplyWithVoiceMail crée et ajoute une action personnalisée nommée « Reply with Voice Mail » à la barre de commandes de l’inspecteur.</span><span class="sxs-lookup"><span data-stu-id="11982-107">In the following code example,   creates and adds a custom action named "Reply with Voice Mail" to the inspector command bar.</span></span> <span data-ttu-id="11982-108">ReplyWithVoiceMail obtient d’abord un objet [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)), puis crée un objet [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) en appelant la méthode **Add** de la collection **Actions** qui est associée à l’objet **MailItem**.</span><span class="sxs-lookup"><span data-stu-id="11982-108"> first gets a _MailItem object and then creates an Action object by calling the Add method of the Actions collection that is associated with the MailItem.</span></span> <span data-ttu-id="11982-109">Il définit ensuite la propriété [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) de l’objet **Action** avec la valeur « Reply with Voice Mail ».</span><span class="sxs-lookup"><span data-stu-id="11982-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to "Reply with Voice Mail".</span></span> <span data-ttu-id="11982-110">Les propriétés [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) et [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) sont également définies.</span><span class="sxs-lookup"><span data-stu-id="11982-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)) , [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)) , [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) , and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="11982-111">Enfin, l’élément **MailItem** est enregistré.</span><span class="sxs-lookup"><span data-stu-id="11982-111">Finally, the **MailItem**is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="11982-112">Vous pouvez également ajouter des actions personnalisées au moment de la conception à l’aide du concepteur Forms d’Outlook.</span><span class="sxs-lookup"><span data-stu-id="11982-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="11982-113">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="11982-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="11982-114">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="11982-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="11982-115">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="11982-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a><span data-ttu-id="11982-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11982-116">See also</span></span>

- [<span data-ttu-id="11982-117">Courrier</span><span class="sxs-lookup"><span data-stu-id="11982-117">Mail</span></span>](mail.md)

