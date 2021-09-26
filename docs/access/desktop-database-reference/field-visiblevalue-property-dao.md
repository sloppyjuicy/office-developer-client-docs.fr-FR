---
title: Field.VisibleValue, propriété (DAO)
TOCTitle: VisibleValue Property
ms:assetid: e40fcb43-9a1d-69e7-1544-8f15ef21daf4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835776(v=office.15)
ms:contentKeyID: 48548332
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5b99b60edbe6b14091a81cf9f48c6a894932b083
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622332"
---
# <a name="fieldvisiblevalue-property-dao"></a>Field.VisibleValue, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* VisibleValue

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Cette propriété contient la valeur du champ actuellement dans la base de données sur le serveur. Lors d'une mise à jour en lot optimiste, une collision peut survenir dans le cas où un second client a modifié le même champ et le même enregistrement entre le moment où le premier client a extrait les données et celui où il essaie de les mettre à jour. Dans ce cas, la valeur définie par le second client est accessible via cette propriété.

