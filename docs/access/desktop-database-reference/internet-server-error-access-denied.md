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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="7bc0b-102">Erreur de serveur Internet : accès refusé</span><span class="sxs-lookup"><span data-stu-id="7bc0b-102">Internet Server error: Access Denied</span></span>


<span data-ttu-id="7bc0b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bc0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bc0b-104">Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :</span><span class="sxs-lookup"><span data-stu-id="7bc0b-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="7bc0b-105">État\_\_http refusé 401</span><span class="sxs-lookup"><span data-stu-id="7bc0b-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="7bc0b-106">Assurez-vous dans ce cas que les répertoires accédés par IIS disposent des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-106">Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="7bc0b-107">RDS peut communiquer avec un serveur Web IIS s'exécutant dans l'un des trois modes d'authentification de mot de passe: Anonymous, Basic ou NT Challenge/Response (appelé authentification Windows intégrée dans Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="7bc0b-107">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="7bc0b-108">De plus, le serveur Web doit disposer d'autorisations sur l'ordinateur de source de données s'il s'agit d'un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7bc0b-108">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>

