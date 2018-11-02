---
title: FilterAxis, propriété (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 214de72e71a51c6b6b65bc2636a28e5650035c0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926905"
---
# <a name="filteraxis-property-ado-md"></a>FilterAxis, propriété (ADO MD)


**S’applique à**: Access 2013, Office 2013

Fournit des informations de filtrage concernant l'ensemble de cellules actif.

## <a name="return-values"></a>Valeurs de retour

Retourne un objet [Axis](axis-object-ado-md.md) et est en lecture seule.

## <a name="remarks"></a>Notes

Utilisez la propriété **FilterAxis** pour retourner les informations sur les dimensions utilisées pour découper les données. La propriété [DimensionCount](dimensioncount-property-ado-md.md) de l'objet **Axis** retourne le nombre de dimensions de découpage. Cet axe comprend généralement une seule ligne.

L'objet **Axis** retourné par [FilterAxis](filteraxis-property-ado-md.md) n'est pas compris dans la collection [Axes](axes-collection-ado-md.md) d'un objet [Cellset](cellset-object-ado-md.md).

