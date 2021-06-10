---
title: ActiveCommand, propriété (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281928"
---
# <a name="activecommand-property-ado"></a><span data-ttu-id="d3b81-102">ActiveCommand, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3b81-102">ActiveCommand property (ADO)</span></span>

<span data-ttu-id="d3b81-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3b81-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3b81-104">Indique l'objet [Command](command-object-ado.md) qui a créé l'objet [Recordset](recordset-object-ado.md) associé.</span><span class="sxs-lookup"><span data-stu-id="d3b81-104">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3b81-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d3b81-105">Return value</span></span>

<span data-ttu-id="d3b81-p101">Renvoie une valeur de type **Variant** qui contient un objet **Command**. La valeur par défaut est une référence d'objet Null.</span><span class="sxs-lookup"><span data-stu-id="d3b81-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3b81-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d3b81-108">Remarks</span></span>

<span data-ttu-id="d3b81-109">La propriété  **ActiveCommand** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d3b81-109">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="d3b81-110">Si un **objet Command** n’a pas été utilisé pour créer l’objet **Recordset** actuel, une référence d’objet **Null** est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="d3b81-110">If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>

<span data-ttu-id="d3b81-111">Utilisez cette propriété pour rechercher l'objet **Command** associé lorsque vous ne recevez que l'objet **Recordset** qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="d3b81-111">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

