---
title: Name, propriété (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469877"
---
# <a name="name-property-ado-md"></a>Name, propriété (ADO MD)


**S’applique à**: Access 2013 | Office 2013

Indique le nom d'un objet.

## <a name="return-values"></a>Valeurs de retour

Retourne une valeur de type **String** et est en lecture seule.

## <a name="remarks"></a>Notes

Vous pouvez récupérer la propriété **Name** d'un objet par référence ordinale, après quoi vous pouvez directement faire référence à l'objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).

