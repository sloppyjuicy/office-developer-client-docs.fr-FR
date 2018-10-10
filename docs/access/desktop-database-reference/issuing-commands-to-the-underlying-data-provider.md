---
title: Émission de commandes au fournisseur de données sous-jacent
TOCTitle: Issuing Commands to the Underlying Data Provider
ms:assetid: 9d8ef3f3-d93c-af67-3114-d2c36c78a802
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249716(v=office.15)
ms:contentKeyID: 48546626
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5083f339860e0b28b43e2ceefeaf2cdd1de4b660
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470167"
---
# <a name="issuing-commands-to-the-underlying-data-provider"></a><span data-ttu-id="ecfc1-102">Émission de commandes au fournisseur de données sous-jacent</span><span class="sxs-lookup"><span data-stu-id="ecfc1-102">Issuing Commands to the Underlying Data Provider</span></span>


<span data-ttu-id="ecfc1-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ecfc1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ecfc1-104">Toute commande ne commençant pas par SHAPE est transférée au fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="ecfc1-104">Any command that does not begin with SHAPE is passed through to the data provider.</span></span> <span data-ttu-id="ecfc1-105">Ceci équivaut à l'émission d'une commande de mise en forme telle que « SHAPE {commande du fournisseur} ».</span><span class="sxs-lookup"><span data-stu-id="ecfc1-105">This is equivalent to issuing a shape command in the form "SHAPE {provider command}".</span></span> <span data-ttu-id="ecfc1-106">Effectuez ces commandes *pas* obligé de générer un **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="ecfc1-106">These commands do *not* have to produce a **Recordset**.</span></span> <span data-ttu-id="ecfc1-107">Par exemple, la commande de mise en forme « SHAPE {DROP TABLE MyTable} » est parfaitement valide, à condition que le fournisseur de données prenne en charge la commande DROP TABLE.</span><span class="sxs-lookup"><span data-stu-id="ecfc1-107">For instance, "SHAPE {DROP TABLE MyTable} is a perfectly valid shape command, assuming the data provider supports DROP TABLE.</span></span>

<span data-ttu-id="ecfc1-108">Cette fonctionnalité permet aux commandes de fournisseur normales et aux commandes de mise en forme de partager la même connexion et la même transaction.</span><span class="sxs-lookup"><span data-stu-id="ecfc1-108">This capability allows both normal provider commands and shape commands to share the same connection and transaction.</span></span>

