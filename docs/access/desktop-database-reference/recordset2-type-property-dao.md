---
title: Recordset2. type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 9bec543e-7f59-ea59-dc79-41d0e08b5ab6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198080(v=office.15)
ms:contentKeyID: 48546583
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052880
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6646658daf482373ef8b62f6d3420b1d11152cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307174"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="fccab-102">Recordset2. type, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="fccab-102">Recordset2.Type property (DAO)</span></span>


<span data-ttu-id="fccab-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fccab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fccab-104">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet.</span><span class="sxs-lookup"><span data-stu-id="fccab-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="fccab-105">Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="fccab-105">Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fccab-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fccab-106">Syntax</span></span>

<span data-ttu-id="fccab-107">*expression* . Entrer</span><span class="sxs-lookup"><span data-stu-id="fccab-107">*expression* .Type</span></span>

<span data-ttu-id="fccab-108">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="fccab-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="fccab-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fccab-109">Remarks</span></span>

<span data-ttu-id="fccab-110">Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="fccab-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fccab-111">Constante</span><span class="sxs-lookup"><span data-stu-id="fccab-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="fccab-112">Type d'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="fccab-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fccab-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="fccab-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="fccab-114">Table (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="fccab-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fccab-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="fccab-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="fccab-116">Dynamique (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="fccab-116">Dynamic (ODBCDirect workspaces only)</span></span></p>
<p><span data-ttu-id="fccab-117"><strong>Remarque</strong>: les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="fccab-117"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="fccab-118">Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fccab-118">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fccab-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="fccab-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="fccab-120">Jeu</span><span class="sxs-lookup"><span data-stu-id="fccab-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fccab-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="fccab-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="fccab-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="fccab-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fccab-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="fccab-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="fccab-124">Avant uniquement</span><span class="sxs-lookup"><span data-stu-id="fccab-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

