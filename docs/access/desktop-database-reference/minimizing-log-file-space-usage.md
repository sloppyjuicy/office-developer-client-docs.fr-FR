---
title: Minimiser l’utilisation de l’espace de fichier journal
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c462641616c126c7732433fc8b7d23bb137b06a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944766"
---
# <a name="minimizing-log-file-space-usage"></a>Minimiser l’utilisation de l’espace de fichier journal

**S’applique à**: Access 2013, Office 2013

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

