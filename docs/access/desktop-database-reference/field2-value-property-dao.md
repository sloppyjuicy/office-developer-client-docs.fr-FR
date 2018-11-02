---
title: Propriété Field2.Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec1bdab14743a43bc4abda029e5f77ec1a8e6212
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925148"
---
# <a name="field2value-property-dao"></a>Propriété Field2.Value (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie la valeur d'un objet. Type de données **Variant** en lecture/écriture.

## <a name="syntax"></a>Syntaxe

*expression* . Valeur

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est un type de données Variant qui est évalué à une valeur appropriée pour le type de données, tel que spécifié par la propriété **Type** d'un objet.

En règle générale, la propriété **Value** permet d'extraire et de modifier les données des objets **Recordset**.

La propriété **Value** est la propriété par défaut des objets **Field2**, **Parameter** et **Property**. Par conséquent, vous pouvez définir ou renvoyer la valeur de l'un de ces objets en leur faisant directement référence plutôt qu'en définissant la propriété **Value**.

Une erreur capturable survient si vous tentez de définir ou de retourner la propriété **Value** dans un contexte inapproprié (par exemple, la propriété **Value** d'un objet **Field2** de la collection **Fields** d'un objet **TableDef**) entraîne une erreur capturable.


> [!NOTE]
> <P>Lorsque vous lisez des valeurs décimales d'une base de données Microsoft SQL Server, elles sont formattées à l'aide d'une notation scientifique dans un espace de travail Microsoft Access, mais apparaissent comme des valeurs décimales normales dans un espace de travail ODBCDirect.</P>


