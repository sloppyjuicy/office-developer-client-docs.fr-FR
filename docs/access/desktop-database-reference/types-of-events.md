---
title: Types d’événements (référence de base de données de bureau Access)
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3bcf631ffc6c9b4b847af3f973114d6b271d26f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314153"
---
# <a name="types-of-events"></a>Types d’événements


**S’applique à** : Access 2013, Office 2013



Il existe deux types d'événements de base. Les « événements Will », appelés avant le début d'une opération, comportent généralement le terme « Will » dans leur nom, par exemple, **WillChangeRecordset** ou **WillConnect**. Les événements appelés au terme d'un événement comportent généralement le terme « Complete » dans leur nom, par exemple, **RecordChangeComplete** ou **ConnectComplete**. Des exceptions existent, par exemple **InfoMessage**, mais ces événements se produisent une fois que l'opération associée est terminée.

## <a name="will-events"></a>Événements Will

Les gestionnaires d'événements appelés avant le démarrage d'une opération vous permettent d'examiner ou de modifier les paramètres de l'opération, puis d'annuler l'opération ou de l'autoriser à se poursuivre. Ces routines de handler d’événements ont généralement des noms sous la forme **Will* Event***.

## <a name="complete-events"></a>Événements Complete

Les gestionnaires d'événements appelés au terme d'une opération peuvent avertir votre application qu'une opération est terminée. Ces gestionnaires reçoivent aussi une notification lorsqu'un gestionnaire d'événements Will annule une opération en attente. Ces routines de handler d’événements ont généralement des noms au formulaire ***Événement*Complet**.

Les événements Will et Complete sont généralement utilisés par paire.

## <a name="other-events"></a>Autres événements

Les autres handlers d’événements, c’est-à-dire les événements dont le nom n’a pas la forme **Will*Event*** ou ***Event*Complete,** sont appelés uniquement une fois l’opération terminée. Il s'agit des événements **Disconnect**, **EndOfRecordset** et **InfoMessage**.

