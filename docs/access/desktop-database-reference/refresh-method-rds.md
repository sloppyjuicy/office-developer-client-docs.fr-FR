---
title: Refresh, méthode (RDS)
TOCTitle: Refresh method (RDS)
ms:assetid: 968baa7c-9128-7155-a1eb-d77aedda6601
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249668(v=office.15)
ms:contentKeyID: 48546450
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 60de3b25e5eedc277eaafbe4bd1c078863e13f7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309297"
---
# <a name="refresh-method-rds"></a>Refresh, méthode (RDS)

**S’applique à** : Access 2013, Office 2013

Interroge à nouveau la source de données spécifiée dans la propriété [Connect](connect-property-rds.md) et met à jour les résultats de la requête.

## <a name="syntax"></a>Syntaxe

*DataControl*. Actualiser

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*DataControl* |Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).|

## <a name="remarks"></a>Remarques

Vous devez définir les propriétés [Connect](connect-property-rds.md), [Server](server-property-rds.md) et [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) avant d'utiliser la méthode **Refresh**. Tous les contrôles liés aux données présents sur le formulaire associé à un objet **RDS.DataControl** refléteront le nouveau jeu d'enregistrements. Tout objet [Recordset](recordset-object-ado.md) préexistant est libéré et les modifications non enregistrées sont ignorées. La méthode **Refresh** fait automatiquement du premier enregistrement l'enregistrement actif.

Il est conseillé d'appeler régulièrement la méthode **Refresh** lorsque vous manipulez des données. Si vous récupérez des données et que vous les laissez pendant un certain temps sur votre ordinateur client, il est fort possible qu'elles ne soient plus à jour. Il se peut que certaines de vos modifications échouent si un autre utilisateur modifie l'enregistrement et valide les modifications avant vous.

