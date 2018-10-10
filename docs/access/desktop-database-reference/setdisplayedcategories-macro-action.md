---
title: DéfinirCatégoriesAffichées, action de macro
TOCTitle: SetDisplayedCategories Macro Action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
ms.openlocfilehash: af4b491ff76a28c998e1ec195a861dbf065d36c8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471824"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="e8d76-102">DéfinirCatégoriesAffichées, action de macro</span><span class="sxs-lookup"><span data-stu-id="e8d76-102">SetDisplayedCategories Macro Action</span></span>


<span data-ttu-id="e8d76-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8d76-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8d76-p101">L'action **DéfinirCatégoriesAffichées** permet de spécifier les catégories affichées sous **Atteindre la catégorie** dans la barre de titre du volet de navigation. Par exemple, si vous souhaitez empêcher les utilisateurs de modifier le volet de navigation de façon à afficher les objets triés par **Date de création**, utilisez cette action pour masquer cette option dans la liste déroulante de la barre de titre.</span><span class="sxs-lookup"><span data-stu-id="e8d76-p101">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane. For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="e8d76-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8d76-106">Setting</span></span>

<span data-ttu-id="e8d76-107">L'action **DéfinirCatégoriesAffichées** accepte les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e8d76-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8d76-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="e8d76-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="e8d76-109">Description</span><span class="sxs-lookup"><span data-stu-id="e8d76-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8d76-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="e8d76-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d76-p102">Sélectionnez <strong>Oui</strong> pour afficher les catégories. Sélectionnez <strong>Non</strong> pour les masquer.</span><span class="sxs-lookup"><span data-stu-id="e8d76-p102">Select <strong>Yes</strong> to show the category or categories. Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8d76-113"><strong>Catégorie</strong></span><span class="sxs-lookup"><span data-stu-id="e8d76-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="e8d76-p103">Entrez ou sélectionnez le nom de la catégorie que vous souhaitez afficher ou masquer. Laissez ce champ vide pour afficher ou masquer toutes les catégories.</span><span class="sxs-lookup"><span data-stu-id="e8d76-p103">Enter or select the name of the category you want to show or hide. Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e8d76-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e8d76-116">Remarks</span></span>

  - <span data-ttu-id="e8d76-p104">La légende dans la barre de titre du volet de navigation indique le filtre activé, le cas échéant. Cliquez n'importe où dans la barre pour afficher la liste déroulante. Les éléments contrôlés par cette macro sont répertoriés sous **Atteindre la catégorie**.</span><span class="sxs-lookup"><span data-stu-id="e8d76-p104">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active. Click anywhere in the bar to display the drop-down list. The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="e8d76-p105">Cette action active ou désactive uniquement l'affichage de la ou des catégories spécifiées ; elle ne modifie pas l'affichage du volet de navigation. Par exemple, si vous affichez les objets triés par **Date de création** et que vous utilisez l'action **DéfinirCatégoriesAffichées** pour désactiver l'option **Date de création**, Access n'affiche aucune autre catégorie dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="e8d76-p105">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="e8d76-122">Pour exécuter l'action **DéfinirCatégoriesAffichées** dans un module VBA, utilisez la méthode **SetDisplayedCategories** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="e8d76-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

