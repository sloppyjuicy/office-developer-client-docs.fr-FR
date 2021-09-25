---
title: Commandes paramétrées avec l’intervention de commandes COMPUTE
TOCTitle: Parameterized commands with intervening COMPUTE commands
ms:assetid: ff3724cd-040b-4b5f-bb9b-e6a38fd938c9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250311(v=office.15)
ms:contentKeyID: 48548959
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 37045eac6ab306a1eb992a7456aee02ca40c056d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585528"
---
# <a name="parameterized-commands-with-intervening-compute-commands"></a>Commandes paramétrées avec l’intervention de commandes COMPUTE


**S’applique à** : Access 2013, Office 2013

Une commande APPEND de mise en forme paramétrée contient généralement une clause qui crée un objet **Recordset** parent à l'aide d'une commande de requête et une autre clause qui crée un objet **Recordset** enfant également au moyen d'une commande de requête paramétrée — c'est-à-dire, une commande contenant un espace réservé de paramètre (un point d'interrogation, « ? »). L'objet **Recordset** mis en forme qui en résulte présente deux niveaux : un niveau supérieur occupé par le parent, et un niveau inférieur occupé par l'enfant.

La clause qui crée l'objet **Recordset** enfant peut désormais représenter un nombre arbitraire de commandes  de mise en forme imbriquées, la commande la plus profondément imbriquée contenant la requête paramétrée. L'objet **Recordset** mis en forme résultant présente plusieurs niveaux. Le parent occupe le niveau supérieur et l'enfant le niveau inférieur, et un nombre arbitraire d'objets **Recordset** générés par les commandes COMPUTE de mise en forme occupent les niveaux intermédiaires.

Cette fonctionnalité est généralement utilisée pour appeler la fonction d'agrégation et les les fonctionnalités de regroupement des commandes COMPUTE de mise en forme dans le but de créer des objets **Recordset** intermédiaires contenant des informations analytiques sur l'objet **Recordset** enfant. Par ailleurs, s'agissant d'une commande de mise en forme paramétrée, chaque accès à une colonne de chapitre du parent peut donner lieu à la récupération d'un nouvel objet **Recordset** enfant. Dans la mesure où les niveaux intermédiaires sont dérivés de l'enfant, ils sont également recalculés.

