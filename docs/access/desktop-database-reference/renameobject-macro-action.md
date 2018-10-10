---
title: RenommerObjet, action de macro
TOCTitle: RenameObject Macro Action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6522e85aa0407800ea0aade039a65c79a25c1419
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470142"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="18c91-102">RenommerObjet, action de macro</span><span class="sxs-lookup"><span data-stu-id="18c91-102">RenameObject Macro Action</span></span>


<span data-ttu-id="18c91-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="18c91-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="18c91-104">Vous pouvez utiliser l'action **RenommerObjet** pour renommer un objet de base de données spécifique.</span><span class="sxs-lookup"><span data-stu-id="18c91-104">You can use the **RenameObject** action to rename a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="18c91-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="18c91-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="18c91-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="18c91-107">Setting</span></span>

<span data-ttu-id="18c91-108">L'action **RenommerObjet** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="18c91-108">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18c91-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="18c91-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="18c91-110">Description</span><span class="sxs-lookup"><span data-stu-id="18c91-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18c91-111"><strong>Nouveau nom</strong></span><span class="sxs-lookup"><span data-stu-id="18c91-111"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="18c91-p102">Nouveau nom pour l’objet de base de données. Entrez le nom de l’objet dans la zone <strong>Nouveau nom</strong> de la section <strong>Arguments de l’action</strong> dans le volet Générateur de macro. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="18c91-p102">A new name for the database object. Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18c91-115"><strong>Type d'objet</strong></span><span class="sxs-lookup"><span data-stu-id="18c91-115"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="18c91-p103">Type d’objet que vous voulez renommer. Cliquez sur <strong>Table</strong>, <strong>Requête</strong>, <strong>Formulaire</strong>, <strong>État</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Page d’accès aux données</strong>, <strong>Vue serveur</strong>, <strong>Schéma</strong>, <strong>Procédure stockée</strong> ou <strong>Fonction</strong>. Pour renommer l’objet sélectionné dans le volet de navigation, laissez cet argument vide.</span><span class="sxs-lookup"><span data-stu-id="18c91-p103">The type of object you want to rename. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>. To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18c91-119"><strong>Ancien nom</strong></span><span class="sxs-lookup"><span data-stu-id="18c91-119"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="18c91-p104">Nom de l’objet à renommer. La zone <strong>Ancien nom</strong> affiche tous les objets dans la base de données dont le type correspond à celui sélectionné par l’argument <strong>Type d’objet</strong>. Si vous laissez l’argument <strong>Type d’objet</strong> vide, laissez cet argument également vide. 

</span><span class="sxs-lookup"><span data-stu-id="18c91-p104">The name of the object to be renamed. The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument. If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="18c91-123">Si vous exécutez une macro contenant l’action <STRONG>Renommer</STRONG> dans une base de données bibliothèque, Microsoft Access recherche d’abord l’objet de ce nom dans la base de données bibliothèque, puis dans la base de données active.</span><span class="sxs-lookup"><span data-stu-id="18c91-123">If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="18c91-124">Notes</span><span class="sxs-lookup"><span data-stu-id="18c91-124">Remarks</span></span>

<span data-ttu-id="18c91-125">Le nouveau nom de l'objet de base de données doit respecter les conventions d'appellation standard pour les objets Access.</span><span class="sxs-lookup"><span data-stu-id="18c91-125">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="18c91-126">Vous ne pouvez pas renommer un objet ouvert.</span><span class="sxs-lookup"><span data-stu-id="18c91-126">You can't rename an open object.</span></span>

<span data-ttu-id="18c91-p105">Si vous laissez les arguments **Type d'objet** et **Ancien nom** vides, Access renomme l'objet sélectionné dans le volet de navigation. Pour sélectionner un objet dans le volet de navigation, vous pouvez utiliser l'action **SélectionnerObjet** en attribuant la valeur **Oui** à l'argument **Dans le volet de navigation**.</span><span class="sxs-lookup"><span data-stu-id="18c91-p105">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="18c91-p106">Vous pouvez également renommer un objet en cliquant avec le bouton droit sur celui-ci dans le volet de navigation, en cliquant sur **RenommerObjet** et en indiquant un nouveau nom. Avec l'action **Renommer**, vous ne devez pas d'abord sélectionner l'objet dans le volet de navigation ni arrêter la macro pour entrer le nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="18c91-p106">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name. With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="18c91-131">Cette action diffère de l'action **CopierObjet** qui crée une copie de l'objet sous un nouveau nom.</span><span class="sxs-lookup"><span data-stu-id="18c91-131">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="18c91-132">Pour exécuter l'action **RenommerObjet** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Rename** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="18c91-132">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

