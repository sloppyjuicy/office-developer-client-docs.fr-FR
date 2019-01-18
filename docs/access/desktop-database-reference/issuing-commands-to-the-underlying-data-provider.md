---
title: Émission de commandes au fournisseur de données sous-jacentes
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d8876b180d668be5734233a33714d7541b9c3d1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709613"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Émission de commandes au fournisseur de données sous-jacentes

**S’applique à**: Access 2013, Office 2013

Toute commande ne commençant pas par SHAPE est transférée au fournisseur de données. Ceci équivaut à l'émission d'une commande de mise en forme telle que « SHAPE {commande du fournisseur} ». Effectuez ces commandes *pas* obligé de générer un **jeu d’enregistrements**. Par exemple, la commande de mise en forme « SHAPE {DROP TABLE MyTable} » est parfaitement valide, à condition que le fournisseur de données prenne en charge la commande DROP TABLE.

Cette fonctionnalité permet aux commandes de fournisseur normales et aux commandes de mise en forme de partager la même connexion et la même transaction.

