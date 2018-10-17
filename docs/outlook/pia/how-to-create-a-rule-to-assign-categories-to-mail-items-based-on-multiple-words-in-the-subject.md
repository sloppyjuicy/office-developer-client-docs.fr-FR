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
# <a name="create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject"></a><span data-ttu-id="31088-102">Création d’une règle pour affecter des catégories aux éléments de courrier selon les mots employés dans l’objet</span><span class="sxs-lookup"><span data-stu-id="31088-102">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>

<span data-ttu-id="31088-103">Cet exemple montre comment configurer une règle qui affecte des catégories aux éléments de courrier en fonction de mots figurant dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="31088-103">This example shows how to set up a rule that assigns categories to mail items based on multiple words in the subject.</span></span>

## <a name="example"></a><span data-ttu-id="31088-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="31088-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="31088-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="31088-105">The following code example is an excerpt from  [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)  , from Microsoft Press (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="31088-106">Dans Outlook, les éléments peuvent être catégorisés pour faciliter l’organisation et l’affichage.</span><span class="sxs-lookup"><span data-stu-id="31088-106">In Outlook, items can be categorized for easier organization and display.</span></span> <span data-ttu-id="31088-107">Le modèle objet Outlook fournit l’objet [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) et la collection [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) pour représenter les catégories.</span><span class="sxs-lookup"><span data-stu-id="31088-107">The Outlook object model provides the [Category](https://msdn.microsoft.com/library/bb623480\(v=office.15\)) object and the [Categories](https://msdn.microsoft.com/library/bb623535\(v=office.15\)) collection to represent categories.</span></span> <span data-ttu-id="31088-108">Pour en savoir plus sur l’objet **Category** et la collection **Categories** pour un élément Outlook, consultez l’article [Énumérer et ajouter des catégories](how-to-enumerate-and-add-categories.md).</span><span class="sxs-lookup"><span data-stu-id="31088-108">For more information about the **Category** object and the **Categories** collection for an Outlook item, see [How to: Enumerate and Add Categories](how-to-enumerate-and-add-categories.md).</span></span>

<span data-ttu-id="31088-109">Une règle, représentée par un objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)), peut être affectée avec plusieurs conditions.</span><span class="sxs-lookup"><span data-stu-id="31088-109">A rule, represented by a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object, can be assigned with multiple conditions.</span></span> <span data-ttu-id="31088-110">Vous pouvez obtenir ou définir un tableau qui représente les conditions à évaluer ou les actions à exécuter.</span><span class="sxs-lookup"><span data-stu-id="31088-110">You can get or set an array that represents conditions to be evaluated or actions to be completed.</span></span> <span data-ttu-id="31088-111">Par exemple, la propriété [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) de l'objet [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) retourne ou définit un tableau d'éléments de type chaîne qui représente le texte que la condition de la règle doit évaluer.</span><span class="sxs-lookup"><span data-stu-id="31088-111">For example, the [Text](https://msdn.microsoft.com/library/bb611271\(v=office.15\)) property of the [TextRuleCondition](https://msdn.microsoft.com/library/bb644796\(v=office.15\)) object returns or sets an array of string elements that represents the text to be evaluated by the rule condition.</span></span> <span data-ttu-id="31088-112">Vous devez assigner un tableau contenant une ou plusieurs chaînes pour l'évaluation.</span><span class="sxs-lookup"><span data-stu-id="31088-112">You must assign an array with one string or multiple strings for evaluation.</span></span> <span data-ttu-id="31088-113">Pour évaluer plusieurs chaînes de caractères affectées dans un tableau, utilisez l’opérateur logique OR.</span><span class="sxs-lookup"><span data-stu-id="31088-113">To evaluate multiple text strings that are assigned in an array, use the logical OR operation.</span></span> 

<span data-ttu-id="31088-114">Les propriétés à utiliser pour obtenir ou définir un tableau sont : [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)), [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)), [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) et **TextRuleCondition.Text**.</span><span class="sxs-lookup"><span data-stu-id="31088-114">The properties that you can use to get or set an array are as follows: [Address](https://msdn.microsoft.com/library/bb647045\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb611021\(v=office.15\)) , [Categories](https://msdn.microsoft.com/library/bb612345\(v=office.15\)) , [FormName](https://msdn.microsoft.com/library/bb647042\(v=office.15\)) , and **TextRuleCondition.Text**.</span></span> <span data-ttu-id="31088-115">Pour en savoir plus sur les règles, consultez l’article relatif à la [création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span><span class="sxs-lookup"><span data-stu-id="31088-115">For more information about rules, see [How to: Create a Rule to File Mail Items from a Manager and Flag Them for Follow-Up](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md).</span></span>

<span data-ttu-id="31088-116">Dans l’exemple suivant, CreateTextAndCategoryRule utilise la méthode CategoryExists pour rechercher les éléments de courrier électronique de l’utilisateur dans toutes les catégories portant le nom « Office » ou « Outlook » dans la collection **Categories**.</span><span class="sxs-lookup"><span data-stu-id="31088-116">In the following example,   uses the   method to check the user's mail items for any categories by the name "Office" or "Outlook" in the Categories collection.</span></span> <span data-ttu-id="31088-117">Si aucune catégorie n’est trouvée, les éléments de courrier sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="31088-117">If no categories are found, they are added.</span></span> <span data-ttu-id="31088-118">L’exemple crée ensuite un tableau de chaînes qui inclut « Office », « Outlook » et « 2007 ».</span><span class="sxs-lookup"><span data-stu-id="31088-118">The example then creates an array of strings that include "Office, "Outlook", and "2007".</span></span> <span data-ttu-id="31088-119">Ce tableau représente les conditions à évaluer.</span><span class="sxs-lookup"><span data-stu-id="31088-119">This array will represent the conditions to be evaluated.</span></span> <span data-ttu-id="31088-120">CreateTextAndCategoryRule crée ensuite une règle qui affecte des catégories en examinant l’objet du message par rapport aux conditions contenues dans le tableau à l’aide de la propriété **Text** de l’objet **TextRuleCondition** et de la propriété [BodyOrSubject](https://msdn.microsoft.com/library/bb612744\(v=office.15\)) de la collection [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="31088-120"> then creates a rule that assigns categories by examining the subject for any of the conditions in the array by using the Text property of the TextRuleCondition object and the BodyOrSubject property of the RuleConditions collection.</span></span> <span data-ttu-id="31088-121">Si la condition est satisfaite, les catégories Office et Outlook sont assignées à l'élément en utilisant la méthode [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) de l'objet [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="31088-121">If the condition is satisfied, the categories of Office and Outlook are assigned to the item by using the [AssignToCategory](https://msdn.microsoft.com/library/bb623146\(v=office.15\)) method of the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) object.</span></span>

<span data-ttu-id="31088-122">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="31088-122">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="31088-123">L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="31088-123">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="31088-124">La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.</span><span class="sxs-lookup"><span data-stu-id="31088-124">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="31088-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31088-125">See also</span></span>

- [<span data-ttu-id="31088-126">Règles</span><span class="sxs-lookup"><span data-stu-id="31088-126">Rules</span></span>](rules.md)

