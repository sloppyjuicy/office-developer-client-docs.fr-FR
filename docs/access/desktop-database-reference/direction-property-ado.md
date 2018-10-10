---
title: Direction, propriété (ADO)
TOCTitle: Direction Property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611e5efbe53964c5ba255380e2659f024bd6be9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471061"
---
# <a name="direction-property-ado"></a><span data-ttu-id="b424c-102">Direction, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="b424c-102">Direction Property (ADO)</span></span>


<span data-ttu-id="b424c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b424c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b424c-104">Indique si l'objet [Parameter](parameter-object-ado.md) représente un paramètre d'entrée, de sortie, d'entrée et de sortie, ou encore si le paramètre est la valeur renvoyée par une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="b424c-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b424c-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="b424c-105">Settings and Return Values</span></span>

<span data-ttu-id="b424c-106">Définit ou renvoie une valeur [ParameterDirectionEnum](parameterdirectionenum.md).</span><span class="sxs-lookup"><span data-stu-id="b424c-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b424c-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b424c-107">Remarks</span></span>

<span data-ttu-id="b424c-p101">Utilisez la propriété **Direction** pour spécifier le mode de transmission d'un paramètre dans une procédure. La propriété **Direction** est en lecture-écriture, ce qui vous permet d'utiliser des fournisseurs qui ne retournent pas ces informations ou de définir ces informations lorsque vous ne souhaitez pas qu'ADO effectue un appel supplémentaire au fournisseur pour récupérer des informations de paramètre.</span><span class="sxs-lookup"><span data-stu-id="b424c-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="b424c-p102">Les fournisseurs ne peuvent pas tous déterminer la direction des paramètres dans leurs procédures stockées. En pareil cas, vous devez définir la propriété **Direction** avant d'exécuter la requête.</span><span class="sxs-lookup"><span data-stu-id="b424c-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

