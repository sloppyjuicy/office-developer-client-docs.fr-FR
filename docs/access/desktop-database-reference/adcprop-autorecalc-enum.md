---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: b9c1aff21b62eff061a3f68ef3ad56e07e46388d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860083"
---
# <a name="adcpropautorecalcenum"></a><span data-ttu-id="2d67c-102">ADCPROP\_AUTORECALC\_ENUM</span><span class="sxs-lookup"><span data-stu-id="2d67c-102">ADCPROP\_AUTORECALC\_ENUM</span></span>

<span data-ttu-id="2d67c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d67c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2d67c-104">Indique si le fournisseur [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcule les colonnes regroupées et calculées dans un Recordset hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="2d67c-104">Specifies when the [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) provider re-calculates aggregate and calculated columns in a hierarchical Recordset.</span></span>

<span data-ttu-id="2d67c-105">Ces constantes ne sont utilisées avec le fournisseur **MSDataShape** et la propriété dynamique «**Auto Recalc**» du **Recordset** , qui est référencée dans l' [Index des propriétés dynamiques ADO](ado-dynamic-property-index.md) et expliquée dans la [Service de curseur Microsoft pour OLE Base de données](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou la documentation de [Microsoft Data Shaping Service pour OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="2d67c-105">These constants are only used with the **MSDataShape** provider and the **Recordset** "**Auto Recalc**" dynamic property, which is referenced in the [ADO Dynamic Property Index](ado-dynamic-property-index.md) and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) or [Microsoft Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d67c-106">Constant</span><span class="sxs-lookup"><span data-stu-id="2d67c-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d67c-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d67c-107">Value</span></span></p></th>
<th><p><span data-ttu-id="2d67c-108">Description</span><span class="sxs-lookup"><span data-stu-id="2d67c-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d67c-109"><strong>adRecalcAlways</strong></span><span class="sxs-lookup"><span data-stu-id="2d67c-109"><strong>adRecalcAlways</strong></span></span></p></td>
<td><p><span data-ttu-id="2d67c-110">1</span><span class="sxs-lookup"><span data-stu-id="2d67c-110">1</span></span></p></td>
<td><p><span data-ttu-id="2d67c-p101">Par défaut. Effectue un nouveau calcul à chaque fois que le fournisseur <strong>MSDataShape</strong> détermine des valeurs modifiées dont dépendent les colonnes calculées.</span><span class="sxs-lookup"><span data-stu-id="2d67c-p101">Default. Recalculates whenever the <strong>MSDataShape</strong> provider determines values that the calculated columns depend upon have changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d67c-113"><strong>adRecalcUpFront</strong></span><span class="sxs-lookup"><span data-stu-id="2d67c-113"><strong>adRecalcUpFront</strong></span></span></p></td>
<td><p><span data-ttu-id="2d67c-114">0</span><span class="sxs-lookup"><span data-stu-id="2d67c-114">0</span></span></p></td>
<td><p><span data-ttu-id="2d67c-115">N'effectue de calcul qu'à la première construction de l'objet <strong>Recordset</strong> hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="2d67c-115">Calculates only when initially building the hierarchical <strong>Recordset</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2d67c-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2d67c-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="2d67c-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="2d67c-117">These constants do not have ADO/WFC equivalents.</span></span>

