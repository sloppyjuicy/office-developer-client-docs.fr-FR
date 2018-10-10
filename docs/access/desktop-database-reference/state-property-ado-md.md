---
title: State, propriété (ADO MD)
TOCTitle: State Property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a42ade39a50eb5dc40e213d6f4c3f4ed0ba3475e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470562"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="2bc20-102">State, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2bc20-102">State Property (ADO MD)</span></span>


<span data-ttu-id="2bc20-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2bc20-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2bc20-104">Indique l'état actuel de l'ensemble de cellules.</span><span class="sxs-lookup"><span data-stu-id="2bc20-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="2bc20-105">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2bc20-105">Return Values</span></span>

<span data-ttu-id="2bc20-p101">Retourne un entier de type **Long** qui indique la condition actuelle de l'objet [Cellset](cellset-object-ado-md.md) et est en lecture seule. Les valeurs suivantes sont valides : **adStateClosed** (0) et **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="2bc20-p101">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only. The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="2bc20-108">Notes</span><span class="sxs-lookup"><span data-stu-id="2bc20-108">Remarks</span></span>

<span data-ttu-id="2bc20-p102">Pour utiliser les noms des constantes [ObjectStateEnum](objectstateenum.md) la bibliothèque de types ADO doit être référencée dans votre projet. Pour plus d'informations, consultez [Utilisation d'ADO avec ADO MD](using-ado-with-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="2bc20-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

