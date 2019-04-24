---
title: Field2. VisibleValue, propriété (DAO)
TOCTitle: VisibleValue Property
ms:assetid: 1e023a1a-fd49-7570-42bd-2f4c06ac5e5e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845809(v=office.15)
ms:contentKeyID: 48543611
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101184
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 0161ea66068457b53a9667a6739c3a3a0458c8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292614"
---
# <a name="field2visiblevalue-property-dao"></a>Field2. VisibleValue, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . VisibleValue

*expression* Variable qui représente un objet **Field2** .

## <a name="remarks"></a>Remarques

Cette propriété contient la valeur du champ actuellement dans la base de données sur le serveur. Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client a modifié le même champ et le même enregistrement entre le moment où le premier client a extrait les données et celui où il essaie de les mettre à jour. Dans ce cas, la valeur définie par le second client est accessible via cette propriété.

