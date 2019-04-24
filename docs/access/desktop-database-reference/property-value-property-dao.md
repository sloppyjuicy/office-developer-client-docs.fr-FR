---
title: Propriété Property. Value (DAO)
TOCTitle: Value Property
ms:assetid: 26e47b3a-4f70-27b5-2498-b44ce4dfc99f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191905(v=office.15)
ms:contentKeyID: 48543824
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052994
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3e7c79fe12b3b7bfe98e0c7547f4ed2d12b148ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301168"
---
# <a name="propertyvalue-property-dao"></a>Propriété Property. Value (DAO)

**S’applique à** : Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Valeur

*expression* Variable qui représente un objet **Property** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui correspond à une valeur adaptée au type de données, tel qu'il est défini par la propriété **Type** d'un objet.

En général, la propriété **Value** sert à récupérer et modifier des données dans les objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.

Si vous tentez de définir ou de renvoyer la propriété **Value** dans un contexte inadapté (par exemple la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), une erreur piégeable est générée.

> [!NOTE]
> Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles seront mises en forme à l'aide de la notation scientifique dans un espace de travail Microsoft Access mais apparaîtront comme des valeurs décimales normales dans un espace de travail ODBCDirect.


