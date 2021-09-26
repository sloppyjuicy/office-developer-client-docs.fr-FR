---
title: Field2.VisibleValue, propriété (DAO)
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
ms.localizationpriority: medium
ms.openlocfilehash: 82e3e113290bd34adfcf79e5bc429c539c757f29
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626693"
---
# <a name="field2visiblevalue-property-dao"></a>Field2.VisibleValue, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* VisibleValue

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

Cette propriété contient la valeur du champ actuellement dans la base de données sur le serveur. Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client a modifié le même champ et le même enregistrement entre le moment où le premier client a extrait les données et celui où il essaie de les mettre à jour. Dans ce cas, la valeur définie par le second client est accessible via cette propriété.

