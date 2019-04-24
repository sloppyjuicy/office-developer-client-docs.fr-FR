---
title: QueryDef. Updatable, propriété (DAO)
TOCTitle: Updatable Property
ms:assetid: 9b978b7d-1d76-ff27-a032-dd94660fb088
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198056(v=office.15)
ms:contentKeyID: 48546575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5321e834f1dd5ed663033cacb530962d7beeb5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303331"
---
# <a name="querydefupdatable-property-dao"></a>QueryDef. Updatable, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui indique si vous pouvez changer un objet DAO. Type de données **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*expression* . Modifiable

*expression* Variable qui représente un objet **QueryDef** .

## <a name="remarks"></a>Remarques

La propriété **Updatable** d'un objet **QueryDef** a la valeur **True** si la définition de la requête peut être mise à jour même si l'objet **[Recordset](recordset-object-dao.md)** résultat n'est pas modifiable.

