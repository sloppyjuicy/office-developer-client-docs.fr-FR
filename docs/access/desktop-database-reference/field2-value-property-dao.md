---
title: Field2.Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292628"
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


