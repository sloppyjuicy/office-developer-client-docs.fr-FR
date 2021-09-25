---
title: Name, propriété (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8bf9420370021b35c86c08746d0257289d156cd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568795"
---
# <a name="name-property-ado-md"></a>Name, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique le nom d'un objet.

## <a name="return-values"></a>Valeurs de retour

Retourne une valeur de type **String** et est en lecture seule.

## <a name="remarks"></a>Remarques

Vous pouvez récupérer la propriété **Name** d’un objet par référence ordinale, après quoi vous pouvez directement faire référence à l’objet par son nom. Si, par exemple, cdf.CubeDefs(0).Name produit la valeur « Bobs Video Store », vous pouvez faire référence à cet objet [CubeDef](cubedef-object-ado-md.md) comme suit : cdf.CubeDefs(« Bobs Video Store »).

