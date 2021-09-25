---
title: Field.Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 305b94655d46dcbd089f1bfde5b2b0482fdde23f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597302"
---
# <a name="fieldvalue-property-dao"></a>Field.Value, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*.* Valeur

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui correspond à une valeur adaptée au type de données, tel qu'il est défini par la propriété **Type** d'un objet.

En général, la propriété **Value** sert à récupérer et modifier des données dans les objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.

Si vous tentez de définir ou de renvoyer la propriété **Value** dans un contexte inadapté (par exemple la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), une erreur piégeable est générée.


> [!NOTE]
> Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles seront mises en forme à l'aide de la notation scientifique dans un espace de travail Microsoft Access mais apparaîtront comme des valeurs décimales normales dans un espace de travail ODBCDirect.


