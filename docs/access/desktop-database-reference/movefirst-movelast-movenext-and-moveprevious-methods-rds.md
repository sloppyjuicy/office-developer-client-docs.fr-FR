---
title: Méthodes MoveFirst, MoveLast, MoveNext et MovePrevious (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c78ea7f7b5ae34c291d9eab272cf893f3d073b95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558225"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>Méthodes MoveFirst, MoveLast, MoveNext et MovePrevious (RDS)

**S’applique à** : Access 2013, Office 2013

Accède au premier ou dernier enregistrement, à l’enregistrement suivant ou précédent d’un objet [Recordset](recordset-object-ado.md) spécifié.

## <a name="syntax"></a>Syntaxe

*DataControl*. Recordset. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les **méthodes Move** avec **rdS. Objet DataControl** pour naviguer dans les enregistrements de données dans les contrôles liés aux données sur une page web. 

Supposons, par exemple, que vous affichez un objet **Recordset** dans une grille en le liant à un objet **RDS.DataControl**. Vous pouvez ensuite inclure des boutons Premier, Dernier, Suivant et Précédent sur lesquels les utilisateurs peuvent cliquer pour accéder au premier ou dernier enregistrement, ou encore à l'enregistrement suivant ou précédent de l'objet **Recordset** affiché. Pour ce faire, appelez les méthodes **MoveFirst**, **MoveLast**, **MoveNext** et **MovePrevious** de l'objet **RDS.DataControl** dans les procédures onClick, respectivement pour les boutons Premier, Dernier, Suivant et Précédent. L' [exemple du Carnet d'adresses](address-book-navigation-buttons.md) illustre cette procédure.

