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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720386"
---
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="06143-102">Erreur de serveur Internet : accès refusé</span><span class="sxs-lookup"><span data-stu-id="06143-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="06143-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="06143-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="06143-104">Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :</span><span class="sxs-lookup"><span data-stu-id="06143-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="06143-105">HTTP\_état\_refusé 401</span><span class="sxs-lookup"><span data-stu-id="06143-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="06143-106">Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="06143-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="06143-107">RDS peut communiquer avec un serveur web IIS dans l’un des trois modes d’authentification de mot de passe : anonyme, Basic ou stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="06143-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="06143-108">En outre, le serveur web doit disposer des autorisations sur l’ordinateur source de données s’il s’agit d’un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="06143-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

