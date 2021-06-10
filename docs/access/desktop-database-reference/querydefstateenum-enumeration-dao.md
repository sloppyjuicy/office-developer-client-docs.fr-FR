---
title: QueryDefStateEnum, éumération (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ca9923b1604b17c1d7f64d2d968378fec4a8c24
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303317"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="8cc9c-102">QueryDefStateEnum, éumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="8cc9c-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="8cc9c-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cc9c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8cc9c-104">Cette énumération est utilisée avec la propriété **Prepare** afin de spécifier la méthode utilisée pour définir la préparation d'une requête.</span><span class="sxs-lookup"><span data-stu-id="8cc9c-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cc9c-105">Nom</span><span class="sxs-lookup"><span data-stu-id="8cc9c-105">Name</span></span></p></th>
<th><p><span data-ttu-id="8cc9c-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cc9c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8cc9c-107">Description</span><span class="sxs-lookup"><span data-stu-id="8cc9c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cc9c-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="8cc9c-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="8cc9c-109">1</span><span class="sxs-lookup"><span data-stu-id="8cc9c-109">1</span></span></p></td>
<td><p><span data-ttu-id="8cc9c-110">(Valeur par défaut) L'instruction est préparée (l'API ODBC SQLPrepare est appelée).</span><span class="sxs-lookup"><span data-stu-id="8cc9c-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cc9c-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="8cc9c-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="8cc9c-112">2</span><span class="sxs-lookup"><span data-stu-id="8cc9c-112">2</span></span></p></td>
<td><p><span data-ttu-id="8cc9c-113">L'instruction n'est pas préparée (l'API ODBC SQLExecDirect est appelée).</span><span class="sxs-lookup"><span data-stu-id="8cc9c-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

