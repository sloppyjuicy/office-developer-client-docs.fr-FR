---
title: NativeError, propriété (ADO)
TOCTitle: NativeError property (ADO)
ms:assetid: 9f4d4064-5ee7-20f8-fd54-2cb2eae64d7b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249731(v=office.15)
ms:contentKeyID: 48546685
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 86734d77cafd8dbe3c26219e291c16b81ef0026b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288609"
---
# <a name="nativeerror-property-ado"></a>NativeError, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique le code d'erreur spécifique au fournisseur pour un objet [Error](error-object-ado.md) donné.

## <a name="return-value"></a>Valeur renvoyée

Renvoie une valeur de type **Long** qui indique le code d'erreur.

## <a name="remarks"></a>Remarques

Utilisez la propriété **NativeError** pour récupérer les informations spécifiques à la base de données sur l'objet **Error** concerné. Par exemple, lorsque l'on utilise un fournisseur Microsoft ODBC pour OLE DB avec une base de données Microsoft SQL, les codes d'erreur d'origine provenant de SQL Server transitent par ODBC et par le fournisseur ODBC pour atteindre la propriété **Native Error** ADO.

