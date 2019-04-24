---
title: 'Erreur de serveur Internet : accès refusé'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: af823f46653b3ec83950c2e2cfe639b514196b08
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291254"
---
# <a name="internet-server-error-access-denied"></a>Erreur de serveur Internet : accès refusé


**S’applique à** : Access 2013, Office 2013

Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :

État\_\_http refusé 401

Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées. RDS peut communiquer avec un serveur Web IIS s'exécutant dans l'un des trois modes d'authentification de mot de passe: Anonymous, Basic ou NT Challenge/Response (appelé authentification Windows intégrée dans Windows 2000). De plus, le serveur Web doit disposer d'autorisations sur l'ordinateur de source de données s'il s'agit d'un ordinateur Windows NT/Windows 2000.

