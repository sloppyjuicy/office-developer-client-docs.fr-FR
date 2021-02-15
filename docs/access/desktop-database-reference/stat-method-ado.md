---
title: Stat, méthode - ActiveX Data Objects (ADO)
TOCTitle: Stat method (ADO)
ms:assetid: d3d3976b-14d4-dee0-412d-a37bc72fbfd3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250056(v=office.15)
ms:contentKeyID: 48547916
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 853d89bde9184bd546b3e7df9e8eda287faf86c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308548"
---
# <a name="stat-method-ado"></a>Stat, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Extrait des informations relatives à un objet **Stream**.

## <a name="syntax"></a>Syntaxe

Flux *long*. Stat(*StatStg*, *StatFlag*)

## <a name="return-value"></a>Valeur renvoyée

Valeur de type Long indiquant l'état de l'opération.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*StatStg* |Structure STATSTG contenant des informations relatives au flux. L'implémentation de la méthode Stat utilisée par l'objet Stream ADO ne remplit pas tous les champs de la structure.|
|*StatFlag* |Indique que cette méthode ne renvoie pas certains membres dans la structure STATSTG, ce qui permet d'éviter une opération d'allocation de mémoire. Les valeurs sont extraites de l'énumération STATFLAG.<br/><br/>L’éumération STATFLAG a deux valeurs :<br/>- STATFLAG_DEFAULT : 0<br/>- STATFLAG_NONAME : 1 |


## <a name="remarks"></a>Remarques

La version de la méthode Stat implémentée pour l'objet Stream ADO remplit les champs de la structure STATSTG suivants :

|Champ|Description|
|:--------|:----------|
|*pwcsName* |Chaîne contenant le nom du flux, si une chaîne est disponible et si la valeur STATFlag \_ STATFLAG NONAME n’a pas été spécifiée.|
|*cbSize* |Indique la taille en octets du flux ou du tableau d'octets.|
|*mtime* |Indique l'heure de dernière modification de ce stockage, flux ou tableau d'octets.|
|*ctime* |Indique l'heure de création de ce stockage, flux ou tableau d'octets.|
|*atime* |Indique l'heure du dernier accès à ce stockage, flux ou tableau d'octets.|

Si STATFLAG NONAME est spécifié dans le paramètre StatFlag, le nom du flux \_ n’est pas renvoyé.

Si STATFLAG NONAME n’a pas été spécifié dans le paramètre StatFlag et qu’aucun nom n’est disponible pour le flux actuel, cette valeur sera \_ E \_ NOTIMPL.

