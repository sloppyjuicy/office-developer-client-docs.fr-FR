---
title: DeleteObject, action de macro
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dae5718e7b4cb609cb50bd65ee6e2486f4ebaab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700093"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="65839-102">DeleteObject, action de macro</span><span class="sxs-lookup"><span data-stu-id="65839-102">DeleteObject macro action</span></span>

<span data-ttu-id="65839-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="65839-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="65839-104">Utilisez l'action **SupprimerObjet** pour supprimer un objet de base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="65839-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="65839-105">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="65839-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="65839-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="65839-106">Setting</span></span>

<span data-ttu-id="65839-107">L'action **SupprimerObjet** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="65839-107">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="65839-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="65839-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="65839-109">Description</span><span class="sxs-lookup"><span data-stu-id="65839-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="65839-110"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="65839-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="65839-p101">Type d’objet à supprimer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong> dans la zone <strong>Type d’objet</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Pour supprimer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="65839-p101">The type of object to delete. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="65839-114"><strong>Nom de l'objet</strong></span><span class="sxs-lookup"><span data-stu-id="65839-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="65839-115">Nom de l’objet à supprimer.</span><span class="sxs-lookup"><span data-stu-id="65839-115">The name of the object to delete.</span></span> <span data-ttu-id="65839-116">La zone <strong>Nom de l'objet</strong> regroupe tous les objets de la base de données ayant le type sélectionné par l'argument <strong>Type d'objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="65839-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="65839-117">Si vous laissez la zone <strong>Type d’objet</strong> vide, laissez cette zone vide également.</span><span class="sxs-lookup"><span data-stu-id="65839-117">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="65839-118">Si vous exécutez une macro contenant l’action <strong>SupprimerObjet</strong> dans une base de données bibliothèque, Microsoft Office Access 2007 commence par rechercher un objet portant ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="65839-118">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> <span data-ttu-id="65839-119">[!ATTENTION] Si vous laissez les zones **Type d'objet** et **Nom de l'objet** vides, Access supprime l'objet sélectionné dans le volet de navigation sans afficher de message d'avertissement lorsqu'il rencontre l'action **SupprimerObjet**.</span><span class="sxs-lookup"><span data-stu-id="65839-119">If you leave the **Object Type** and **Object Name** boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the **DeleteObject** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="65839-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="65839-120">Remarks</span></span>

<span data-ttu-id="65839-p103">Vous pouvez utiliser l'action **SupprimerObjet** pour supprimer des objets temporaires créés pendant l'exécution de la macro. Par exemple, vous pouvez être amené à utiliser l'action **OuvrirRequête** pour exécuter une requête Création de table qui crée une table temporaire. Lorsque vous avez terminé d'utiliser la table temporaire, vous pouvez utiliser l'action **SupprimerObjet** pour la supprimer.</span><span class="sxs-lookup"><span data-stu-id="65839-p103">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro. For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table. When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="65839-124">Cette action équivaut à sélectionner un objet dans le volet de navigation, puis à appuyer sur la touche Suppr ou encore, à cliquer avec le bouton droit sur l'objet dans le volet de navigation, puis à cliquer sur **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="65839-124">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="65839-125">Pour exécuter l'action **SupprimerObjet** dans un module Visual Basic pour Applications, vous pouvez utiliser la méthode **DeleteObject** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="65839-125">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

