---
title: SQLState, propriété (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f5fa247b03efa0391d117b94f3d64184927e4b89
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589105"
---
# <a name="sqlstate-property-ado"></a>SQLState, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'état SQL d'un objet [Error](error-object-ado.md) donné.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **String** de 5 caractères qui, conformément à la norme ANSI SQL, indique le code d'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **SQLState** pour lire le code d'erreur à 5 caractères renvoyé par le fournisseur lorsqu'une erreur se produit lors du traitement d'une instruction SQL. Par exemple, lorsque l'on utilise le fournisseur Microsoft OLE DB pour ODBC avec une base de données Microsoft SQL Server, les codes d'erreur d'état SQL sont issus d'ODBC ; ils reposent soit sur des erreurs spécifiques à ODBC, soit sur des erreurs provenant de Microsoft SQL Server, et sont ensuite mappés sur des erreurs ODBC. Ces codes d'erreur sont documentés dans la norme ANSI SQL, mais peuvent être implémentés différemment dans d'autres sources de données.

