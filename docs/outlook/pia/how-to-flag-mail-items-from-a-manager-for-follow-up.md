---
title: Marquage des éléments de courrier envoyés par un manager pour le suivi
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
# <a name="flag-mail-items-from-a-manager-for-follow-up"></a>Marquage des éléments de courrier envoyés par un responsable pour le suivi

Cet exemple montre comment marquer des éléments de courrier provenant du responsable d’un utilisateur pour le suivi.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de la [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Microsoft Outlook fournit un système de marquage des tâches dans lequel certains éléments Outlook comme les éléments de courrier ou les contacts peuvent être marqués pour le suivi. Lorsque vous marquez un élément Outlook pour le suivi, les informations relatives à cet élément, ainsi que d'autres informations relatives aux tâches, sont affichées sur la **Barre des tâches** et sur le module de navigation Calendrier de l'interface utilisateur d'Outlook. La **Barre des tâches** est affichée dans un volet vertical dans une configuration standard de la fenêtre de l'explorateur Outlook. Elle contient un contrôle navigateur de dates, les rendez-vous à venir et les éléments qui ont été marqués pour le suivi. La **Barre des tâches** n'est pas extensible, et vous ne pouvez définir les options de configuration de la **Barre des tâches** que via l'interface utilisateur d'Outlook. Le marquage des éléments vous permet d'organiser et d'attribuer des priorités aux tâches et aux choses à faire.

L’exemple de code suivant marque un groupe d’éléments pour un intervalle de suivi spécifié. L’exemple récupère tous les éléments de la Boîte de réception de l’utilisateur actuel provenant du responsable de l’utilisateur actuel en utilisant une requête DASL pour filtrer les messages du type « IPM.NOTE » avec le nom du responsable comme expéditeur. Il marque ensuite tous les éléments en fonction de la valeur [OlImportance](https://msdn.microsoft.com/library/bb609592\(v=office.15\)) de la propriété [Importance](https://msdn.microsoft.com/library/bb611974\(v=office.15\)). Tous les éléments d’importance élevée sont marqués pour un suivi aujourd’hui et tous les éléments d’importance normale sont marqués pour un suivi cette semaine à l’aide de la méthode [MarkAsTask(OlMarkInterval)](https://msdn.microsoft.com/library/bb609068\(v=office.15\)).


> [!NOTE]
> La propriété **Importance** et la méthode **MarkAsTask** sont membres de l’objet **Item**.


Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Tâches](tasks.md)

