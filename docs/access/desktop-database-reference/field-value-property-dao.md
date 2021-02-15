---
title: Field.Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 6c0f9a8d-f51a-b8cf-8830-f8d960a1d08c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195493(v=office.15)
ms:contentKeyID: 48545465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9b51bb4e08546531f95e3795074f90b5d94d4c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292922"
---
# <a name="fieldvalue-property-dao"></a>Field.Value, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. **Variant** en lecture/écriture.

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


