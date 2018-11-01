---
title: Recordset.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: d841b088-50bf-16d9-33e0-2140050e1ac6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835080(v=office.15)
ms:contentKeyID: 48548030
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bf4d06ad1785c829291fb907585a8784d6b0b75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888005"
---
# <a name="recordsettype-property-dao"></a><span data-ttu-id="aecfb-102">Recordset.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="aecfb-102">Recordset.Type Property (DAO)</span></span>


<span data-ttu-id="aecfb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aecfb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aecfb-p101">Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. Type de données **Integer** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aecfb-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="aecfb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aecfb-106">Syntax</span></span>

<span data-ttu-id="aecfb-107">*expression* . Type</span><span class="sxs-lookup"><span data-stu-id="aecfb-107">*expression* .Type</span></span>

<span data-ttu-id="aecfb-108">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="aecfb-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="aecfb-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="aecfb-109">Remarks</span></span>

<span data-ttu-id="aecfb-110">Pour un objet **Recordset**, les paramètres et valeurs de retour possibles sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="aecfb-110">For a **Recordset** object, the possible settings and return values are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aecfb-111">Constante</span><span class="sxs-lookup"><span data-stu-id="aecfb-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="aecfb-112">Type d'objet Recordset</span><span class="sxs-lookup"><span data-stu-id="aecfb-112">Recordset type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aecfb-113"><strong>dbOpenTable</strong></span><span class="sxs-lookup"><span data-stu-id="aecfb-113"><strong>dbOpenTable</strong></span></span></p></td>
<td><p><span data-ttu-id="aecfb-114">Table (espaces de travail Microsoft Access uniquement)</span><span class="sxs-lookup"><span data-stu-id="aecfb-114">Table (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aecfb-115"><strong>dbOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="aecfb-115"><strong>dbOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="aecfb-116">Dynamique (espaces de travail ODBCDirect uniquement)</span><span class="sxs-lookup"><span data-stu-id="aecfb-116">Dynamic (ODBCDirect workspaces only)</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="aecfb-p102">[!REMARQUE] Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aecfb-p102">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aecfb-119"><strong>dbOpenDynaset</strong></span><span class="sxs-lookup"><span data-stu-id="aecfb-119"><strong>dbOpenDynaset</strong></span></span></p></td>
<td><p><span data-ttu-id="aecfb-120">Feuille de réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="aecfb-120">Dynaset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aecfb-121"><strong>dbOpenSnapshot</strong></span><span class="sxs-lookup"><span data-stu-id="aecfb-121"><strong>dbOpenSnapshot</strong></span></span></p></td>
<td><p><span data-ttu-id="aecfb-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="aecfb-122">Snapshot</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aecfb-123"><strong>dbOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="aecfb-123"><strong>dbOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="aecfb-124">Avant uniquement</span><span class="sxs-lookup"><span data-stu-id="aecfb-124">Forward-only</span></span></p></td>
</tr>
</tbody>
</table>

