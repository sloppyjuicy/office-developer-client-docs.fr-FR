---
title: Blocages avec niveau d’isolation répétable de lecture
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c3b28c8d9be6a81ecc03ccf02d5361110de32f07
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558407"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Blocages avec niveau d’isolation répétable de lecture


**S’applique à** : Access 2013, Office 2013

Si un objet métier personnalisé utilise un niveau d'isolation récurrent de lecture pour accéder à un serveur SQL Server et si l'objet métier est appelé simultanément par deux clients qui envoient une requête et se mettent à jour dans la même transaction, un blocage est possible. Le service RDS est conçu de telle sorte que l'un des processus expire et libère ainsi le blocage. Toutefois, la mise à jour échoue pour ce client.

Utilisez la [propriété dynamique Time](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Out** du service de curseur pour modifier la durée du délai d’accès.

