---
title: Parameters, collection (ADO)
TOCTitle: Parameters collection (ADO)
ms:assetid: 554387c3-3572-5391-3b24-c7d3443844cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249283(v=office.15)
ms:contentKeyID: 48544923
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: feb24e0f498e02bae01ef689a2ad62e487e314bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287943"
---
# <a name="parameters-collection-ado"></a><span data-ttu-id="cceb0-102">Parameters, collection (ADO)</span><span class="sxs-lookup"><span data-stu-id="cceb0-102">Parameters collection (ADO)</span></span>


<span data-ttu-id="cceb0-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cceb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cceb0-104">Contient tous les objets [Parameter](parameter-object-ado.md) d’un objet [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="cceb0-104">Contains all the [Parameter](parameter-object-ado.md) objects of a [Command](command-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cceb0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="cceb0-105">Remarks</span></span>

<span data-ttu-id="cceb0-106">Un objet **Command** possède une collection **Parameters** composée d'objets **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="cceb0-106">A **Command** object has a **Parameters** collection made up of **Parameter** objects.</span></span>

<span data-ttu-id="cceb0-p101">L'utilisation de la méthode [Refresh](refresh-method-ado.md) sur une collection **Parameters** de l'objet **Command** récupère les informations des paramètres du fournisseur pour la procédure stockée ou la requête paramétrée spécifiée dans l'objet **Command**. Certains fournisseurs ne prennent pas en charge les appels de procédure stockée ou les requêtes paramétrées ; si vous appelez la méthode **Refresh** sur la collection **Parameters** avec ce type de fournisseur, vous obtenez une erreur.</span><span class="sxs-lookup"><span data-stu-id="cceb0-p101">Using the [Refresh](refresh-method-ado.md) method on a **Command** object's **Parameters** collection retrieves provider parameter information for the stored procedure or parameterized query specified in the **Command** object. Some providers do not support stored procedure calls or parameterized queries; calling the **Refresh** method on the **Parameters** collection when using such a provider will return an error.</span></span>

<span data-ttu-id="cceb0-109">Si vous n'avez pas défini vos propres objets **Parameter** et que vous accédez à la collection **Parameters** avant d'appeler la méthode **Refresh**, ADO appelle automatiquement la méthode et remplit la collection à votre place.</span><span class="sxs-lookup"><span data-stu-id="cceb0-109">If you have not defined your own **Parameter** objects and you access the **Parameters** collection before calling the **Refresh** method, ADO will automatically call the method and populate the collection for you.</span></span>

<span data-ttu-id="cceb0-p102">Si vous connaissez les propriétés des paramètres associés à la procédure stockée ou à la requête paramétrée que vous voulez appeler, vous pouvez minimiser les appels au fournisseur pour accroître les performances. Utilisez la méthode [CreateParameter](createparameter-method-ado.md) pour créer des objets **Parameter** avec les paramètres de propriété appropriés et utilisez la méthode [Append](append-method-ado.md) pour les ajouter à la collection **Parameters**. Cela vous permet de définir et de renvoyer des valeurs de paramètre sans appeler le fournisseur afin qu'il fournisse les informations de paramètre. Si vous écrivez du code pour un fournisseur qui ne fournit pas d'informations de paramètre, vous devez remplir manuellement la collection **Parameters** à l'aide de cette méthode pour pouvoir utiliser des paramètres. Utilisez la méthode [Delete](delete-method-ado-parameters-collection.md) pour supprimer les objets **Parameter** de la collection **Parameters** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="cceb0-p102">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call. Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the [Append](append-method-ado.md) method to add them to the **Parameters** collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must manually populate the **Parameters** collection using this method to be able to use parameters at all. Use the [Delete](delete-method-ado-parameters-collection.md) method to remove **Parameter** objects from the **Parameters** collection if necessary.</span></span>

<span data-ttu-id="cceb0-115">Les objets de la collection **Parameters** d'un objet **Recordset** sont hors de portée (ils deviennent donc indisponibles) lorsque cet objet **Recordset** est fermé.</span><span class="sxs-lookup"><span data-stu-id="cceb0-115">The objects in the **Parameters** collection of a **Recordset** go out of scope (therefore becoming unavailable) when the **Recordset** is closed.</span></span>

