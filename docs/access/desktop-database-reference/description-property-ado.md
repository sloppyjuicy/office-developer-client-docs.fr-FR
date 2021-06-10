---
title: Description, propriété (ADO)
TOCTitle: Description property (ADO)
ms:assetid: 31df5e36-641c-d213-31fc-6244e2983327
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249092(v=office.15)
ms:contentKeyID: 48544064
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba6d05aa1bfb626520af60a30279983bae6fa566
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293930"
---
# <a name="description-property-ado"></a><span data-ttu-id="94da2-102">Description, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="94da2-102">Description property (ADO)</span></span>


<span data-ttu-id="94da2-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94da2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94da2-104">Décrit un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="94da2-104">Describes an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="94da2-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="94da2-105">Return value</span></span>

<span data-ttu-id="94da2-106">Renvoie une valeur de type **String** qui contient une description de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="94da2-106">Returns a **String** value that contains a description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="94da2-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="94da2-107">Remarks</span></span>

<span data-ttu-id="94da2-p101">Utilisez la propriété **Description** pour obtenir une courte description de l'erreur. Affichez cette propriété pour avertir l'utilisateur d'une erreur que vous ne pouvez pas ou ne souhaitez pas gérer. La chaîne provient d'ADO ou d'un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94da2-p101">Use the **Description** property to obtain a short description of the error. Display this property to alert the user to an error that you cannot or do not want to handle. The string will come from either ADO or a provider.</span></span>

<span data-ttu-id="94da2-p102">Les fournisseurs sont chargés de transmettre un texte d'erreur spécifique à ADO. ADO ajoute un objet [Error](error-object-ado.md) à la collection **Errors** pour chaque erreur ou avertissement de fournisseur reçu. Énumérez la collection **Errors** pour identifier les erreurs transmises par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94da2-p102">Providers are responsible for passing specific error text to ADO. ADO adds an [Error](error-object-ado.md) object to the **Errors** collection for each provider error or warning it receives. Enumerate the **Errors** collection to trace the errors that the provider passes.</span></span>

