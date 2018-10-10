---
title: Number, propriété (ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469082"
---
# <a name="number-property-ado"></a>Number, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique le numéro qui identifie de manière unique un objet [Error](error-object-ado.md).

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** pouvant correspondre à l'une des constantes [ErrorValueEnum](errorvalueenum.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Number** pour identifier l'erreur générée. La valeur de la propriété est un nombre unique qui correspond à la condition d'erreur.

La collection [Errors](errors-collection-ado.md) renvoie un HRESULT en format format hexadécimal (0x80004005 par exemple) ou une valeur longue (2147467259 par exemple). Ces HRESULT peuvent être déclenchés par composants sous-jacents comme OLE DB ou même OLE. Pour plus d’informations sur ces numéros, consultez le chapitre 16 de la *de référence du programmeur OLE DB.*

