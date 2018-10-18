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
# <a name="internet-server-error-access-denied"></a><span data-ttu-id="3a803-102">Erreur du serveur Internet : Accès refusé</span><span class="sxs-lookup"><span data-stu-id="3a803-102">Internet Server Error: Access Denied</span></span>


<span data-ttu-id="3a803-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a803-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a803-104">Si vous obtenez cette erreur, elle signifie généralement que Microsoft Internet Information Services (IIS) a retourné l'état suivant :</span><span class="sxs-lookup"><span data-stu-id="3a803-104">If you get this error, it usually means that Microsoft Internet Information Services (IIS) returned the following status:</span></span>

<span data-ttu-id="3a803-105">HTTP\_état\_refusé 401</span><span class="sxs-lookup"><span data-stu-id="3a803-105">HTTP\_STATUS\_DENIED 401</span></span>

<span data-ttu-id="3a803-106"><<<<<<< Tête Assurez-vous que les répertoires accédés par IIS disposent des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="3a803-106"><<<<<<< HEAD Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="3a803-107">RDS peut communiquer avec un serveur Web IIS fonctionnant sous l'un des trois modes d'authentification de mot de passe : anonyme, de base ou stimulation/réponse de Windows NT (appelée Authentification intégrée Windows sous Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="3a803-107">RDS can communicate with an IIS Web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="3a803-108">Le serveur Web doit également disposer d'autorisations d'accès à l'ordinateur source de données s'il s'agit d'un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3a803-108">Also, the Web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
<span data-ttu-id="3a803-109">=== Vérifiez que les répertoires accédés par IIS disposent des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="3a803-109">======= Make sure the directories accessed by IIS have proper permissions.</span></span> <span data-ttu-id="3a803-110">RDS peut communiquer avec un serveur web IIS dans l’un des trois modes d’authentification de mot de passe : anonyme, Basic ou stimulation/réponse NT (appelée authentification Windows intégrée dans Windows 2000).</span><span class="sxs-lookup"><span data-stu-id="3a803-110">RDS can communicate with an IIS web server running in any one of the three Password Authentication modes: Anonymous, Basic, or NT Challenge/Response (called Integrated Windows authentication in Windows 2000).</span></span> <span data-ttu-id="3a803-111">En outre, le serveur web doit disposer des autorisations sur l’ordinateur source de données s’il s’agit d’un ordinateur Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3a803-111">Also, the web server must have permissions to the data source computer if it is a Windows NT/Windows 2000 computer.</span></span>
>>>>>>> <span data-ttu-id="3a803-112">master</span><span class="sxs-lookup"><span data-stu-id="3a803-112">master</span></span>

