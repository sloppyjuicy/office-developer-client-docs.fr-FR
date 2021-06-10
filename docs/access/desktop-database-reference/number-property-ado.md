---
title: Number, propriété (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288573"
---
# <a name="number-property-ado"></a><span data-ttu-id="5a6c4-102">Number, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="5a6c4-102">Number property (ADO)</span></span>


<span data-ttu-id="5a6c4-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a6c4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a6c4-104">Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="5a6c4-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a6c4-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a6c4-105">Return value</span></span>

<span data-ttu-id="5a6c4-106">Renvoie une valeur de type **Long** pouvant correspondre à l’une des constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="5a6c4-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a6c4-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="5a6c4-107">Remarks</span></span>

<span data-ttu-id="5a6c4-p101">Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.</span><span class="sxs-lookup"><span data-stu-id="5a6c4-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="5a6c4-p102">La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple). Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE. Pour plus d’informations sur ces chiffres, consultez le chapitre 16 du guide *OLE DB Programmer’s Reference* (en anglais).</span><span class="sxs-lookup"><span data-stu-id="5a6c4-p102">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259). These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself. For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

