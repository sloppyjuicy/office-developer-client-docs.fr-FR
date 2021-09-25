---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ebaf5f3a9e0c8ae005c21b0872177e0699c0f9aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568417"
---
# <a name="source-property-ado-error"></a>Source, propriété (objet Erreur ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nom de l'objet ou de l'application à l'origine d'une erreur.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **String** qui indique le nom d'un objet ou d'une application.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Source** sur un objet [Error](error-object-ado.md) pour déterminer le nom de l'objet ou de l'application à l'origine de l'erreur. Il peut s'agir du nom de la classe ou l'ID de programme de l'objet. Pour les erreurs dans ADO, la valeur de la propriété est **ADODB.** *NomObjet*, où *NomObjet* est le nom de l’objet ayant déclenché l’erreur. Pour ADOX et ADO MD, la valeur est **ADOX.** *NomObjet* et **ADOMD.** *NomObjet* respectivement.

À partir de la documentation sur l’erreur indiquant les valeurs des propriétés **Source**, [Number](number-property-ado.md) et [Description](description-property-ado.md) des objets **Error**, vous pouvez écrire un code qui gèrera l’erreur de façon appropriée.

La propriété **Source** des objets **Error** est en lecture seule.

