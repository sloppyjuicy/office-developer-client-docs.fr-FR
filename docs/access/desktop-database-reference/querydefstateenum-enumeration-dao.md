---
title: QueryDefStateEnum, énumération (DAO)
TOCTitle: QueryDefStateEnum Enumeration
ms:assetid: edfa3085-f8b4-b813-0828-2ba2a9dc0b9d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836359(v=office.15)
ms:contentKeyID: 48548549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7a2163caf8b0c6f7b17d0a551d95d18d0883e183
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945473"
---
# <a name="querydefstateenum-enumeration-dao"></a><span data-ttu-id="03fcd-102">QueryDefStateEnum, énumération (DAO)</span><span class="sxs-lookup"><span data-stu-id="03fcd-102">QueryDefStateEnum enumeration (DAO)</span></span>


<span data-ttu-id="03fcd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03fcd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03fcd-104">Cette énumération est utilisée avec la propriété **Prepare** afin de spécifier la méthode utilisée pour définir la préparation d'une requête.</span><span class="sxs-lookup"><span data-stu-id="03fcd-104">Used with the **Prepare** property to specify the method used to specify how a query should be prepared.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03fcd-105">Nom</span><span class="sxs-lookup"><span data-stu-id="03fcd-105">Name</span></span></p></th>
<th><p><span data-ttu-id="03fcd-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="03fcd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="03fcd-107">Description</span><span class="sxs-lookup"><span data-stu-id="03fcd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03fcd-108">dbQPrepare</span><span class="sxs-lookup"><span data-stu-id="03fcd-108">dbQPrepare</span></span></p></td>
<td><p><span data-ttu-id="03fcd-109">1</span><span class="sxs-lookup"><span data-stu-id="03fcd-109">1</span></span></p></td>
<td><p><span data-ttu-id="03fcd-110">(Valeur par défaut) L'instruction est préparée (l'API ODBC SQLPrepare est appelée).</span><span class="sxs-lookup"><span data-stu-id="03fcd-110">(Default) The statement is prepared (that is, the ODBC SQLPrepare API is called).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03fcd-111">dbQUnprepare</span><span class="sxs-lookup"><span data-stu-id="03fcd-111">dbQUnprepare</span></span></p></td>
<td><p><span data-ttu-id="03fcd-112">2</span><span class="sxs-lookup"><span data-stu-id="03fcd-112">2</span></span></p></td>
<td><p><span data-ttu-id="03fcd-113">L'instruction n'est pas préparée (l'API ODBC SQLExecDirect est appelée).</span><span class="sxs-lookup"><span data-stu-id="03fcd-113">The statement is not prepared (that is, the ODBC SQLExecDirect API is called).</span></span></p></td>
</tr>
</tbody>
</table>

