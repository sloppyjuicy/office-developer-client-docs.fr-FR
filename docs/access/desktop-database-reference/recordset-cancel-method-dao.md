---
title: Recordset.Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: 89acfbf1-b937-dc19-ada1-6f8f50489147
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197080(v=office.15)
ms:contentKeyID: 48546169
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 102511575770ceb38cf682d5e627fb7e64faa1ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300811"
---
# <a name="recordsetcancel-method-dao"></a>Recordset.Cancel, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* Annuler

*expression* Variable qui représente un objet **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la **méthode Cancel** pour terminer l’exécution d’un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été invoquée avec l’option dbRunAsync). **L’annulation** retourne une erreur d’utilisation si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez de terminer.

