---
title: Méthode QueryDef.Cancel (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 6c404f493072974632bfdd155fc2664258721867
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558043"
---
# <a name="querydefcancel-method-dao"></a>Méthode QueryDef.Cancel (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* Annuler

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

Utilisez la **méthode Cancel** pour terminer l’exécution d’un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été invoquée avec l’option dbRunAsync). **L’annulation** retourne une erreur d’utilisation si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez de terminer.

