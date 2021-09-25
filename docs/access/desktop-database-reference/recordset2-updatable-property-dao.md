---
title: Recordset2.Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 072eae0ef403aef283af5078cd0a2dc6f0320140
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557966"
---
# <a name="recordset2updatable-property-dao"></a>Recordset2.Updatable, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Updatable

*expression* Variable qui représente un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Les objets Recordset de type capture instantanée et avant uniquement retournent toujours **la forme False**.

De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.

Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.

Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.

