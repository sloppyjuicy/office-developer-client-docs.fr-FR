---
title: 'Erreur du serveur Internet : Accès refusé'
TOCTitle: 'Internet Server Error: Access Denied'
ms:assetid: 65f4608b-afec-2867-dae3-e29bae03a6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249395(v=office.15)
ms:contentKeyID: 48545334
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db78b6f2c51e2e5df918622043e33abc6bc9e674
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470329"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="0a2ae-102">Erreur du serveur Internet : Accès refusé</span><span class="sxs-lookup"><span data-stu-id="0a2ae-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="0a2ae-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a2ae-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a2ae-104">Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :</span><span class="sxs-lookup"><span data-stu-id="0a2ae-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="0a2ae-105">HTTP\_état\_refusé 401</span><span class="sxs-lookup"><span data-stu-id="0a2ae-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="0a2ae-p101">Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées. RDS peut communiquer avec un serveur Web IIS fonctionnant sous l'un des trois modes d'authentification de mot de passe : anonyme, de base ou stimulation/réponse de Windows NT (appelée Authentification intégrée Windows sous Windows 2000). Le serveur Web doit également disposer d'autorisations d'accès à l'ordinateur source de données s'il s'agit d'un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0a2ae-p101">Make sure the directories accessed by IIS have proper permissions. RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000). Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

