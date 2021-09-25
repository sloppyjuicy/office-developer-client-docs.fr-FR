---
title: Exécuter une règle instantanément
TOCTitle: Execute a rule instantly
ms:assetid: b41031d5-aa81-40e2-ae78-b45a2f79eb5d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424476(v=office.15)
ms:contentKeyID: 55119919
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 563859880794ba75cea3f96ddbc2eb0ecdd17aff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574698"
---
# <a name="execute-a-rule-instantly"></a>Exécuter une règle instantanément

Cet exemple montre comment exécuter instantanément une règle à l’aide de la méthode [Execute(Object, Object, Object, Object)](https://msdn.microsoft.com/library/bb645769\(v=office.15\)) de l’objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)).

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Vous pouvez déclencher l'exécution immédiate d'une règle en appelant la méthode **Execute** sur l'objet **Rule**. Les paramètres de la méthode **Execute** sont facultatifs ; s'ils ne sont pas spécifiés, la règle sera appliquée à tous les messages de la Boîte de réception mais pas à ses sous-dossiers, et des valeurs par défaut seront utilisées pour les paramètres. Le tableau suivant répertorie les valeurs par défaut pour les paramètres facultatifs de la méthode **Execute**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre</p></th>
<th><p>Valeur par défaut</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ShowProgress</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>Dossier</p></td>
<td><p>Boîte de réception</p></td>
</tr>
<tr class="odd">
<td><p>IncludeSubfolders</p></td>
<td><p>False</p></td>
</tr>
<tr class="even">
<td><p>RuleExecuteOption</p></td>
<td><p>OlRuleExecuteOption.olRuleExecuteAllMessages</p></td>
</tr>
</tbody>
</table>


Vous pouvez annuler l’exécution d’une règle à l’aide de l’Assistant Règles et alertes. Vous pouvez aussi annuler l’exécution d’une règle en définissant le paramètre *ShowProgress* sur **true**, puis en annulant la boîte de dialogue de progression. Une fois que vous avez annulé la boîte de dialogue de progression, **Execute** renvoie une erreur.

Dans l’exemple de code suivant, ExecuteManagerRule obtient la règle qui a été créée dans la procédure CreateManagerRule de la rubrique [Créer une règle pour classer les éléments de courrier provenant d’un responsable et les marquer pour suivi](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md). ExecuteManagerRule vérifie ensuite si la règle n’est pas une référence NULL. Si ce n’est pas le cas, ExecuteManagerRule appelle la méthode **Execute** sur la règle avec les paramètres par défaut, exécutant immédiatement la règle.

> [!NOTE]
> Pour appliquer une règle une fois, indépendamment du fait que la propriété [Enabled](https://msdn.microsoft.com/library/bb609147(v=office.15)) retourne **true**, utilisez la méthode **Rule.Execute**. Pour appliquer la règle pour la session actuelle et au-delà de cette session, utilisez à la fois la propriété **Rule.Enabled** et la méthode [Save(Object)](https://msdn.microsoft.com/library/bb610738(v=office.15)) .

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique. Le code suivant illustre l’importation et l’affectation dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ExecuteManagerRule()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            string managerName = currentUser.
                GetExchangeUser().GetExchangeUserManager().Name;
            Outlook.Rule managerRule =
                Application.Session.DefaultStore.GetRules()[managerName];
            if (managerRule != null)
            {
                managerRule.Execute(false, Type.Missing,
                    Type.Missing, Type.Missing);
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Règles](rules.md)

