---
title: Minimisation de l’espace occupé par le fichier journal
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c8d582d55596b7d19220580bc2e670e92bfeb0ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602205"
---
# <a name="minimizing-log-file-space-usage"></a>Minimisation de l’espace occupé par le fichier journal

**S’applique à** : Access 2013, Office 2013

Un fichier journal peut rapidement arriver à saturation (et par là même arrêter le serveur) si une base de données SQL Server est fortement sollicitée. Vous pouvez faire en sorte que le fichier journal soit **vidé au point de contrôle** pour allonger de manière significative la durée de vie du fichier journal d'une base de données.

**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 6.5**

1.  Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Unités de base de données.

2.  Double-cliquez sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction.

3.  Sous l'onglet **Base de données**, sélectionnez **Tronquer**.

4.  Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.

**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 7.0**

1.  Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Bases de données.

2.  Cliquez avec le bouton droit sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction et choisissez **Propriétés**.

3.  Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.

Pour plus d'informations sur la fonction de **vidage au point de contrôle**, consultez la documentation de Microsoft SQL Server.

