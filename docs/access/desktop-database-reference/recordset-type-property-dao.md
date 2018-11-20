---
title: Propriété Recordset.Type (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3eedbab083807f91ffef78aab25d110db779188
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026084"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="de9fe-102">Propriété Recordset.Type (DAO)</span><span class="sxs-lookup"><span data-stu-id="de9fe-102">Recordset.Type property (DAO)</span></span>


<span data-ttu-id="de9fe-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de9fe-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de9fe-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="de9fe-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="de9fe-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de9fe-106">Syntax</span></span>

<span data-ttu-id="de9fe-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="de9fe-107">*expression* .Type</span></span>

<span data-ttu-id="de9fe-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="de9fe-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="de9fe-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="de9fe-109">Remarks</span></span>

<span data-ttu-id="de9fe-110">Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="de9fe-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="de9fe-111">Constante</span><span class="sxs-lookup"><span data-stu-id="de9fe-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="de9fe-112">Type d'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="de9fe-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="de9fe-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="de9fe-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="de9fe-114">Table (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="de9fe-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de9fe-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="de9fe-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="de9fe-116">Dynamique (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="de9fe-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="de9fe-117"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="de9fe-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="de9fe-118">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="de9fe-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de9fe-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="de9fe-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="de9fe-120">Feuille de réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="de9fe-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="de9fe-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="de9fe-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="de9fe-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="de9fe-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="de9fe-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="de9fe-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="de9fe-124">Avant uniquement</span><span class="sxs-lookup"><span data-stu-id="de9fe-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

