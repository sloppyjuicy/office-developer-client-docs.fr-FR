---
title: 'Erreur du serveur Internet : Accès refusé'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c874b7a2c4facb9f5969bf9a2150c86773a2687a
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603342"
---
# <a name="internet-server-error-access-denied"></a>Erreur du serveur Internet : Accès refusé


**S’applique à**: Access 2013 | Office 2013

Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :

HTTP\_état\_refusé 401

<<<<<<< Tête Assurez-vous que les répertoires accédés par IIS disposent des autorisations appropriées. RDS peut communiquer avec un serveur Web IIS fonctionnant sous l'un des trois modes d'authentification de mot de passe : anonyme, de base ou stimulation/réponse de Windows NT (appelée Authentification intégrée Windows sous Windows 2000). Le serveur Web doit également disposer d'autorisations d'accès à l'ordinateur source de données s'il s'agit d'un ordinateur Windows NT/Windows 2000.
=== Vérifiez que les répertoires accédés par IIS disposent des autorisations appropriées. RDS peut communiquer avec un serveur web IIS dans l’un des trois modes d’authentification de mot de passe : anonyme, Basic ou stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000). En outre, le serveur web doit disposer des autorisations sur l’ordinateur source de données s’il s’agit d’un ordinateur Windows NT/Windows 2000.
>>>>>>> master

