---
title: Ajouter des options de vote à un élément de courrier
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6a65bdd5086a10b2d6e9803047555a8b052ff38e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407169"
---
# <a name="add-voting-options-to-a-mail-item"></a>Ajouter des options de vote à un élément de courrier

Cet exemple montre comment utiliser la propriété [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) de l’objet [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) pour ajouter des options de vote à un message électronique.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).


Les options de vote dans des messages servent à proposer aux destinataires d'un message une liste de choix et à suivre leurs réponses. Pour créer des options de vote par programme, définissez une chaîne correspondant à une liste de valeurs délimitées par des points-virgules pour la propriété **VotingOptions** d'un objet **MailItem**. Les valeurs de la propriété **VotingOptions** apparaissent sous la commande **Vote** du groupe **Répondre** dans le ruban du message reçu.

Dans l’exemple suivant, OrderPizza crée des options de vote dans un nouveau message électronique. OrderPizza crée d’abord un objet **MailItem**, puis définit la propriété sur **VotingOptions** sur « Cheese; Mushroom; Sausage; Combo; Veg Combo », puis la propriété [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) sur « Pizza Order ». Lorsque le message « Pizza Order » est envoyé, les options de vote apparaissent aux destinataires. Pour chaque réponse reçue, le choix du destinataire sera reporté dans la page **Suivi** du message dans le dossier Éléments envoyés de l’expéditeur.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a>Voir aussi

- [Courrier](mail.md)

