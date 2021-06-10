---
title: Configuration de serveurs virtuels sur IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9c7f5782885aafd43e365ddc4f08dedd0975234
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295974"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="5abb8-102">Configuration de serveurs virtuels sur IIS</span><span class="sxs-lookup"><span data-stu-id="5abb8-102">Configuring virtual servers on IIS</span></span>

<span data-ttu-id="5abb8-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5abb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5abb8-104">Au moment de créer un serveur virtuel dans Internet Information Services 4.0, il convient d'exécuter les deux étapes supplémentaires suivantes pour permettre au serveur virtuel de fonctionner avec RDS :</span><span class="sxs-lookup"><span data-stu-id="5abb8-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="5abb8-105">Lors de la configuration du serveur, activez la case à cocher « Autoriser l'accès en exécution ».</span><span class="sxs-lookup"><span data-stu-id="5abb8-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="5abb8-106">Déplacez msadcs.dll vers *vroot* \\ msadc, où *vroot* est le répertoire d’accueil de votre serveur virtuel.</span><span class="sxs-lookup"><span data-stu-id="5abb8-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

