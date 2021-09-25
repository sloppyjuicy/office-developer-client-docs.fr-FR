---
title: Parameter.Value, propriété (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4663a9dcdc31107e674cfe0e039e37240a81b0eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568746"
---
# <a name="parametervalue-property-dao"></a>Parameter.Value, propriété (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*.* Valeur

*expression* Variable qui représente un objet **Parameter.**

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui correspond à une valeur adaptée au type de données, tel qu'il est défini par la propriété **Type** d'un objet.

En général, la propriété **Value** sert à récupérer et modifier des données dans les objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.

Si vous tentez de définir ou de renvoyer la propriété **Value** dans un contexte inadapté (par exemple la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), une erreur piégeable est générée.

> [!NOTE]
> Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles seront mises en forme à l'aide de la notation scientifique dans un espace de travail Microsoft Access mais apparaîtront comme des valeurs décimales normales dans un espace de travail ODBCDirect.


