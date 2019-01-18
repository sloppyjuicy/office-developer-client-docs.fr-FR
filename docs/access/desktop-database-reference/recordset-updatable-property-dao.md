---
title: Propriété Recordset.Updatable (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 722ccc2334cd00ed89a1193709023db039ba9fd3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712917"
---
# <a name="recordsetupdatable-property-dao"></a>Propriété Recordset.Updatable (DAO)


**S’applique à**: Access 2013, Office 2013

Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour

*expression* Variable qui représente un objet **Recordset** .

## <a name="remarks"></a>Remarques

Les objets Recordset et transférer-only type instantané renvoient toujours **False**.

De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.

Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.

Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.

