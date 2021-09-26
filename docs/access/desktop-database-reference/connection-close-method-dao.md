---
title: Connection.Close, méthode (DAO)
TOCTitle: Close Method
ms:assetid: 9b1a77cb-da12-24d6-892f-a56be103d51d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198015(v=office.15)
ms:contentKeyID: 48546559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 120ad21231187aa2cba21e1ef55c6f9d135b6934
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590079"
---
# <a name="connectionclose-method-dao"></a>Connection.Close, méthode (DAO)


**S’applique à** : Access 2013, Office 2013

Ferme un objet **Connection** ouvert.

## <a name="syntax"></a>Syntaxe

*expression* .Close

*expression* Variable qui représente un objet **Connection**.

## <a name="remarks"></a>Remarques

Si le **jeu d’enregistrements** objet est déjà fermé lorsque vous utilisez **fermer**, une erreur d’exécution se produit.

Si vous essayez de fermer une **connexion** objet alors qu’il a toutes **jeu d’enregistrements** objets, le **jeu d’enregistrements** seront fermés les objets et les mises à jour en attente ou modifications seront annulées . De même, si vous essayez de fermer une **espace de travail** objet alors qu’il a toutes **connexion** objets ceux **connexion** objets seront fermés, qui sera fermer leur **jeu d’enregistrements** objets.

Une alternative à l’utilisation de la méthode **Close** consiste à définir la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).

