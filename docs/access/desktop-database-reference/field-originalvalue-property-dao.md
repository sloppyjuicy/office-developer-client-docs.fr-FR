---
title: Propriété Field.OriginalValue (DAO)
TOCTitle: OriginalValue Property
ms:assetid: 69ccec1e-311f-6905-e7bb-ad7fa8277494
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195384(v=office.15)
ms:contentKeyID: 48545418
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d850ebcfef6ea2c08e20ed953dfcc7b5ea23cbab
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926793"
---
# <a name="fieldoriginalvalue-property-dao"></a>Propriété Field.OriginalValue (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . OriginalValue

*expression* Variable qui représente un objet **Field** .

## <a name="remarks"></a>Remarques

Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client modifie le même champ et le même enregistrement entre le moment où le premier client extrait les données et celui où il essaie de les mettre à jour. La propriété **OriginalValue** renferme la valeur du champ au moment du lancement de la dernière opération **Update** en lot. Si cette valeur ne correspond pas à celle de la base de données lorsque la méthode **Update** en lot tente d'écrire dans la base de données, une collision survient. Dans ce cas, la nouvelle valeur de la base de données est accessible via la propriété **[VisibleValue](field-visiblevalue-property-dao.md)**.

