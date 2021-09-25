---
title: Spécifier différents types de destinataires pour un élément de messagerie
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 592dc4ca206e71079e794e19e3ba65790be2169e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574650"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a>Spécifier différents types de destinataires pour un élément de messagerie

Cet exemple montre comment définir par programmation différents types de destinataires (À, Cc ou Cci) pour un élément de messagerie.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

L’exemple de code suivant illustre comment spécifier si un destinataire d’un objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) est un destinataire de type À, Cc ou Cci. SetRecipientTypeForMail crée un objet **MailItem**, ajoute trois objets [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) à la collection [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) de **MailItem**, puis affecte à la propriété [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) de chaque objet **Recipient** une valeur de l’énumération [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)).


> [!NOTE]
> La propriété **Type** de l’objet **Recipient** est un type int et n’est en corrélation avec aucune énumération de type de destinataire spécifique.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

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

## <a name="see-also"></a>Voir aussi

- [Courrier](mail.md)

