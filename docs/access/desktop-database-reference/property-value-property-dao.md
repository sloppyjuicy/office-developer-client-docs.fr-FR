---
title: Propriété Property.Value (DAO)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713379"
---
# <a name="propertyvalue-property-dao"></a>Propriété Property.Value (DAO)

**S’applique à**: Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Valeur

*expression* Variable qui représente un objet **Property** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.

En général, la propriété **Value** est utilisée pour récupérer et modifier les données dans les objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en les référençant directement au lieu de spécifier la propriété **Value**.

Si vous essayez de définir ou de renvoyer la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**), vous obtenez une erreur interceptable.

> [!NOTE]
> Lorsque vous lisez des valeurs décimales depuis une base de données Microsoft SQL Server, elle sont mises en forme à l'aide d'une notation scientifique via un espace de travail Microsoft Access, mais elles s'affichent sous forme de valeurs décimales normales via un espace de travail ODBCDirect.


