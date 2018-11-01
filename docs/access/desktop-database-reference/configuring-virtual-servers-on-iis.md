---
title: Configuration des serveurs virtuels dans IIS
TOCTitle: Configuring Virtual Servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7408e2dc10a5e47b298b77a9244477b16bca3ff1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879241"
---
# <a name="configuring-virtual-servers-on-iis"></a><span data-ttu-id="10988-102">Configuration des serveurs virtuels dans IIS</span><span class="sxs-lookup"><span data-stu-id="10988-102">Configuring Virtual Servers on IIS</span></span>


<span data-ttu-id="10988-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="10988-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="10988-104">Au moment de créer un serveur virtuel dans Internet Information Services 4.0, il convient d'exécuter les deux étapes supplémentaires suivantes pour permettre au serveur virtuel de fonctionner avec RDS :</span><span class="sxs-lookup"><span data-stu-id="10988-104">When creating virtual servers in Internet Information Services 4.0, the following two extra steps are needed in order to configure the virtual server to work with RDS:</span></span>

1.  <span data-ttu-id="10988-105">Lors de la configuration du serveur, activez la case à cocher « Autoriser l'accès en exécution ».</span><span class="sxs-lookup"><span data-stu-id="10988-105">When setting up the server, check "Allow Execute Access."</span></span>

2.  <span data-ttu-id="10988-106">Déplacez msadcs.dll dans *vroot*\\msadc, où *vroot* est le répertoire racine de votre serveur virtuel.</span><span class="sxs-lookup"><span data-stu-id="10988-106">Move msadcs.dll to *vroot*\\msadc, where *vroot* is the home directory of your virtual server.</span></span>

