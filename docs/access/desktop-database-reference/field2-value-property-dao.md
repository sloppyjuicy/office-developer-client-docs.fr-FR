---
title: Field2.Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7071967f662f3cc8a477fde08d151e892674b12f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622248"
---
# <a name="field2value-property-dao"></a>Field2.Value, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*.* Valeur

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui correspond à une valeur adaptée au type de données, tel qu'il est défini par la propriété **Type** d'un objet.

En règle générale, la propriété **Value** permet d'extraire et de modifier les données des objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field2**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en leur faisant directement référence plutôt qu'en définissant la propriété **Value**.

Une erreur capturable survient si vous tentez de définir ou de retourner la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field2** de la collection **Fields** d'un objet **TableDef**) entraîne une erreur capturable.


> [!NOTE]
> Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles sont formattées à l'aide d'une notation scientifique dans un espace de travail Microsoft Access, mais apparaissent comme des valeurs décimales normales dans un espace de travail ODBCDirect.


