---
title: Refresh, méthode (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309255"
---
# <a name="refresh-method-ado"></a><span data-ttu-id="b4ea0-102">Refresh, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4ea0-102">Refresh method (ADO)</span></span>

<span data-ttu-id="b4ea0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4ea0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4ea0-104">Met à jour les objets d’une collection pour qu’ils reflètent les objets disponibles ou spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-104">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4ea0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4ea0-105">Syntax</span></span>

<span data-ttu-id="b4ea0-106">*.* Actualiser</span><span class="sxs-lookup"><span data-stu-id="b4ea0-106">*collection*.Refresh</span></span>

## <a name="remarks"></a><span data-ttu-id="b4ea0-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4ea0-107">Remarks</span></span>

<span data-ttu-id="b4ea0-108">La méthode **Refresh** exécute différentes tâches selon la collection à partir de laquelle vous l'appelez.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-108">The **Refresh** method accomplishes different tasks depending on the collection from which you call it.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4ea0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4ea0-109">Parameters</span></span>

<span data-ttu-id="b4ea0-p101">Lorsque vous appliquez la méthode **Refresh** à la collection [Parameters](command-object-ado.md) d'un objet [Command](parameters-collection-ado.md), des informations de paramètres côté fournisseur sont extraites pour la procédure stockée ou la requête paramétrée spécifiée dans l'objet **Command**. La collection est vide pour les fournisseurs qui ne prennent pas en charge les appels de procédure stockée et les requêtes paramétrées.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-p101">Using the **Refresh** method on a [Command](command-object-ado.md) object's [Parameters](parameters-collection-ado.md) collection retrieves provider-side parameter information for the stored procedure or parameterized query specified in the **Command** object. The collection will be empty for providers that do not support stored procedure calls or parameterized queries.</span></span>

<span data-ttu-id="b4ea0-112">Affectez un objet [Connection](activeconnection-property-ado.md) valide à la propriété **ActiveConnection** de l'objet [Command](connection-object-ado.md), une commande valide à la propriété [CommandText](commandtext-property-ado.md) et la valeur [adCmdStoredProc](commandtype-property-ado.md) à la propriété **CommandType** avant d'appeler la méthode **Refresh**.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-112">You should set the [ActiveConnection](activeconnection-property-ado.md) property of the **Command** object to a valid [Connection](connection-object-ado.md) object, the [CommandText](commandtext-property-ado.md) property to a valid command, and the [CommandType](commandtype-property-ado.md) property to **adCmdStoredProc** before calling the **Refresh** method.</span></span>

<span data-ttu-id="b4ea0-113">Si vous accédez à la collection **Parameters** avant d'appeler la méthode **Refresh**, ADO appelle automatiquement cette méthode et remplit la collection.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-113">If you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

> [!NOTE]
> <span data-ttu-id="b4ea0-p102">[!REMARQUE] Si vous utilisez la méthode **Refresh** pour obtenir des paramètres du fournisseur et que cette méthode retourne un ou plusieurs objets [Parameter](parameter-object-ado.md) qui possèdent un type de données de longueur variable, ADO peut allouer de la mémoire à ces paramètres en fonction de leur taille maximale potentielle, ce qui entraîne une erreur lors de l'exécution. Pour éviter ces erreurs, vous devez définir explicitement la propriété [Size](size-property-ado.md) de ces paramètres avant d'appeler la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="b4ea0-p102">If you use the **Refresh** method to obtain parameter information from the provider and it returns one or more variable-length data type [Parameter](parameter-object-ado.md) objects, ADO may allocate memory for the parameters based on their maximum potential size, which will cause an error during execution. You should explicitly set the [Size](size-property-ado.md) property for these parameters before calling the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method to prevent errors.</span></span>

### <a name="fields"></a><span data-ttu-id="b4ea0-116">Champs</span><span class="sxs-lookup"><span data-stu-id="b4ea0-116">Fields</span></span>

<span data-ttu-id="b4ea0-p103">L'application de la méthode **Refresh** à la collection **Fields** ne produit aucun effet visible. Pour extraire des modifications de la structure de base de données sous-jacente , vous devez utiliser la méthode [Requery](requery-method-ado.md) ou, si l'objet [Recordset](recordset-object-ado.md) ne prend pas en charge les signets, la méthode [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b4ea0-p103">Using the **Refresh** method on the **Fields** collection has no visible effect. To retrieve changes from the underlying database structure, you must use either the [Requery](requery-method-ado.md) method or, if the [Recordset](recordset-object-ado.md) object does not support bookmarks, the [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) method.</span></span>

### <a name="properties"></a><span data-ttu-id="b4ea0-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4ea0-119">Properties</span></span>

<span data-ttu-id="b4ea0-p104">L'application de la méthode **Refresh** à la collection **Properties** de certains objets remplit cette collection de propriétés dynamiques exposées par le fournisseur. Ces propriétés fournissent des informations sur les fonctionnalités propres au fournisseur, au-delà des propriétés intégrées prises en charge par ADO.</span><span class="sxs-lookup"><span data-stu-id="b4ea0-p104">Using the **Refresh** method on a **Properties** collection of some objects populates the collection with the dynamic properties that the provider exposes. These properties provide information about functionality specific to the provider, beyond the built-in properties ADO supports.</span></span>

