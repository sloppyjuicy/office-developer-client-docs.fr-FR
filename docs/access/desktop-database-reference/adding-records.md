---
title: Ajout d'enregistrements (référence de base de données de bureau Access)
TOCTitle: Adding records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 268cd381cdeef11f2a6f351160d930e4b169cfbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280286"
---
# <a name="adding-records"></a><span data-ttu-id="d1b55-102">Ajout d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="d1b55-102">Adding records</span></span>

<span data-ttu-id="d1b55-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1b55-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1b55-p101">Utilisez la méthode **AddNew** pour créer et initialiser un nouvel enregistrement dans un objet **Recordset** existant. Vous pouvez utiliser la méthode **Supports** avec **CursorOptionEnum** affecté de la valeur **adAddNew** pour vérifier si vous pouvez ajouter des enregistrements à l'objet **Recordset** actif.</span><span class="sxs-lookup"><span data-stu-id="d1b55-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="d1b55-p102">Après l'appel de la méthode **AddNew**, le nouvel enregistrement devient l'enregistrement actif et il le reste après l'appel de la méthode **Update**. Si l'objet **Recordset** ne prend pas en charge les signets, vous risquez de ne pas pouvoir accéder au nouvel enregistrement si vous passez à un autre. C'est pourquoi, en fonction du type de curseur, vous devrez peut-être appeler la méthode **Requery** pour rendre le nouvel enregistrement accessible.</span><span class="sxs-lookup"><span data-stu-id="d1b55-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="d1b55-109">Si vous appelez **AddNew** alors que vous modifiez l'enregistrement actif ou que vous en ajoutez un nouveau, ADO appelle la méthode **Update** pour enregistrer toute modification avant de créer le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d1b55-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="d1b55-110">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d1b55-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="d1b55-111">Ajout de plusieurs champs</span><span class="sxs-lookup"><span data-stu-id="d1b55-111">Adding multiple fields</span></span>](adding-multiple-fields.md)
- [<span data-ttu-id="d1b55-112">Détermination du mode d'édition</span><span class="sxs-lookup"><span data-stu-id="d1b55-112">Determining Edit mode</span></span>](determining-edit-mode.md)
- [<span data-ttu-id="d1b55-113">Utilisation de AddNew dans les modes immédiat et batch</span><span class="sxs-lookup"><span data-stu-id="d1b55-113">Using AddNew in Immediate and Batch modes</span></span>](using-addnew-in-immediate-and-batch-modes.md)

