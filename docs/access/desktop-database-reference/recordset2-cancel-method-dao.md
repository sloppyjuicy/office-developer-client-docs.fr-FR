---
title: Recordset2.Cancel, méthode (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a7fbf84e610f57081bea30a0b6a609a11d865f13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611748"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*.* Annuler

*expression* Expression qui renvoie un **objet Recordset2.**

## <a name="remarks"></a>Remarques

Utilisez la **méthode Cancel** pour terminer l’exécution d’un appel asynchrone de méthode **Execute** ou **OpenConnection** (autrement dit, la méthode a été invoquée avec l’option dbRunAsync). **L’annulation** retourne une erreur d’utilisation si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez de terminer.

