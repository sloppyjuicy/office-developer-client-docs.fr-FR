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
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Si votre boîte aux lettres est hébergée sur un serveur Exchange, une règle est exécutable sur le serveur Exchange ou sur le client Outlook. Si la règle est exécutée sur le serveur, il n'est pas nécessaire qu'Outlook s'exécute pour que les conditions de la règle soient évaluées et que les actions de la règle soient exécutées. Si la règle est exécutée sur le client, Outlook doit s'exécuter pour que la règle s'exécute. Si la propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l'objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) retourne **true**, la règle est exécutée sur le client.

Pour les actions de règle qui s'exécutent par défaut sur le client (comme afficher une alerte de nouveau message électronique), la condition **OnLocalMachine** sera automatiquement activée, et la propriété [Enabled](https://msdn.microsoft.com/library/bb611875\(v=office.15\)) est définie à **true** pour un objet [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) côté client uniquement. Pour les actions de règle qui s'exécutent généralement sur le serveur, définissez la propriété **Enabled** de l'objet **RuleAction** côté client uniquement pour activer la condition **OnLocalMachine**. Cela forcera l'exécution de la règle localement sur le client. 

Si la condition **OnLocalMachine** pour une règle est activée, la condition [OnOtherMachine](https://msdn.microsoft.com/library/bb624486\(v=office.15\)) est également activée lorsque la même règle est examinée par une autre machine. Une condition de règle du type [olConditionOtherMachine](https://msdn.microsoft.com/library/bb645741\(v=office.15\)) signale que la règle est exécutable uniquement sur un ordinateur spécifique autre que l'ordinateur actuel, et n'est pas activable ou désactivable par programmation. Par exemple, si une règle est créée sur l'ordinateur actuel et que la condition de règle **OnLocalMachine** est activée, la règle est exécutable uniquement sur cet ordinateur. Si la même règle est exécutée sur un autre ordinateur, la règle indique que la condition de règle **OnOtherMachine** est activée.

Dans l’exemple de code suivant, DemoOnMachineOnly crée une règle et active la condition [OnlyToMe](https://msdn.microsoft.com/library/bb609250\(v=office.15\)) et l’action [Forward](https://msdn.microsoft.com/library/bb652908\(v=office.15\)) en définissant les propriétés **Enabled** sur **true**. La condition **OnLocalMachine** est activée, forçant une règle côté serveur à s’exécuter localement, et les règles sont enregistrées. Par défaut, une action **Forward** et une condition **OnlyToMe** fonctionneront sur le serveur. Une fois la condition **OnLocalMachine** activée, les règles fonctionnent comme des règles côté client.

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

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

