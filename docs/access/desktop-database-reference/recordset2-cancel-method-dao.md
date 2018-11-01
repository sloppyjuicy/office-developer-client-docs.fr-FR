---
title: Recordset2.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: cae49f36-3aad-80d8-c15f-a7a584aa2e9b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834366(v=office.15)
ms:contentKeyID: 48547703
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5df46c36ff28bae1e48dfc8dc77443f707fc3e0a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877533"
---
# <a name="recordset2cancel-method-dao"></a>Recordset2.Cancel Method (DAO)


**S’applique à**: Access 2013, Office 2013

## <a name="syntax"></a>Syntaxe

*expression* . Annuler

*expression* Expression qui renvoie un objet **Recordset2** .

## <a name="remarks"></a>Remarques

Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync). **Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.

