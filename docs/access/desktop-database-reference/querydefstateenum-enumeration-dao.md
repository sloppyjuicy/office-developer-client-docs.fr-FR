---
title: QueryDefStateEnum, énumération (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698658"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="6d443-102">QueryDefStateEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d443-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="6d443-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d443-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d443-104">Cette énumération est utilisée avec la propriété **Prepare** afin de spécifier la méthode utilisée pour définir la préparation d'une requête.</span><span class="sxs-lookup"><span data-stu-id="6d443-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d443-105">Nom</span><span class="sxs-lookup"><span data-stu-id="6d443-105">Name</span></span></p></th>
<th><p><span data-ttu-id="6d443-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d443-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6d443-107">Description</span><span class="sxs-lookup"><span data-stu-id="6d443-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d443-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="6d443-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="6d443-109">1</span><span class="sxs-lookup"><span data-stu-id="6d443-109">1</span></span></p></td>
<td><p><span data-ttu-id="6d443-110">(Valeur par défaut) L'instruction est préparée (l'API ODBC SQLPrepare est appelée).</span><span class="sxs-lookup"><span data-stu-id="6d443-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d443-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="6d443-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="6d443-112">2</span><span class="sxs-lookup"><span data-stu-id="6d443-112">2</span></span></p></td>
<td><p><span data-ttu-id="6d443-113">L'instruction n'est pas préparée (l'API ODBC SQLExecDirect est appelée).</span><span class="sxs-lookup"><span data-stu-id="6d443-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

