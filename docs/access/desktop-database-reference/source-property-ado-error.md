---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061306"
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

