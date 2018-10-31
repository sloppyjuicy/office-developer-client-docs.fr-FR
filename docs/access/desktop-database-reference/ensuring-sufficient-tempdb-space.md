---
title: Prévision d'un espace TempDB suffisant
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d049a098a7f7cfd826c6c5945c71831acbceb04
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863051"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="73740-102">Prévision d'un espace TempDB suffisant</span><span class="sxs-lookup"><span data-stu-id="73740-102">Ensuring Sufficient TempDB Space</span></span>


<span data-ttu-id="73740-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73740-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="73740-p101">Si des erreurs se produisent lors du traitement d'objets [Recordset](recordset-object-ado.md) nécessitant un espace de traitement dans Microsoft SQL Server 6.5, vous serez peut-être amené à augmenter la taille de TempDB. (Certaines requêtes nécessitent un espace de traitement temporaire ; par exemple, une requête assortie d'une clause ORDER BY exige le tri de l'objet **Recordset**, ce qui requiert une certaine quantité d'espace temporaire.)</span><span class="sxs-lookup"><span data-stu-id="73740-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73740-106">[!IMPORTANTE] Lisez cette procédure avant d'effectuer des actions, car il est plus difficile de réduire une unité qui a été préalablement étendue.</span><span class="sxs-lookup"><span data-stu-id="73740-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="73740-p102">[!REMARQUE] Par défaut, dans Microsoft SQL Server 7.0 et les versions ultérieures, la base de données TempDB est configurée pour croître automatiquement en fonction des besoins. Ainsi, il est possible que cette procédure ne s'applique qu'aux serveurs exécutant des versions antérieures à la version 7.0.</span><span class="sxs-lookup"><span data-stu-id="73740-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="73740-109">**Pour augmenter l'espace de TempDB dans SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="73740-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="73740-110">Démarrez Microsoft® SQL Server Enterprise Manager, ouvrez l'arborescence Serveur, puis l'arborescence Unités de base de données.</span><span class="sxs-lookup"><span data-stu-id="73740-110">Start Microsoft® SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="73740-p103">Sélectionnez une unité (physique) à développer, telle que Master, puis double-cliquez sur l'unité pour ouvrir la boîte de dialogue **Edition des unités de base de données**. Cette boîte de dialogue indique la quantité d'espace utilisée par les bases de données actives.</span><span class="sxs-lookup"><span data-stu-id="73740-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="73740-113">Dans la zone **Taille**, augmentez l'espace disque attribué à l'unité selon la quantité souhaitée (par exemple, 50 mégaoctets (Mo)).</span><span class="sxs-lookup"><span data-stu-id="73740-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="73740-114">Cliquez sur **Modifier maintenant** pour augmenter la quantité d'espace de la base de données (logique) TempDB.</span><span class="sxs-lookup"><span data-stu-id="73740-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="73740-p104">Ouvrez l'arborescence Bases de données sur le serveur, puis double-cliquez sur **TempDB** pour ouvrir la boîte de dialogue **Edition de la base de données**. L'onglet **Base de données** affiche la quantité d'espace actuellement alloué à TempDB (**Taille des données**). La valeur par défaut est 2 Mo.</span><span class="sxs-lookup"><span data-stu-id="73740-p104">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box. The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**). By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="73740-p105">Sous le groupe **Taille**, cliquez sur **Développer**. Les graphiques indiquent la quantité d'espace disponible et allouée sur chaque unité physique. Les barres de couleur bordeau représentent l'espace disponible.</span><span class="sxs-lookup"><span data-stu-id="73740-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="73740-121">Sélectionnez une **unité de journal** (par exemple, Master) pour afficher la taille disponible dans la zone **Taille (Mo)**.</span><span class="sxs-lookup"><span data-stu-id="73740-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="73740-p106">Cliquez sur **Développer maintenant** pour allouer cet espace à la base de données TempDB. La boîte de dialogue **Edition de la base de données** affiche la nouvelle taille allouée à TempDB.</span><span class="sxs-lookup"><span data-stu-id="73740-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="73740-124">Pour plus d'informations à ce sujet, effectuez une recherche sur « Développement de la base de données, boîte de dialogue » dans le fichier d'aide de Microsoft SQL Server Enterprise Manager.</span><span class="sxs-lookup"><span data-stu-id="73740-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

