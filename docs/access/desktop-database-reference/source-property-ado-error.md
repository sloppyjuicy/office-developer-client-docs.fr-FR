---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f03dcc8049113df13ff8654aee340d1e2d6e502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308595"
---
# <a name="source-property-ado-error"></a>Source, propriété (objet Erreur ADO)


**S’applique à** : Access 2013, Office 2013

Indique le nom de l'objet ou de l'application à l'origine d'une erreur.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **String** qui indique le nom d'un objet ou d'une application.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Source** sur un objet [Error](error-object-ado.md) pour déterminer le nom de l'objet ou de l'application à l'origine de l'erreur. Il peut s'agir du nom de la classe ou l'ID de programme de l'objet. Pour les erreurs dans ADO, la valeur de la propriété sera **ADODB.***ObjectName*, *où ObjectName* est le nom de l’objet qui a déclenché l’erreur. Pour ADOX et ADO MD, la valeur sera **ADOX.***ObjectName* et **ADOMD.**ObjectName,* respectivement.

À partir de la documentation sur l'erreur indiquant les valeurs des propriétés **Source**, [Number](number-property-ado.md) et [Description](description-property-ado.md) des objets **Error**, vous pouvez écrire un code qui gèrera l'erreur de façon appropriée.

La propriété **Source** des objets **Error** est en lecture seule.

