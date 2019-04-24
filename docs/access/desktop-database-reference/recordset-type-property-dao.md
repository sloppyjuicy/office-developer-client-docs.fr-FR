---
title: Recordset. type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4a55af8aaa5cfb3d87e13125871a6ccbe1e7f2dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307552"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="87d35-102">Recordset. type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="87d35-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="87d35-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="87d35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87d35-104">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="87d35-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="87d35-105">Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87d35-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="87d35-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87d35-106">Syntax</span></span>

<span data-ttu-id="87d35-107">*expression* . Entrer</span><span class="sxs-lookup"><span data-stu-id="87d35-107">*expression* .Type</span></span>

<span data-ttu-id="87d35-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="87d35-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d35-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="87d35-109">Remarks</span></span>

<span data-ttu-id="87d35-110">Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="87d35-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="87d35-111">Constante</span><span class="sxs-lookup"><span data-stu-id="87d35-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="87d35-112">Type d'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="87d35-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87d35-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="87d35-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="87d35-114">Table (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="87d35-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87d35-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="87d35-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="87d35-116">Dynamique (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="87d35-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="87d35-117"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="87d35-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="87d35-118">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="87d35-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87d35-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="87d35-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="87d35-120">Jeu</span><span class="sxs-lookup"><span data-stu-id="87d35-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87d35-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="87d35-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="87d35-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="87d35-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87d35-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="87d35-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="87d35-124">Avant uniquement</span><span class="sxs-lookup"><span data-stu-id="87d35-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

