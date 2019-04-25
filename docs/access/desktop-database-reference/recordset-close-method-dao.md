---
title: Recordset.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: e76a81c6-ca0d-e310-c1dc-cbc5d6f6248b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836011(v=office.15)
ms:contentKeyID: 48548404
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f7cbd94bfacc91bfe080d33807ca7989c1dca661
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300552"
---
# <a name="recordsetclose-method-dao"></a>Recordset.Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **Recordset** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* .Close

*expression* Variable représentant un objet **Recordset**.

## <a name="remarks"></a>Remarques

Si le **jeu d’enregistrements** objet est déjà fermé lorsque vous utilisez **fermer**, une erreur d’exécution se produit.

Si vous essayez de fermer une **connexion** objet alors qu’il a toutes **jeu d’enregistrements** objets, le **jeu d’enregistrements** seront fermés les objets et les mises à jour en attente ou modifications seront annulées . De même, si vous essayez de fermer une **espace de travail** objet alors qu’il a toutes **connexion** objets ceux **connexion** objets seront fermés, qui sera fermer leur **jeu d’enregistrements** objets.

Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

