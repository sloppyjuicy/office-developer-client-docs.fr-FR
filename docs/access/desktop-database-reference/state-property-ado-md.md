---
title: State, propriété (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5e6d8dbad4245e68fb18cbc5c90dab54d4466601
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593543"
---
# <a name="state-property-ado-md"></a>State, propriété (ADO MD)


**S’applique à** : Access 2013, Office 2013

Indique l'état actuel de l'ensemble de cellules.

## <a name="return-values"></a>Valeurs de retour

Retourne un entier de type **Long** qui indique la condition actuelle de l'objet [Cellset](cellset-object-ado-md.md) et est en lecture seule. Les valeurs suivantes sont valides : **adStateClosed** (0) et **adStateOpen** (1).

## <a name="remarks"></a>Remarques

Pour utiliser les noms des constantes [ObjectStateEnum](objectstateenum.md)  la bibliothèque de types ADO doit être référencée dans votre projet. Pour plus d’informations, consultez  [Utilisation d’ADO avec ADO MD](using-ado-with-ado-md.md).

