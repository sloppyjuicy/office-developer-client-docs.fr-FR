---
title: Limitation de l'espace utilisé dans le fichier journal
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2ac2bee2bf3f1036583bd195edc0c3da9e052f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472407"
---
# <a name="minimizing-log-file-space-usage"></a><span data-ttu-id="70dc5-102">Limitation de l'espace utilisé dans le fichier journal</span><span class="sxs-lookup"><span data-stu-id="70dc5-102">Minimizing Log File Space Usage</span></span>


<span data-ttu-id="70dc5-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="70dc5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="70dc5-p101">Un fichier journal peut rapidement arriver à saturation (et par là même arrêter le serveur) si une base de données SQL Server est fortement sollicitée. Vous pouvez faire en sorte que le fichier journal soit **vidé au point de contrôle** pour allonger de manière significative la durée de vie du fichier journal d'une base de données.</span><span class="sxs-lookup"><span data-stu-id="70dc5-p101">A log file may fill quickly (thus halting the server) if there is a large volume of activity on an SQL Server database. You can set the log file to **Truncate on Checkpoint** to significantly extend the life of the log file for a database.</span></span>

<span data-ttu-id="70dc5-106">**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="70dc5-106">**To enable Truncate on Checkpoint in Microsoft SQL Server 6.5**</span></span>

1.  <span data-ttu-id="70dc5-107">Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Unités de base de données.</span><span class="sxs-lookup"><span data-stu-id="70dc5-107">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="70dc5-108">Double-cliquez sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction.</span><span class="sxs-lookup"><span data-stu-id="70dc5-108">Double-click the name of the database on which this feature will be enabled.</span></span>

3.  <span data-ttu-id="70dc5-109">Sous l'onglet **Base de données**, sélectionnez **Tronquer**.</span><span class="sxs-lookup"><span data-stu-id="70dc5-109">From the **Database** tab, select **Truncate**.</span></span>

4.  <span data-ttu-id="70dc5-110">Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="70dc5-110">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="70dc5-111">**Pour activer la fonction de vidage au point de contrôle dans Microsoft SQL Server 7.0**</span><span class="sxs-lookup"><span data-stu-id="70dc5-111">**To enable Truncate on Checkpoint in Microsoft SQL Server 7.0**</span></span>

1.  <span data-ttu-id="70dc5-112">Démarrez Microsoft SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Bases de données.</span><span class="sxs-lookup"><span data-stu-id="70dc5-112">Start Microsoft SQL Server Enterprise Manager, open the tree for the Server, and then open the Databases tree.</span></span>

2.  <span data-ttu-id="70dc5-113">Cliquez avec le bouton droit sur le nom de la base de données pour laquelle vous souhaitez activer cette fonction et choisissez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="70dc5-113">Right-click the name of the database on which this feature will be enabled and choose **Properties**.</span></span>

3.  <span data-ttu-id="70dc5-114">Sous l'onglet **Options**, sélectionnez **Vider le journal au point de contrôle**, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="70dc5-114">From the **Options** tab, select **Truncate Log on Checkpoint**, and then click **OK**.</span></span>

<span data-ttu-id="70dc5-115">Pour plus d'informations sur la fonction de **vidage au point de contrôle**, consultez la documentation de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="70dc5-115">For more information about the **Truncate on Checkpoint** feature, see the Microsoft SQL Server documentation.</span></span>

