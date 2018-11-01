---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869560"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="75cb4-102">ActiveCommand, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="75cb4-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="75cb4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="75cb4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75cb4-104">Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.</span><span class="sxs-lookup"><span data-stu-id="75cb4-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="75cb4-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75cb4-105">Return value</span></span>

<span data-ttu-id="75cb4-p101">Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.</span><span class="sxs-lookup"><span data-stu-id="75cb4-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="75cb4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="75cb4-108">Remarks</span></span>

<span data-ttu-id="75cb4-109">La propriété **ActiveCommand** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="75cb4-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="75cb4-110">Si un objet **Command** n’était utilisé pour créer l' **objet Recordset**actif, une référence d’objet **Null** est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="75cb4-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="75cb4-111">Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="75cb4-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

