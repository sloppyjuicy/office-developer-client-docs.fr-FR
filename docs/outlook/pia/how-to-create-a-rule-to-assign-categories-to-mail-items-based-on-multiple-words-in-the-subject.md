---
title: Création d’une règle pour affecter des catégories aux éléments de courrier selon les mots employés dans l’objet
TOCTitle: Create a rule to assign categories to mail items based on multiple words in the subject
ms:assetid: 6e1fa40c-edf3-407c-9e90-99f634fa8e24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424472(v=office.15)
ms:contentKeyID: 55119918
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 1ff096454aa15a0a45c423913140eb50e6de9678
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406322"
---
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a>Création d’une règle pour affecter des catégories aux éléments de courrier selon les mots employés dans l’objet

Cet exemple montre comment configurer une règle qui affecte des catégories aux éléments de courrier en fonction de mots figurant dans l’objet.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Dans Outlook, les éléments peuvent être catégorisés pour faciliter l’organisation et l’affichage. Le modèle objet Outlook fournit l’objet [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) et la collection [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) pour représenter les catégories. Pour en savoir plus sur l’objet **Category** et la collection **Categories** pour un élément Outlook, consultez l’article [Énumérer et ajouter des catégories](how-to-enumerate-and-add-categories.md).

Une règle, représentée par un objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), peut être affectée avec plusieurs conditions. Vous pouvez obtenir ou définir un tableau qui représente les conditions à évaluer ou les actions à exécuter. Par exemple, la propriété [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) de l'objet [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) retourne ou définit un tableau d'éléments de type chaîne qui représente le texte que la condition de la règle doit évaluer. Vous devez assigner un tableau contenant une ou plusieurs chaînes pour l'évaluation. Pour évaluer plusieurs chaînes de caractères affectées dans un tableau, utilisez l’opérateur logique OR. 

Les propriétés à utiliser pour obtenir ou définir un tableau sont : [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) et **TextRuleCondition.Text**. Pour en savoir plus sur les règles, consultez l’article relatif à la [création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).

Dans l’exemple suivant, CreateTextAndCategoryRule utilise la méthode CategoryExists pour rechercher les éléments de courrier électronique de l’utilisateur dans toutes les catégories portant le nom « Office » ou « Outlook » dans la collection **Categories**. Si aucune catégorie n’est trouvée, les éléments de courrier sont ajoutés. L’exemple crée ensuite un tableau de chaînes qui inclut « Office », « Outlook » et « 2007 ». Ce tableau représente les conditions à évaluer. CreateTextAndCategoryRule crée ensuite une règle qui affecte des catégories en examinant l’objet du message par rapport aux conditions contenues dans le tableau à l’aide de la propriété **Text** de l’objet **TextRuleCondition** et de la propriété [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) de la collection [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)). Si la condition est satisfaite, les catégories Office et Outlook sont assignées à l'élément en utilisant la méthode [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) de l'objet [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) .

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateTextAndCategoryRule()
{
    if (!CategoryExists("Office"))
    {
        Application.Session.Categories.Add(
            "Office", Type.Missing, Type.Missing);
    }
    if (!CategoryExists("Outlook"))
    {
        Application.Session.Categories.Add(
            "Outlook", Type.Missing, Type.Missing);
    }
    Outlook.Rules rules =
        Application.Session.DefaultStore.GetRules();
    Outlook.Rule textRule =
        rules.Create("Demo Text and Category Rule",
        Outlook.OlRuleType.olRuleReceive);
    Object[] textCondition = 
        { "Office", "Outlook", "2007" };
    Object[] categoryAction = 
        { "Office", "Outlook" };
    textRule.Conditions.BodyOrSubject.Text =
        textCondition;
    textRule.Conditions.BodyOrSubject.Enabled = true;
    textRule.Actions.AssignToCategory.Categories =
        categoryAction;
    textRule.Actions.AssignToCategory.Enabled = true;
    rules.Save(true);
}

// Determines if categoryName exists in Categories collection
private bool CategoryExists(string categoryName)
{
    try
    {
        Outlook.Category category =
            Application.Session.Categories[categoryName];
        if (category != null)
        {
            return true;
        }
        else
        {
            return false;
        }
    }
    catch { return false; }
}
```

## <a name="see-also"></a>Voir aussi

- [Règles](rules.md)

