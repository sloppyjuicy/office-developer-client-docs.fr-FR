---
title: MaxRecords, propriété (ADO)
TOCTitle: MaxRecords property (ADO)
ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15)
ms:contentKeyID: 48544475
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7d66a26cffb14220670643c5b6b5aafe94e8fcb5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870085"
---
# <a name="maxrecords-property-ado"></a><span data-ttu-id="3e52e-102">MaxRecords, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e52e-102">MaxRecords property (ADO)</span></span>


<span data-ttu-id="3e52e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e52e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e52e-104">Indique le nombre maximum d'enregistrements à renvoyer à un [Recordset](recordset-object-ado.md) après une requête.</span><span class="sxs-lookup"><span data-stu-id="3e52e-104">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="3e52e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="3e52e-105">Settings and return values</span></span>

<span data-ttu-id="3e52e-p101">Définit ou renvoie une valeur de type **Long** qui indique le nombre maximum d'enregistrements à renvoyer. La valeur par défaut est zéro (pas de limite).</span><span class="sxs-lookup"><span data-stu-id="3e52e-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="3e52e-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="3e52e-108">Remarks</span></span>

<span data-ttu-id="3e52e-p102">Utilisez la propriété **MaxRecords** pour limiter le nombre d'enregistrements de la source de données que le fournisseur doit renvoyer. Le paramètre par défaut de cette propriété est zéro, ce qui signifie que le fournisseur renvoie tous les enregistrements demandés.</span><span class="sxs-lookup"><span data-stu-id="3e52e-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="3e52e-111">La propriété **MaxRecords** est accessible en lecture/écriture lorsque le **Recordset** est fermé et en lecture seule lorsqu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="3e52e-111">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

