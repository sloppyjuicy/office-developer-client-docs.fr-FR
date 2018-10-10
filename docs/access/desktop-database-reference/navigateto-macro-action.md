---
title: AccéderA, action de macro
TOCTitle: NavigateTo Macro Action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9a6a59b6c84e9814aeb9b4709d27955f29fd9e1e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470752"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="e43c2-102">AccéderA, action de macro</span><span class="sxs-lookup"><span data-stu-id="e43c2-102">NavigateTo Macro Action</span></span>


<span data-ttu-id="e43c2-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e43c2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e43c2-p101">Utilisez l'action **AccéderA** pour contrôler l'affichage des objets de base de données dans le volet de navigation. Vous pouvez par exemple modifier le classement des objets de base de données et appliquer un filtre aux objets de sorte que seuls certains d'entre eux soient affichés.</span><span class="sxs-lookup"><span data-stu-id="e43c2-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="e43c2-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e43c2-106">Setting</span></span>

<span data-ttu-id="e43c2-107">L'action **AccéderA** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e43c2-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e43c2-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="e43c2-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e43c2-109">Description</span><span class="sxs-lookup"><span data-stu-id="e43c2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e43c2-110"><strong>Catégorie</strong></span><span class="sxs-lookup"><span data-stu-id="e43c2-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="e43c2-p102">Obligatoire. Catégorie dans laquelle les objets doivent être affichés dans le volet de navigation. Cliquez sur <strong>Type d’objet</strong>, <strong>Tables et vues</strong>, <strong>Modifié le</strong>, <strong>Créé le</strong> ou <strong>Personnalisé</strong> dans la zone <strong>Catégorie</strong>.</span><span class="sxs-lookup"><span data-stu-id="e43c2-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e43c2-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="e43c2-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="e43c2-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="e43c2-115">Optional.</span></span> <span data-ttu-id="e43c2-116">L’argument <strong>groupe</strong> limite les objets de la catégorie s’affichent dans le volet de Navigation.</span><span class="sxs-lookup"><span data-stu-id="e43c2-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="e43c2-117">Si vous laissez l’argument <strong>groupe</strong> vide, le volet de Navigation affiche tous les objets de base de données, classés selon les critères que vous spécifiez dans l’argument <strong>catégorie</strong> .</span><span class="sxs-lookup"><span data-stu-id="e43c2-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="e43c2-118">Des exemples d'arguments  <strong>Groupe</strong> valides pour les différents arguments <strong>Catégorie</strong> sont répertoriés dans le tableau ci-après.</span><span class="sxs-lookup"><span data-stu-id="e43c2-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e43c2-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="e43c2-119">Remarks</span></span>

  - <span data-ttu-id="e43c2-120">Cette action équivaut à sélectionner des catégories et des groupes dans la barre de titre du volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="e43c2-120">This action is similar to selecting categories and groups from the title bar of the Navigation Pane.</span></span>

  - <span data-ttu-id="e43c2-p104">La validité des arguments **Groupe** dépend de l'argument **Catégorie** utilisé. Si vous entrez un argument **Groupe** non valide, un message d'erreur s'affiche.Le tableau ci-dessous contient des exemples d'arguments **Groupe** valides pour chaque argument **Catégorie**.</span><span class="sxs-lookup"><span data-stu-id="e43c2-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="e43c2-123">Argument Catégorie</span><span class="sxs-lookup"><span data-stu-id="e43c2-123">Category argument</span></span></p></th>
    <th><p><span data-ttu-id="e43c2-124">Exemples d’arguments Groupe</span><span class="sxs-lookup"><span data-stu-id="e43c2-124">Example Group arguments</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="e43c2-125">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="e43c2-125">Object Type</span></span></p></td>
    <td><p><span data-ttu-id="e43c2-126">Tables, Formulaires, Requêtes, Pages, Macros, Modules</span><span class="sxs-lookup"><span data-stu-id="e43c2-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="e43c2-127">Tables et affichages</span><span class="sxs-lookup"><span data-stu-id="e43c2-127">Tables and Views</span></span></p></td>
    <td><p><span data-ttu-id="e43c2-128">Noms de tables donnés dans la base de données</span><span class="sxs-lookup"><span data-stu-id="e43c2-128">Names of specific tables in your database</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="e43c2-129">Modifié le</span><span class="sxs-lookup"><span data-stu-id="e43c2-129">Modified Date</span></span></p></td>
    <td><p><span data-ttu-id="e43c2-130">Aujourd'hui, Hier, Le mois dernier, Avant le mois dernier</span><span class="sxs-lookup"><span data-stu-id="e43c2-130">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="e43c2-131">Créé le</span><span class="sxs-lookup"><span data-stu-id="e43c2-131">Created Date</span></span></p></td>
    <td><p><span data-ttu-id="e43c2-132">Aujourd’hui, Hier, Le mois dernier, Avant le mois dernier</span><span class="sxs-lookup"><span data-stu-id="e43c2-132">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="e43c2-133">Catégorie personnalisée</span><span class="sxs-lookup"><span data-stu-id="e43c2-133">Custom category</span></span></p></td>
    <td><p><span data-ttu-id="e43c2-134">Noms des groupes que vous avez créés pour la catégorie personnalisée spécifiée</span><span class="sxs-lookup"><span data-stu-id="e43c2-134">Names of groups you have created for the specified custom category</span></span></p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="e43c2-135">Pour exécuter l'action **AccéderA** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **NavigateTo** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e43c2-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e43c2-p105">[!REMARQUE] Pour accéder au niveau supérieur d'une catégorie ( <STRONG>Toutes les tables</STRONG>, <STRONG>Tous les objets Access</STRONG> ou <STRONG>Toutes les dates</STRONG>, par exemple), vous devez laisser l'argument Groupe vide. Par exemple, lorsque l'argument <STRONG>Catégorie</STRONG> est défini sur <STRONG>Type d'objet</STRONG>, choisir <STRONG>Tous les objets Access</STRONG> en tant qu'argument <STRONG>Groupe</STRONG> génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="e43c2-p105">To navigate to the top level of a category (for example, <STRONG>All Tables</STRONG>, <STRONG>All Access Objects</STRONG>, or <STRONG>All Dates</STRONG>), you must leave the Group argument blank. For example, when the <STRONG>Category</STRONG> argument is <STRONG>Object Type</STRONG>, entering <STRONG>All Access Objects</STRONG> as a <STRONG>Group</STRONG> argument results in an error.</span></span></P>


