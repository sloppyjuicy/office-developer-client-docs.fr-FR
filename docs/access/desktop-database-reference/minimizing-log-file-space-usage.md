---
title: Minimisation de l’espace occupé par le fichier journal
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715276"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="f88ba-102">Minimisation de l’espace occupé par le fichier journal</span><span class="sxs-lookup"><span data-stu-id="f88ba-102">Minimizing log file space usage</span></span>

<span data-ttu-id="f88ba-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f88ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f88ba-p101">Un fichier journal peut rapidement arriver à saturation (et par là même arrêter le serveur) si une base de données SQL Server est fortement sollicitée. Vous pouvez faire en sorte que le fichier journal soit **vidé au point de contrôle** pour allonger de manière significative la durée de vie du fichier journal d'une base de données.</span><span class="sxs-lookup"><span data-stu-id="f88ba-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="f88ba-106">**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="f88ba-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="f88ba-107">Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Unités de base de données.</span><span class="sxs-lookup"><span data-stu-id="f88ba-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="f88ba-108">Double-cliquez sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f88ba-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="f88ba-109">Sous l'onglet **Base de données**, sélectionnez **Tronquer**.</span><span class="sxs-lookup"><span data-stu-id="f88ba-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="f88ba-110">Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f88ba-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="f88ba-111">**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="f88ba-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="f88ba-112">Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Bases de données.</span><span class="sxs-lookup"><span data-stu-id="f88ba-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="f88ba-113">Cliquez avec le bouton droit sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f88ba-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="f88ba-114">Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f88ba-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="f88ba-115">Pour plus d'informations sur la fonction de **vidage au point de contrôle**, consultez la documentation de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f88ba-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

