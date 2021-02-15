---
title: RenameObject, action de macro
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306719"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="01990-102">RenameObject, action de macro</span><span class="sxs-lookup"><span data-stu-id="01990-102">RenameObject macro action</span></span>

<span data-ttu-id="01990-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="01990-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01990-104">Vous pouvez utiliser l'action **RenommerObjet** pour renommer un objet de base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="01990-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="01990-105">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="01990-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="01990-106">Setting</span><span class="sxs-lookup"><span data-stu-id="01990-106">Setting</span></span>

<span data-ttu-id="01990-107">L’action **RenommerObjet** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="01990-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01990-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="01990-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="01990-109">Description</span><span class="sxs-lookup"><span data-stu-id="01990-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01990-110"><strong>Nouveau nom</strong></span><span class="sxs-lookup"><span data-stu-id="01990-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="01990-p101">Nouveau nom pour l’objet de base de données. Entrez le nom de l’objet dans la zone <strong>Nouveau nom</strong> de la section <strong>Arguments de l’action</strong> dans le volet Générateur de macro. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="01990-p101">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01990-114"><strong>Type d’objet</strong></span><span class="sxs-lookup"><span data-stu-id="01990-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="01990-p102">Type d’objet que vous voulez renommer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong>. Pour renommer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="01990-p102">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01990-118"><strong>Ancien nom</strong></span><span class="sxs-lookup"><span data-stu-id="01990-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="01990-119">Nom de l’objet à renommer.</span><span class="sxs-lookup"><span data-stu-id="01990-119">The name of the object to be renamed.</span></span> <span data-ttu-id="01990-120">La zone <strong>Ancien nom</strong> affiche tous les objets dans la base de données dont le type correspond à celui sélectionné par l’argument <strong>Type d’objet</strong>.</span><span class="sxs-lookup"><span data-stu-id="01990-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="01990-121">Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez cet argument également vide.</span><span class="sxs-lookup"><span data-stu-id="01990-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="01990-122"><strong>REMARQUE</strong>: si vous exécutez une macro contenant <STRONG>l’action</STRONG> Renommer dans une base de données bibliothèque, Microsoft Access recherche d’abord l’objet de ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.</span><span class="sxs-lookup"><span data-stu-id="01990-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="01990-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="01990-123">Remarks</span></span>

<span data-ttu-id="01990-124">Le nouveau nom de l’objet de base de données doit respecter les conventions d’appellation standard pour les objets Access.</span><span class="sxs-lookup"><span data-stu-id="01990-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="01990-125">Vous ne pouvez pas renommer un objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="01990-125">You can't rename an open object.</span></span>

<span data-ttu-id="01990-p104">Si vous laissez les arguments **Type d'objet** et **Ancien nom** vides, Access renomme l'objet sélectionné dans le volet de navigation. Pour sélectionner un objet dans le volet de navigation, vous pouvez utiliser l'action **SélectionnerObjet** en attribuant la valeur **Oui** à l'argument **Dans le volet de navigation**.</span><span class="sxs-lookup"><span data-stu-id="01990-p104">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="01990-p105">Vous pouvez également renommer un objet en cliquant avec le bouton droit sur celui-ci dans le volet de navigation, en cliquant sur **RenommerObjet** et en indiquant un nouveau nom. Avec l'action **Renommer**, vous ne devez pas d'abord sélectionner l'objet dans le volet de navigation ni arrêter la macro pour entrer le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="01990-p105">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="01990-130">Cette action diffère de l'action **CopierObjet** qui crée une copie de l'objet sous un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="01990-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="01990-131">Pour exécuter l'action **RenommerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Rename** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="01990-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

