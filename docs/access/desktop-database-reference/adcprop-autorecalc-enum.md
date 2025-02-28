---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1cd23f801d6a0461349ec558f40d535f28abd699
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558662"
---
# <a name="adcprop_autorecalc_enum"></a>ADCPROPAUTORECALCENUM\_\_

**S’applique à** : Access 2013, Office 2013

Indique si le fournisseur [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) recalcule les colonnes regroupées et calculées dans un Recordset hiérarchique.

Ces constantes sont utilisées uniquement avec le fournisseur **MSDataShape** et la  propriété dynamique « **Recalc** automatique » du jeu d’enregistrements, qui est référencé dans l’index des propriétés dynamiques [ADO](ado-dynamic-property-index.md) et documenté dans la documentation du service de curseur [Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) ou [Microsoft Data Shaping Service pour la documentation OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md).


<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>Par défaut. Effectue un nouveau calcul à chaque fois que le fournisseur <strong>MSDataShape</strong> détermine des valeurs modifiées dont dépendent les colonnes calculées.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>N'effectue de calcul qu'à la première construction de l'objet <strong>Recordset</strong> hiérarchique.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

