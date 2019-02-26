---
title: Exécuter une règle sur un ordinateur local
TOCTitle: Execute a rule on a local computer
ms:assetid: 65e91010-3e4c-4921-a0fb-ad90a7b841b2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424471(v=office.15)
ms:contentKeyID: 55119883
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 76587a72d9c77a5484d9aa9788173f9f40f57614
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405839"
---
# <a name="execute-a-rule-on-a-local-computer"></a>Exécuter une règle sur un ordinateur local

Cet exemple montre comment exécuter une règle sur un ordinateur local à l’aide de la propriété [OnLocalMachine](https://msdn.microsoft.com/library/bb612005\(v=office.15\)) de l’objet [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est extrait du livre[programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (non traduit)..

Si votre boîte aux lettres est hébergée sur un serveur Exchange, vous pouvez exécuter une règle sur le serveur Exchange ou sur le client Outlook. Si vous exécutez la règle sur le serveur, vous n’avez pas besoin d’exécuter Outlook pour évaluer les conditions de la règle et exécuter ses actions. Si vous exécutez la règle sur le client, vous devez exécuter Outlook. Si la propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l’objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) retourne **true**, la règle doit être exécutée sur le client.

En cas d’exécution d’actions de règle par défaut sur le client (comme l’affichage d’une alerte de nouveau message électronique), la condition **OnLocalMachine** s’active automatiquement, tandis que le système définit la propriété [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) sur **true** pour un objet [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) côté client. Si des actions de règle s’exécutent globalement sur le serveur, veuillez définir la propriété **Enabled** de l’objet **RuleAction** côté client pour activer la condition **OnLocalMachine**. Vous forcez ainsi l’exécution de la règle sur le client en local. 

Si la condition **OnLocalMachine** d’une règle s’active, la condition [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) s’active aussi, lorsqu’une autre machine examine la même règle. Une condition de règle du type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) indique que vous pouvez uniquement exécuter la règle sur un ordinateur distinct de l’ordinateur actuel, et que vous ne pouvez pas l’activer ou la désactiver par programmation. Par exemple, si vous créez une règle sur l’ordinateur actuel tout en ayant activé la condition de règle **OnLocalMachine**, vous devez exécuter cette règle sur cet ordinateur, et seulement lui. Si vous exécutez cette règle sur un autre ordinateur, la règle indique que la condition de règle **OnOtherMachine** est active.

Dans l’exemple de code suivant, DemoOnMachineOnly crée une règle et active la condition [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) et l’action [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) en définissant les propriétés **Enabled** sur **true**. La condition **OnLocalMachine** s’active, forçant l’exécution en local d’une règle côté serveur. Puis le système enregistre les règles. Par défaut, une action **Forward** et une condition **OnlyToMe** fonctionneront sur le serveur. Une fois la condition **OnLocalMachine** activée, les règles fonctionnent comme des règles côté client.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoOnMachineOnly()
{
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule rule =
        rules.Create("Demo Machine Only Rule",
        Outlook.OlRuleType.olRuleReceive);
    rule.Conditions.OnlyToMe.Enabled = true;
    rule.Actions.Forward.Enabled = true;
    rule.Actions.Forward.Recipients.Add("someone@example.com");
    rule.Actions.Forward.Recipients.ResolveAll();

    // Force the rule to execute locally
    rule.Conditions.OnLocalMachine.Enabled = true;
    rules.Save(true);
}
```

## <a name="see-also"></a>Voir aussi

- [Règles](rules.md)

