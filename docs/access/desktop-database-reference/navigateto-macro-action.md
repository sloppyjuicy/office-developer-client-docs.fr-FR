---
title: NavigateTo, action de macro
TOCTitle: NavigateTo macro action
ms:assetid: 6594d614-3ea6-7851-b70e-1661d24f8ba0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195165(v=office.15)
ms:contentKeyID: 48545324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm119055
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d8747c5c4fd1a32a36841f648017bc0cab3de8f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920808"
---
# <a name="navigateto-macro-action"></a><span data-ttu-id="0c635-102">NavigateTo, action de macro</span><span class="sxs-lookup"><span data-stu-id="0c635-102">NavigateTo macro action</span></span>


<span data-ttu-id="0c635-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c635-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c635-p101">Utilisez l'action **AccéderA** pour contrôler l'affichage des objets de base de données dans le volet de navigation. Vous pouvez par exemple modifier le classement des objets de base de données et appliquer un filtre aux objets de sorte que seuls certains d'entre eux soient affichés.</span><span class="sxs-lookup"><span data-stu-id="0c635-p101">You can use the **NavigateTo** action to control the display of database objects in the Navigation Pane. For example, you can change how the database objects are categorized, and you can filter the objects so that only certain ones are displayed.</span></span>

## <a name="setting"></a><span data-ttu-id="0c635-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c635-106">Setting</span></span>

<span data-ttu-id="0c635-107">L'action **AccéderA** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="0c635-107">The **NavigateTo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0c635-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="0c635-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0c635-109">Description</span><span class="sxs-lookup"><span data-stu-id="0c635-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c635-110"><strong>Catégorie</strong></span><span class="sxs-lookup"><span data-stu-id="0c635-110"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="0c635-p102">Obligatoire. Catégorie dans laquelle les objets doivent être affichés dans le volet de navigation. Cliquez sur <strong>Type d’objet</strong>, <strong>Tables et vues</strong>, <strong>Modifié le</strong>, <strong>Créé le</strong> ou <strong>Personnalisé</strong> dans la zone <strong>Catégorie</strong>.</span><span class="sxs-lookup"><span data-stu-id="0c635-p102">Required. The category by which you want the Navigation Pane to display objects. Click <strong>Object Type</strong>, <strong>Tables and Views</strong>, <strong>Modified Date</strong>, <strong>Created Date</strong>, or <strong>Custom</strong> in the <strong>Category</strong> box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c635-114"><strong>Group</strong></span><span class="sxs-lookup"><span data-stu-id="0c635-114"><strong>Group</strong></span></span></p></td>
<td><p><span data-ttu-id="0c635-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="0c635-115">Optional.</span></span> <span data-ttu-id="0c635-116">L’argument <strong>groupe</strong> limite les objets de la catégorie s’affichent dans le volet de Navigation.</span><span class="sxs-lookup"><span data-stu-id="0c635-116">The <strong>Group</strong> argument limits which objects in the category appear in the Navigation Pane.</span></span> <span data-ttu-id="0c635-117">Si vous laissez l’argument <strong>groupe</strong> vide, le volet de Navigation affiche tous les objets de base de données, classés selon les critères que vous spécifiez dans l’argument <strong>catégorie</strong> .</span><span class="sxs-lookup"><span data-stu-id="0c635-117">If you leave the <strong>Group</strong> argument blank, the Navigation Pane displays all database objects, categorized by the criteria you specify in the <strong>Category</strong> argument.</span></span> <span data-ttu-id="0c635-118">Des exemples d'arguments  <strong>Groupe</strong> valides pour les différents arguments <strong>Catégorie</strong> sont répertoriés dans le tableau ci-après.</span><span class="sxs-lookup"><span data-stu-id="0c635-118">Examples of valid <strong>Group</strong> arguments for the various <strong>Category</strong> arguments are shown in the following table.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0c635-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c635-119">Remarks</span></span>

  - <span data-ttu-id="0c635-120">Cette action équivaut à sélectionner des catégories et des groupes dans la barre de titre du volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="0c635-120">This action is similar to selecting categories and groups from the title bar of the Navigation Pane.</span></span>

  - <span data-ttu-id="0c635-p104">La validité des arguments **Groupe** dépend de l'argument **Catégorie** utilisé. Si vous entrez un argument **Groupe** non valide, un message d'erreur s'affiche.Le tableau ci-dessous contient des exemples d'arguments **Groupe** valides pour chaque argument **Catégorie**.</span><span class="sxs-lookup"><span data-stu-id="0c635-p104">Valid **Group** arguments depend on which **Category** argument is used. If you enter an invalid **Group** argument, an error message appears.The following table contains examples of valid **Group** arguments for each **Category** argument.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="0c635-123">Argument Catégorie</span><span class="sxs-lookup"><span data-stu-id="0c635-123">Category argument</span></span></p></th>
    <th><p><span data-ttu-id="0c635-124">Exemples d’arguments Groupe</span><span class="sxs-lookup"><span data-stu-id="0c635-124">Example Group arguments</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="0c635-125">Type d'objet</span><span class="sxs-lookup"><span data-stu-id="0c635-125">Object Type</span></span></p></td>
    <td><p><span data-ttu-id="0c635-126">Tables, Formulaires, Requêtes, Pages, Macros, Modules</span><span class="sxs-lookup"><span data-stu-id="0c635-126">Tables; Forms; Queries; Pages; Macros; Modules</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="0c635-127">Tables et affichages</span><span class="sxs-lookup"><span data-stu-id="0c635-127">Tables and Views</span></span></p></td>
    <td><p><span data-ttu-id="0c635-128">Noms de tables donnés dans la base de données</span><span class="sxs-lookup"><span data-stu-id="0c635-128">Names of specific tables in your database</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="0c635-129">Modifié le</span><span class="sxs-lookup"><span data-stu-id="0c635-129">Modified Date</span></span></p></td>
    <td><p><span data-ttu-id="0c635-130">Aujourd'hui, Hier, Le mois dernier, Avant le mois dernier</span><span class="sxs-lookup"><span data-stu-id="0c635-130">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="0c635-131">Créé le</span><span class="sxs-lookup"><span data-stu-id="0c635-131">Created Date</span></span></p></td>
    <td><p><span data-ttu-id="0c635-132">Aujourd’hui, Hier, Le mois dernier, Avant le mois dernier</span><span class="sxs-lookup"><span data-stu-id="0c635-132">Today; Yesterday; Last Month; Older</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="0c635-133">Catégorie personnalisée</span><span class="sxs-lookup"><span data-stu-id="0c635-133">Custom category</span></span></p></td>
    <td><p><span data-ttu-id="0c635-134">Noms des groupes que vous avez créés pour la catégorie personnalisée spécifiée</span><span class="sxs-lookup"><span data-stu-id="0c635-134">Names of groups you have created for the specified custom category</span></span></p></td>
    </tr>
    </tbody>
    </table>


  - <span data-ttu-id="0c635-135">Pour exécuter l'action **AccéderA** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **NavigateTo** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="0c635-135">To run the **NavigateTo** action in a VBA module, use the **NavigateTo** method of the **DoCmd** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0c635-p105">[!REMARQUE] Pour accéder au niveau supérieur d'une catégorie ( <STRONG>Toutes les tables</STRONG>, <STRONG>Tous les objets Access</STRONG> ou <STRONG>Toutes les dates</STRONG>, par exemple), vous devez laisser l'argument Groupe vide. Par exemple, lorsque l'argument <STRONG>Catégorie</STRONG> est défini sur <STRONG>Type d'objet</STRONG>, choisir <STRONG>Tous les objets Access</STRONG> en tant qu'argument <STRONG>Groupe</STRONG> génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="0c635-p105">To navigate to the top level of a category (for example, <STRONG>All Tables</STRONG>, <STRONG>All Access Objects</STRONG>, or <STRONG>All Dates</STRONG>), you must leave the Group argument blank. For example, when the <STRONG>Category</STRONG> argument is <STRONG>Object Type</STRONG>, entering <STRONG>All Access Objects</STRONG> as a <STRONG>Group</STRONG> argument results in an error.</span></span></P>


