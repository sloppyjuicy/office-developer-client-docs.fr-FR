---
title: Configuration de serveurs virtuels sur IIS
TOCTitle: Configuring virtual servers on IIS
ms:assetid: 0a8057a2-c90b-d0b5-21c8-5343e80708ce
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248837(v=office.15)
ms:contentKeyID: 48543154
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: db240ef561de9ba653dbad3453a2ee4d894baa25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602891"
---
# <a name="configuring-virtual-servers-on-iis"></a>Configuration de serveurs virtuels sur IIS

**S’applique à** : Access 2013, Office 2013

Au moment de créer un serveur virtuel dans Internet Information Services 4.0, il convient d'exécuter les deux étapes supplémentaires suivantes pour permettre au serveur virtuel de fonctionner avec RDS :

1.  Lors de la configuration du serveur, activez la case à cocher « Autoriser l'accès en exécution ».

2.  Déplacez msadcs.dll vers *vroot* \\ msadc, où *vroot* est le répertoire d’accueil de votre serveur virtuel.

