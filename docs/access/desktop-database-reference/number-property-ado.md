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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707469"
---
# <a name="number-property-ado"></a><span data-ttu-id="1c13c-102">Number, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1c13c-102">Number property (ADO)</span></span>


<span data-ttu-id="1c13c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c13c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1c13c-104">Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1c13c-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c13c-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1c13c-105">Return value</span></span>

<span data-ttu-id="1c13c-106">Renvoie une valeur de type **Long** pouvant correspondre à l'une des constantes [ErrorValueEnum](errorvalueenum.md).</span><span class="sxs-lookup"><span data-stu-id="1c13c-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c13c-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c13c-107">Remarks</span></span>

<span data-ttu-id="1c13c-p101">Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.</span><span class="sxs-lookup"><span data-stu-id="1c13c-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="1c13c-110">La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple).</span><span class="sxs-lookup"><span data-stu-id="1c13c-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="1c13c-111">Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE.</span><span class="sxs-lookup"><span data-stu-id="1c13c-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="1c13c-112">Pour plus d’informations sur ces numéros, consultez le chapitre 16 de la *de référence du programmeur OLE DB.*</span><span class="sxs-lookup"><span data-stu-id="1c13c-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

