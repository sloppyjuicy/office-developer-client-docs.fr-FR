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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291087"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="713ad-102">Émission de commandes au fournisseur de données sous-jacentes</span><span class="sxs-lookup"><span data-stu-id="713ad-102">Issuing commands to the underlying data provider</span></span>

<span data-ttu-id="713ad-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="713ad-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="713ad-p101">Toute commande ne commençant pas par SHAPE est transférée au fournisseur de données. Ceci équivaut à l'émission d'une commande de mise en forme telle que « SHAPE {commande du fournisseur} ». Ces commandes *ne doivent pas* produire de **jeu d'enregistrements**. Par exemple, la commande de mise en forme « SHAPE {DROP TABLE MyTable} » est parfaitement valide, à condition que le fournisseur de données prenne en charge la commande DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="713ad-p101">Any command that does not begin with SHAPE is passed through to the data provider. This is equivalent to issuing a shape command in the form "SHAPE {provider command}". These commands do *not* have to produce a **Recordset**. For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="713ad-108">Cette fonctionnalité permet aux commandes de fournisseur normales et aux commandes de mise en forme de partager la même connexion et la même transaction.</span><span class="sxs-lookup"><span data-stu-id="713ad-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

