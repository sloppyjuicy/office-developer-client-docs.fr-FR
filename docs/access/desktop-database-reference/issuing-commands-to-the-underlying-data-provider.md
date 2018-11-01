---
title: Émission de commandes au fournisseur de données sous-jacent
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f0379d38b6c38145a72d5ab41b7ee0e7ec45531b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889076"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a>Émission de commandes au fournisseur de données sous-jacent


**S’applique à**: Access 2013, Office 2013

Toute commande ne commençant pas par SHAPE est transférée au fournisseur de données. Ceci équivaut à l'émission d'une commande de mise en forme telle que « SHAPE {commande du fournisseur} ». Effectuez ces commandes *pas* obligé de générer un **jeu d’enregistrements**. Par exemple, la commande de mise en forme « SHAPE {DROP TABLE MyTable} » est parfaitement valide, à condition que le fournisseur de données prenne en charge la commande DROP TABLE.

Cette fonctionnalité permet aux commandes de fournisseur normales et aux commandes de mise en forme de partager la même connexion et la même transaction.

