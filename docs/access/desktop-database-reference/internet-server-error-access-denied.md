---
title: 'Erreur de serveur Internet : accès refusé'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 132ecc75c01cdc54eb2d7664227b7abb1578cc2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876539"
---
# <a name="internet-server-error-access-denied"></a>Erreur de serveur Internet : accès refusé


**S’applique à**: Access 2013, Office 2013

Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :

HTTP\_état\_refusé 401

Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées. RDS peut communiquer avec un serveur web IIS dans l’un des trois modes d’authentification de mot de passe : anonyme, Basic ou stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000). En outre, le serveur web doit disposer des autorisations sur l’ordinateur source de données s’il s’agit d’un ordinateur Windows NT/Windows 2000.

