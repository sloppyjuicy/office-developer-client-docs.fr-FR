---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705399"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="aca66-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="aca66-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="aca66-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aca66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aca66-104">Indique si le fournisseur [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcule les colonnes regroupées et calculées dans un Recordset hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="aca66-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="aca66-105">Ces constantes ne sont utilisées avec le fournisseur **MSDataShape** et la propriété dynamique «**Auto Recalc**» du **Recordset** , qui est référencée dans l' [Index des propriétés dynamiques ADO](ado-dynamic-property-index.md) et expliquée dans la [Service de curseur Microsoft pour OLE Base de données](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou la documentation de [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="aca66-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aca66-106">Constante</span><span class="sxs-lookup"><span data-stu-id="aca66-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="aca66-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="aca66-107">Value</span></span></p></th>
<th><p><span data-ttu-id="aca66-108">Description</span><span class="sxs-lookup"><span data-stu-id="aca66-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aca66-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="aca66-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="aca66-110">1</span><span class="sxs-lookup"><span data-stu-id="aca66-110">1</span></span></p></td>
<td><p><span data-ttu-id="aca66-p101">Par défaut. Effectue un nouveau calcul à chaque fois que le fournisseur <strong>MSDataShape</strong> détermine des valeurs modifiées dont dépendent les colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="aca66-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aca66-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="aca66-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="aca66-114">0</span><span class="sxs-lookup"><span data-stu-id="aca66-114">0</span></span></p></td>
<td><p><span data-ttu-id="aca66-115">N'effectue de calcul qu'à la première construction de l'objet <strong>Recordset</strong> hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="aca66-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="aca66-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="aca66-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="aca66-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="aca66-117">These constants do not have ADO/WFC equivalents.</span></span>

