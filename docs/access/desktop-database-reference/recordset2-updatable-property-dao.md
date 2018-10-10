---
title: Recordset2.Updatable Property (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 54ec9af0b8fa1948afe568dc57eacf9962283504
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469608"
---
# <a name="recordset2updatable-property-dao"></a>Recordset2.Updatable Property (DAO)


**S’applique à**: Access 2013 | Office 2013

Renvoie une valeur indiquant si vous pouvez modifier un objet DAO. Type **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Mise à jour

*expression* Variable qui représente un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Les objets Recordset et transférer-only type instantané renvoient toujours **False**.

De nombreux types d'objets peuvent contenir des champs non modifiables. Par exemple, vous pouvez créer un objet **Recordset** de type feuille de réponse dynamique dans lequel seuls certains champs peuvent être modifiés. Il peut s'agir de champs fixes ou contenant des données incrémentées automatiquement. Il est également possible que la feuille de réponse dynamique soit le résultat d'une requête qui combine des tables modifiables et non modifiables.

Si l'objet ne contient que des champs en lecture seule, la valeur de la propriété **Updatable** est **False**. Lorsqu'un ou plusieurs champs sont modifiables, la valeur de la propriété est **True**. Vous ne pouvez mettre à jour que les champs modifiables. Une erreur piégeable se produit lorsque vous tentez d'affecter une nouvelle valeur à un champ en lecture seule.

Dans la mesure où un objet modifiable peut contenir des champs en lecture seule, vérifiez la propriété **DataUpdatable** de chaque champ de la collection **Fields** d'un objet **Recordset** avant de modifier un enregistrement.

