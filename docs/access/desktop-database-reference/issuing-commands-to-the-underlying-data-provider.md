---
title: Émission de commandes au fournisseur de données sous-jacentes
TOCTitle: Issuing commands to the underlying data provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d9d796218305c8aeef5a7bb0593450fc0deec371
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572941"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Émission de commandes au fournisseur de données sous-jacentes

**S’applique à** : Access 2013, Office 2013

Toute commande ne commençant pas par SHAPE est transférée au fournisseur de données. Ceci équivaut à l'émission d'une commande de mise en forme telle que « SHAPE {commande du fournisseur} ». Ces commandes *ne doivent pas* produire de **jeu d'enregistrements**. Par exemple, la commande de mise en forme « SHAPE {DROP TABLE MyTable} » est parfaitement valide, à condition que le fournisseur de données prenne en charge la commande DROP TABLE.

Cette fonctionnalité permet aux commandes de fournisseur normales et aux commandes de mise en forme de partager la même connexion et la même transaction.

