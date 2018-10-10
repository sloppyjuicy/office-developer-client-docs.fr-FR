---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dcc674a570b3d2adf6108316339a86333a82f9d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470678"
---
# <a name="source-property-ado-error"></a>Source, propriété (objet Erreur ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le nom de l'objet ou de l'application à l'origine d'une erreur.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **String** qui indique le nom d'un objet ou d'une application.

## <a name="remarks"></a>Remarques

Utilisez la propriété **Source** sur un objet [Error](error-object-ado.md) pour déterminer le nom de l'objet ou de l'application à l'origine de l'erreur. Il peut s'agir du nom de la classe ou l'ID de programme de l'objet. Des erreurs dans ADO, la valeur de la propriété sera **ADODB. *** ObjectName*, où *NomObjet* est le nom de l’objet qui a déclenché l’erreur. Pour ADOX et ADO MD, la valeur sera **ADOX. *** ObjectName* et **ADOMD. *** ObjectName,* respectivement.

À partir de la documentation sur l'erreur indiquant les valeurs des propriétés **Source**, [Number](number-property-ado.md) et [Description](description-property-ado.md) des objets **Error**, vous pouvez écrire un code qui gèrera l'erreur de façon appropriée.

La propriété **Source** des objets **Error** est en lecture seule.

