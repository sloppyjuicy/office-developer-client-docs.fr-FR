---
title: Number, propriété (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6707072a61f6be3538e8c0365383584802858981
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597169"
---
# <a name="number-property-ado"></a>Number, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** pouvant correspondre à l’une des constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.

La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple). Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE. Pour plus d’informations sur ces chiffres, consultez le chapitre 16 du guide *OLE DB Programmer’s Reference* (en anglais).

