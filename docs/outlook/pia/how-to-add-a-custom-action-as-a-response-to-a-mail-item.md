---
title: Ajouter une action personnalisée en guise de réponse à un élément de courrier
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359751"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a>Ajouter une action personnalisée en guise de réponse à un élément de courrier

Cet exemple montre comment ajouter des actions personnalisées à un élément de courrier électronique à l’aide de la méthode [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) de la collection [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Vous pouvez créer des actions personnalisées par programmation de façon à ce qu’elles apparaissent sur le ruban dans le groupe **Actions** de l’onglet **Message** dans une réponse de message électronique. Dans l’exemple de code suivant, ReplyWithVoiceMail crée et ajoute une action personnalisée nommée « Reply with Voice Mail » à la barre de commandes de l’inspecteur. ReplyWithVoiceMail obtient d’abord un objet [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)), puis crée un objet [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) en appelant la méthode **Add** de la collection **Actions** qui est associée à l’objet **MailItem**. Il définit ensuite la propriété [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) de l’objet **Action** avec la valeur « Reply with Voice Mail ». Les propriétés [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)) et [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) sont également définies. Enfin, l’élément **MailItem** est enregistré.


> [!NOTE]
> Vous pouvez également ajouter des actions personnalisées au moment de la conception à l’aide du concepteur Forms d’Outlook.


Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Courrier](mail.md)

