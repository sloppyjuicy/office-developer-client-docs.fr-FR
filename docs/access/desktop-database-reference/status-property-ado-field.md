---
title: Status, propriété (champ ADO)
TOCTitle: Status property (ADO Field)
ms:assetid: 7a7b45e8-2934-2e8e-77fa-a4f38272548d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249507(v=office.15)
ms:contentKeyID: 48545795
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9c5f9d73a1081bb27c88541ac99307165222ab65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306320"
---
# <a name="status-property-ado-field"></a><span data-ttu-id="33c0d-102">Status, propriété (champ ADO)</span><span class="sxs-lookup"><span data-stu-id="33c0d-102">Status property (ADO Field)</span></span>


<span data-ttu-id="33c0d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="33c0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="33c0d-104">Indique l'état d'un objet [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="33c0d-104">Indicates the status of a [Field](field-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="33c0d-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33c0d-105">Return value</span></span>

<span data-ttu-id="33c0d-106">Renvoie une valeur [FieldStatusEnum](fieldstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="33c0d-106">Returns a [FieldStatusEnum](fieldstatusenum.md) value.</span></span> <span data-ttu-id="33c0d-107">La valeur par défaut est **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="33c0d-107">The default value is **adFieldOK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="33c0d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="33c0d-108">Remarks</span></span>

<span data-ttu-id="33c0d-109">Cette propriété renvoie toujours **adFieldOK** pour les champs d’un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="33c0d-109">This property always returns **adFieldOK** for fields of a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="33c0d-p102">Les additions et les suppressions effectuées sur les collections [Fields](fields-collection-ado.md) de l'objet [Record](record-object-ado.md) sont mises en cache jusqu'à ce que la méthode [Update](update-method-ado.md) soit appelée. La propriété **Status** vous permet de déterminer les champs ayant été correctement ajoutés ou supprimés.</span><span class="sxs-lookup"><span data-stu-id="33c0d-p102">Additions and deletions to the [Fields](fields-collection-ado.md) collections of the [Record](record-object-ado.md) object are cached until the [Update](update-method-ado.md) method is called. The **Status** property enables you to determine which fields have been successfully added or deleted.</span></span>

<span data-ttu-id="33c0d-112">Pour améliorer les performances, les modifications de schéma sont mises en cache jusqu’à ce que **la** mise à jour soit appelée, puis les modifications sont apportées dans une mise à jour par lot optimiste.</span><span class="sxs-lookup"><span data-stu-id="33c0d-112">To enhance performance, schema changes are cached until **Update** is called, and then the changes are made in a batch optimistic update.</span></span> <span data-ttu-id="33c0d-113">Si la **méthode Update** n’est pas appelée, le serveur n’est pas mis à jour.</span><span class="sxs-lookup"><span data-stu-id="33c0d-113">If the **Update** method is not called, the server is not updated.</span></span> <span data-ttu-id="33c0d-114">Si des mises à jour échouent, une erreur est renvoyée et la propriété **Status** indique les valeurs combinées du code d’état d’opération et d’erreur.</span><span class="sxs-lookup"><span data-stu-id="33c0d-114">If any updates fail then an error is returned and the **Status** property indicates the combined values of the operation and error status code.</span></span> <span data-ttu-id="33c0d-115">Par exemple, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span><span class="sxs-lookup"><span data-stu-id="33c0d-115">For example, **adFieldPendingInsert** **OR** **adFieldPermissionDenied**.</span></span> <span data-ttu-id="33c0d-116">La **propriété Status** de chaque **champ** peut  être utilisée pour déterminer pourquoi le champ n’a pas été ajouté, modifié ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="33c0d-116">The **Status** property for each **Field** can be used to determine why the **Field** was not added, modified, or deleted.</span></span> <span data-ttu-id="33c0d-117">**L’état** est uniquement exposé de manière significative sur **l’enregistrement**. **Fields,** collection et non **recordset**. **Fields,** collection.</span><span class="sxs-lookup"><span data-stu-id="33c0d-117">**Status** is only meaningfully exposed on the **Record**.**Fields** collection and not the **Recordset**.**Fields** collection.</span></span>

<span data-ttu-id="33c0d-p104">Deux problèmes peuvent survenir lors de l'ajout, de la modification ou de la suppression d'un objet **Field**. Si l'utilisateur supprime un objet **Field**, il est marqué pour suppression dans la collection **Fields**. Si l'appel suivant de la méthode **Update** renvoie une erreur parce que l'utilisateur a tenté de supprimer un objet **Field** sur lequel il n'avait pas les autorisations nécessaires, l'objet **Field** aura pour état **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Le fait d'appeler la méthode [CancelUpdate](cancelupdate-method-ado.md) restaure les valeurs d'origine et donne à la propriété **Status** la valeur **adFieldOK**. De même, la méthode **Update** peut renvoyer une erreur lorsqu'un nouvel objet **Field** a été ajouté et que la valeur qui lui a été attribuée est incorrecte. Dans ce cas, le nouvel objet **Field** est stocké dans la collection **Fields**; prend l'état **adFieldPendingInsert**, voire **adFieldCantCreate**. Vous pouvez donner au nouvel objet **Field** une valeur correcte et appeler à nouveau la méthode **Update**. Remarque : si vous appelez **Resync**, une requête est renvoyée au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="33c0d-p104">Two problems can arise when adding, modifying, or deleting a **Field**. If the user deletes a **Field**, it is marked for deletion from the **Fields** collection. If the subsequent **Update** returns an error because the user tried to delete a **Field** for which they do not have permission, the **Field** will have a status of **adFieldPermissionDenied** **OR** **adFieldPendingDelete**. Calling the [CancelUpdate](cancelupdate-method-ado.md) method restores original values and sets the **Status** to **adFieldOK**. Similarly, the **Update** method may return an error because a new **Field** was added and given an inappropriate value. In that case the new **Field** will be in the **Fields** collection and have a status of **adFieldPendingInsert** and perhaps **adFieldCantCreate**. You can supply an appropriate value for the new **Field** and call **Update** again. Note that calling **Resync** instead requeries the provider.</span></span>

