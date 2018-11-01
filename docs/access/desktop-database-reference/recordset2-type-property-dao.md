---
title: Recordset2.Type Property (DAO)
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
ms.openlocfilehash: 7d35f4acb97871f9d7499b67817c6c88ae56f441
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871898"
---
# <a name="recordset2type-property-dao"></a><span data-ttu-id="09e25-102">Recordset2.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="09e25-102">Recordset2.Type Property (DAO)</span></span>


<span data-ttu-id="09e25-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="09e25-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09e25-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09e25-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e25-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09e25-106">Syntax</span></span>

<span data-ttu-id="09e25-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="09e25-107">*expression* .Type</span></span>

<span data-ttu-id="09e25-108">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="09e25-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e25-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="09e25-109">Remarks</span></span>

<span data-ttu-id="09e25-110">Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="09e25-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09e25-111">Constante</span><span class="sxs-lookup"><span data-stu-id="09e25-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="09e25-112">Type d'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="09e25-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09e25-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="09e25-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="09e25-114">Table (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="09e25-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e25-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="09e25-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="09e25-116">Dynamique (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="09e25-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="09e25-p102">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="09e25-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e25-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="09e25-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="09e25-120">Feuille de réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="09e25-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09e25-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="09e25-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="09e25-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="09e25-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09e25-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="09e25-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="09e25-124">Avant uniquement</span><span class="sxs-lookup"><span data-stu-id="09e25-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

