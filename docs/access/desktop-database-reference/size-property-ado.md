---
title: Size, propriété (ADO)
TOCTitle: Size property (ADO)
ms:assetid: 24596b5c-b1cc-e97e-68b6-8ff53baf150b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249017(v=office.15)
ms:contentKeyID: 48543753
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2a1bed3454d081b9d5de3a01e9b326130b40baa4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306929"
---
# <a name="size-property-ado"></a><span data-ttu-id="f323e-102">Size, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="f323e-102">Size property (ADO)</span></span>


<span data-ttu-id="f323e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f323e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f323e-104">Indique la taille maximale, en octets ou en caractères, d'un objet [Parameter](parameter-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f323e-104">Indicates the maximum size, in bytes or characters, of a [Parameter](parameter-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f323e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="f323e-105">Settings and return values</span></span>

<span data-ttu-id="f323e-106">Définit ou retourne une valeur de type **Long** qui indique la taille maximale, en octets ou en caractères, d'une valeur dans un objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="f323e-106">Sets or returns a **Long** value that indicates the maximum size in bytes or characters of a value in a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f323e-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="f323e-107">Remarks</span></span>

<span data-ttu-id="f323e-108">Utilisez la propriété **Size** pour déterminer la taille maximale des valeurs devant être écrites ou lues dans la propriété [Value](value-property-ado.md) d’un objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="f323e-108">Use the **Size** property to determine the maximum size for values written to or read from the [Value](value-property-ado.md) property of a **Parameter** object.</span></span>

<span data-ttu-id="f323e-109">Si vous spécifiez un type de données de longueur variable pour un objet **Parameter** (par exemple tout type de **String**, comme **adVarChar**), vous devez définir la propriété **Size** de l’objet avant de l’ajouter à la collection [Parameters](parameters-collection-ado.md) ; sinon, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="f323e-109">If you specify a variable-length data type for a **Parameter** object (for example, any **String** type, such as **adVarChar**), you must set the object's **Size** property before appending it to the [Parameters](parameters-collection-ado.md) collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="f323e-110">Si vous avez déjà ajouté l'objet **Parameter** à la collection **Parameters** d'un objet [Command](command-object-ado.md) et que modifiez son type pour un type de données de longueur variable, vous devez définir la propriété **Size** de l'objet **Parameter** avant d'exécuter l'objet **Command**; sinon, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="f323e-110">If you have already appended the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object and you change its type to a variable-length data type, you must set the **Parameter** object's **Size** property before executing the **Command** object; otherwise, an error occurs.</span></span>

<span data-ttu-id="f323e-p101">Si vous utilisez la méthode [Refresh](refresh-method-ado.md) pour obtenir du fournisseur des informations sur les paramètres et qu'il renvoie des objets **Parameter** contenant un ou plusieurs types de données de longueur variable, il se peut qu'ADO alloue de la mémoire aux paramètres en fonction de leur taille potentielle maximale, ce qui risque de générer une erreur à l'exécution. Pour éviter les erreurs, définissez explicitement la propriété **Size** de ces paramètres avant d'exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="f323e-p101">If you use the [Refresh](refresh-method-ado.md) method to obtain parameter information from the provider and it returns one or more variable-length data type **Parameter** objects, ADO may allocate memory for the parameters based on their maximum potential size, which could cause an error during execution. To prevent an error, you should explicitly set the **Size** property for these parameters before executing the command.</span></span>

<span data-ttu-id="f323e-113">La propriété **Size** est en accessible lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="f323e-113">The **Size** property is read/write.</span></span>

