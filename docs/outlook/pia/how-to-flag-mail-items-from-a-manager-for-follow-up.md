---
title: Marquage des éléments de courrier envoyés par un responsable pour le suivi
TOCTitle: Flag mail items from a manager for follow-up
ms:assetid: 5f7f3678-0f63-451e-ba08-cd973525aa1b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424470(v=office.15)
ms:contentKeyID: 55119898
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 06e6bdd91198cabeff689681f2999d6fd2cb725a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542589"
---
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a><span data-ttu-id="5cf0a-102">Marquage des éléments de courrier envoyés par un responsable pour le suivi</span><span class="sxs-lookup"><span data-stu-id="5cf0a-102">Flag mail items from a manager for follow-up</span></span>

<span data-ttu-id="5cf0a-103">Cet exemple montre comment marquer des éléments de courrier provenant du responsable d’un utilisateur pour le suivi.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-103">This example shows how to flag email items that were received from the user’s manager for follow-up.</span></span>

## <a name="example"></a><span data-ttu-id="5cf0a-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="5cf0a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5cf0a-105">L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="5cf0a-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="5cf0a-p101">Microsoft Outlook fournit un système de marquage des tâches dans lequel certains éléments Outlook comme les éléments de courrier ou les contacts peuvent être marqués pour le suivi. Lorsque vous marquez un élément Outlook pour le suivi, les informations relatives à cet élément, ainsi que d'autres informations relatives aux tâches, sont affichées sur la **Barre des tâches** et sur le module de navigation Calendrier de l'interface utilisateur d'Outlook. La **Barre des tâches** est affichée dans un volet vertical dans une configuration standard de la fenêtre de l'explorateur Outlook. Elle contient un contrôle navigateur de dates, les rendez-vous à venir et les éléments qui ont été marqués pour le suivi. La **Barre des tâches** n'est pas extensible, et vous ne pouvez définir les options de configuration de la **Barre des tâches** que via l'interface utilisateur d'Outlook. Le marquage des éléments vous permet d'organiser et d'attribuer des priorités aux tâches et aux choses à faire.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-p101">Microsoft Outlook provides a task flagging system in which certain Outlook items such as mail items or contact items can be flagged for follow-up. When you flag an Outlook item for follow-up, information about that Outlook item, along with other task-based information, is displayed on the **To-Do Bar** and Calendar navigation module in the Outlook user interface. The **To-Do Bar** is displayed as a vertical pane in a typical configuration of the Outlook explorer window. It contains a date navigator control, upcoming appointments, and items that have been flagged for follow-up. The **To-Do Bar** itself is not extensible, and you can set configuration options for the **To-Do Bar** only through the Outlook user interface. Flagging items allows to you organize and prioritize tasks and to-do items.</span></span>

<span data-ttu-id="5cf0a-112">L’exemple de code suivant marque un groupe d’éléments pour un intervalle de suivi spécifié.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-112">The following code example marks a group of items for a specified follow-up interval.</span></span> <span data-ttu-id="5cf0a-113">L’exemple récupère tous les éléments de la Boîte de réception de l’utilisateur actuel provenant du responsable de l’utilisateur actuel en utilisant une requête DASL pour filtrer les messages du type « IPM.NOTE » avec le nom du responsable comme expéditeur.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-113">The example gets all items in the current user’s Inbox that are from the current user’s manager by using a DAV Searching and Locating (DASL) query to filter for messages of type “IPM.NOTE” with the manager’s name as the sender.</span></span> <span data-ttu-id="5cf0a-114">Il marque ensuite tous les éléments en fonction de la valeur [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) de la propriété [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5cf0a-114">It then flags all items according to the [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) value of the [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)) property.</span></span> <span data-ttu-id="5cf0a-115">Tous les éléments d’importance élevée sont marqués pour un suivi aujourd’hui et tous les éléments d’importance normale sont marqués pour un suivi cette semaine à l’aide de la méthode [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="5cf0a-115">All high-importance items are flagged for follow-up today and all normal-importance items are flagged for follow-up this week by using the [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)) method.</span></span>


> [!NOTE]
> <span data-ttu-id="5cf0a-116">La propriété **Importance** et la méthode **MarkAsTask** sont membres de l’objet **Item**.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-116">The **Importance** property and the **MarkAsTask** method are **Item** object members.</span></span>


<span data-ttu-id="5cf0a-117">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="5cf0a-118">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-118">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="5cf0a-119">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="5cf0a-119">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTaskFlagging()
{
    const string PR_SENT_REPRESENTING_NAME =
        "http://schemas.microsoft.com/mapi/proptag/0x0042001E";
    const string PR_MESSAGE_CLASS =
        "http://schemas.microsoft.com/mapi/proptag/0x001A001E";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager;
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            string filter = "@SQL=" + "\""
                + PR_SENT_REPRESENTING_NAME + "\""
                + " = '" + displayName + "'" + " AND " + "\""
                + PR_MESSAGE_CLASS + "\"" + " = 'IPM.NOTE'";
            Outlook.Items items =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).
                Items.Restrict(filter);
            foreach (Outlook.MailItem mail in items)
            {
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceHigh)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkToday);
                    mail.Save();
                }
                if (mail.Importance ==
                    Outlook.OlImportance.olImportanceNormal)
                {
                    mail.MarkAsTask(Outlook.OlMarkInterval.olMarkThisWeek);
                    mail.Save();
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5cf0a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf0a-120">See also</span></span>

- [<span data-ttu-id="5cf0a-121">Tâches</span><span class="sxs-lookup"><span data-stu-id="5cf0a-121">Tasks</span></span>](tasks.md)

