---
title: FilterAxis, propriété (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a2bd438f2556aea44785922dd399aeb47940a78
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581153"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Fournit des informations de filtrage concernant l'ensemble de cellules actif.

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Axis](axis-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Remarques

Utilisez la propriété **FilterAxis** pour retourner les informations sur les dimensions utilisées pour découper les données. La propriété [DimensionCount](dimensioncount-property-ado-md.md) de l'objet **Axis** retourne le nombre de dimensions de découpage. Cet axe comprend généralement une seule ligne.

L'objet **Axis** retourné par [FilterAxis](filteraxis-property-ado-md.md) n'est pas compris dans la collection [Axes](axes-collection-ado-md.md) d'un objet [Cellset](cellset-object-ado-md.md).

