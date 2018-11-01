---
title: SQLState, propriété (ADO)
TOCTitle: SQLState property (ADO)
ms:assetid: cf3b078a-849e-1ad2-cba4-a26160080868
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250029(v=office.15)
ms:contentKeyID: 48547806
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6fb45342a56a003856192a353270778b44654de
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872178"
---
# <a name="sqlstate-property-ado"></a>SQLState, propriété (ADO)


**S’applique à**: Access 2013, Office 2013

Indique l'état SQL d'un objet [Error](error-object-ado.md) donné.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur **String** de 5 caractères qui, conformément à la norme ANSI SQL, indique le code d'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **SQLState** pour lire le code d'erreur à 5 caractères renvoyé par le fournisseur lorsqu'une erreur se produit lors du traitement d'une instruction SQL. Par exemple, lorsque l'on utilise le fournisseur Microsoft OLE DB pour ODBC avec une base de données Microsoft SQL Server, les codes d'erreur d'état SQL sont issus d'ODBC ; ils reposent soit sur des erreurs spécifiques à ODBC, soit sur des erreurs provenant de Microsoft SQL Server, et sont ensuite mappés sur des erreurs ODBC. Ces codes d'erreur sont documentés dans la norme ANSI SQL, mais peuvent être implémentés différemment dans d'autres sources de données.

