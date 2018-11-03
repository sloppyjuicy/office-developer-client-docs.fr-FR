---
title: Utilisation de la méthode AddNew en mode de mise à jour immédiate et par lot
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79bd4ed656da49e61ea70ace3b11f09c19382b03
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943639"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="71ac6-102">Avec la méthode AddNew en mode exécution et par lot</span><span class="sxs-lookup"><span data-stu-id="71ac6-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="71ac6-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71ac6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71ac6-104">Le comportement de la méthode **AddNew** varie selon le mode de mise à jour de l’objet **Recordset** et selon que vous passez les arguments *FieldList* et *Values* .</span><span class="sxs-lookup"><span data-stu-id="71ac6-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="71ac6-p101">En mode de mise à jour immédiate (où le fournisseur écrit les modifications dans la source de données sous-jacente dès que vous appelez la méthode **Update**), l'appel de la méthode **AddNew** sans argument affecte à la propriété **EditMode** la valeur **adEditAdd.** Le fournisseur met toutes les modifications des valeurs de champ dans un cache local. L'appel de la méthode **Update** publie le nouvel enregistrement dans la base de données et modifie la propriété **EditMode** en lui affectant la valeur **adEditNone**. Si vous passez les arguments *FieldList* et *Values*, ADO publie immédiatement le nouvel enregistrement dans la base de données (il n'est pas nécessaire d'appeler **Update**) et la valeur de la propriété **EditMode** ne change pas (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="71ac6-p101">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.** The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**. If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="71ac6-109">En mode de mise à jour par lot, l’appel de la méthode **AddNew** sans arguments définit la propriété **EditMode** à **adEditAdd**.</span><span class="sxs-lookup"><span data-stu-id="71ac6-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="71ac6-110">Le fournisseur met en cache toutes les modifications locales de valeurs de champ.</span><span class="sxs-lookup"><span data-stu-id="71ac6-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="71ac6-111">Appeler la méthode **Update** ajoute le nouvel enregistrement au **Recordset** actif et réinitialise la propriété **EditMode** à **adEditNone**, mais le fournisseur ne valide pas les modifications apportées à la base de données sous-jacente que lorsque vous appelez la méthode UpdateBatch \*\* \*\*méthode.</span><span class="sxs-lookup"><span data-stu-id="71ac6-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="71ac6-112">Si vous passez des arguments *FieldList* et *Values* , ADO envoie le nouvel enregistrement au fournisseur pour le stockage dans un cache ; Vous devez appeler la méthode **UpdateBatch** pour publier le nouvel enregistrement dans la base de données sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="71ac6-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="71ac6-113">Pour plus d’informations sur la **mise à jour** et **UpdateBatch**, voir [chapitre 5 : mise à jour et persistance des données](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="71ac6-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

