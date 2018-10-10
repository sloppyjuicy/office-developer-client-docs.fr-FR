---
title: Blocages avec niveau d'isolation récurrent de lecture
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469676"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a>Blocages avec niveau d'isolation récurrent de lecture


**S’applique à**: Access 2013 | Office 2013

Si un objet métier personnalisé utilise un niveau d'isolation récurrent de lecture pour accéder à un serveur SQL Server et si l'objet métier est appelé simultanément par deux clients qui envoient une requête et se mettent à jour dans la même transaction, un blocage est possible. Le service RDS est conçu de telle sorte que l'un des processus expire et libère ainsi le blocage. Toutefois, la mise à jour échoue pour ce client.

Utilisez la propriété dynamique**Command Time Out** de [Service de curseur](microsoft-cursor-service-for-ole-db-ado-service-component.md)pour modifier le délai d’expiration.

