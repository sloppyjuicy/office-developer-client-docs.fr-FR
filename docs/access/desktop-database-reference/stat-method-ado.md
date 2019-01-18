---
title: Méthode Stat - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721072"
---
# <a name="stat-method-ado"></a>Stat, méthode (ADO)

**S’applique à**: Access 2013, Office 2013

Extrait des informations relatives à un objet **Stream**.

## <a name="syntax"></a>Syntaxe

Longueur du *flux*. Stat (*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valeur renvoyée

Valeur de type Long indiquant l'état de l'opération.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*StatStg* |Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.|
|*StatFlag* |Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.<br/><br/>L’énumération STATFLAG possède deux valeurs :<br/>-STATFLAG_DEFAULT : 0<br/>-STATFLAG_NONAME : 1 |


## <a name="remarks"></a>Notes

La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :

|Champ|Description|
|:--------|:----------|
|*pwcsName* |Une chaîne contenant le nom du flux, si elle est disponible et le StatFlag valeur STATFLAG\_anonyme n’a pas été spécifié.|
|*cbSize* |Indique la taille en octets du flux ou du tableau d'octets.|
|*mtime* |Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.|
|*ctime* |Indique l'heure de création de ce stockage, flux ou tableau d'octets.|
|*atime* |Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.|

Si STATFLAG\_anonyme est spécifié dans le paramètre StatFlag, le nom du flux n’est pas retourné.

Si STATFLAG\_anonyme n’a pas été spécifié dans le paramètre StatFlag et aucun nom n’est disponible pour le flux actif, cette valeur sera E\_NOTIMPL.

