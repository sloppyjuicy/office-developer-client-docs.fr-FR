---
title: Ajout d’enregistrements (référence de base de données du bureau Access)
TOCTitle: Adding Records
ms:assetid: 7a5b27bc-7b28-4f43-b55e-a21edfb9e1b3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249505(v=office.15)
ms:contentKeyID: 48545791
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bfa1503e7f7b874136ab5aee70721a3b9cf3463b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472038"
---
# <a name="adding-records"></a><span data-ttu-id="5942b-102">Ajout d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5942b-102">Adding Records</span></span>


<span data-ttu-id="5942b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5942b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5942b-p101">Utilisez la méthode **AddNew** pour créer et initialiser un nouvel enregistrement dans un objet **Recordset** existant. Vous pouvez utiliser la méthode **Supports** avec **CursorOptionEnum** affecté de la valeur **adAddNew** pour vérifier si vous pouvez ajouter des enregistrements à l'objet **Recordset** actif.</span><span class="sxs-lookup"><span data-stu-id="5942b-p101">Use the **AddNew** method to create and initialize a new record in an existing **Recordset**. You can use the **Supports** method with a **CursorOptionEnum** value of **adAddNew** to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="5942b-p102">Après l'appel de la méthode **AddNew**, le nouvel enregistrement devient l'enregistrement actif et il le reste après l'appel de la méthode **Update**. Si l'objet **Recordset** ne prend pas en charge les signets, vous risquez de ne pas pouvoir accéder au nouvel enregistrement si vous passez à un autre. C'est pourquoi, en fonction du type de curseur, vous devrez peut-être appeler la méthode **Requery** pour rendre le nouvel enregistrement accessible.</span><span class="sxs-lookup"><span data-stu-id="5942b-p102">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the **Update** method. If the **Recordset** object does not support bookmarks, you might not be able to access the new record once you move to another record. Therefore, depending on your cursor type, you might need to call the **Requery** method to make the new record accessible.</span></span>

<span data-ttu-id="5942b-109">Si vous appelez **AddNew** alors que vous modifiez l'enregistrement actif ou que vous en ajoutez un nouveau, ADO appelle la méthode **Update** pour enregistrer toute modification avant de créer le nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="5942b-109">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

