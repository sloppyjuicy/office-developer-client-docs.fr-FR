---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471960"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="0be86-102">ActiveCommand, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="0be86-102">ActiveCommand Property (ADO)</span></span>


<span data-ttu-id="0be86-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0be86-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0be86-104">Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.</span><span class="sxs-lookup"><span data-stu-id="0be86-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="0be86-105">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0be86-105">Return Value</span></span>

<span data-ttu-id="0be86-p101">Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.</span><span class="sxs-lookup"><span data-stu-id="0be86-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="0be86-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0be86-108">Remarks</span></span>

<span data-ttu-id="0be86-109">La propriété **ActiveCommand** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0be86-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="0be86-110">Si un objet **Command** n'a pas été utilisé pour créer l'objet **Recordset** actif, une référence d'objet **Null** est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="0be86-110">If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>

<span data-ttu-id="0be86-111">Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="0be86-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

