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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="dd5ba-102">Erreur de serveur Internet : accès refusé</span><span class="sxs-lookup"><span data-stu-id="dd5ba-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="dd5ba-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dd5ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dd5ba-104">Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :</span><span class="sxs-lookup"><span data-stu-id="dd5ba-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="dd5ba-105">HTTP\_état\_refusé 401</span><span class="sxs-lookup"><span data-stu-id="dd5ba-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="dd5ba-106">Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="dd5ba-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="dd5ba-107">RDS peut communiquer avec un serveur web IIS dans l’un des trois modes d’authentification de mot de passe : anonyme, Basic ou stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="dd5ba-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="dd5ba-108">En outre, le serveur web doit disposer des autorisations sur l’ordinateur source de données s’il s’agit d’un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="dd5ba-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

