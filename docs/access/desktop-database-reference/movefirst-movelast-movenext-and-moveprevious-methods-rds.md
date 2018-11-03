---
title: MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c78e6aaca31201e076dffb55b19be638a337dd19
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944927"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (RDS)


**S’applique à**: Access 2013, Office 2013

Accède au premier ou dernier enregistrement, à l'enregistrement suivant ou précédent d'un objet [Recordset](recordset-object-ado.md) spécifié.

## <a name="syntax"></a>Syntaxe

*DataControl*. Jeu d’enregistrements. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Paramètres

  - *DataControl*

  - Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).

## <a name="remarks"></a>Remarques

Vous pouvez utiliser les méthodes **Move** avec le **RDS. DataControl** objet pour parcourir les enregistrements de données dans les contrôles liés aux données sur une page Web. Supposons, par exemple, que vous affichez un objet **Recordset** dans une grille en le liant à un objet **RDS.DataControl**. Vous pouvez ensuite inclure des boutons Premier, Dernier, Suivant et Précédent sur lesquels les utilisateurs peuvent cliquer pour accéder au premier ou dernier enregistrement, ou encore à l'enregistrement suivant ou précédent de l'objet **Recordset** affiché. Pour ce faire, appelez les méthodes **MoveFirst**, **MoveLast**, **MoveNext** et **MovePrevious** de l'objet **RDS.DataControl** dans les procédures onClick, respectivement pour les boutons Premier, Dernier, Suivant et Précédent. L' [exemple du Carnet d'adresses](address-book-navigation-buttons.md) illustre cette procédure.

