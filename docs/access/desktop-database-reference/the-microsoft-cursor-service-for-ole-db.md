---
title: Service de curseur Microsoft pour OLE DB
TOCTitle: The Microsoft Cursor Service for OLE DB
ms:assetid: 31861eef-9860-c884-3c60-9794def7be78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249088(v=office.15)
ms:contentKeyID: 48544057
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce8ebea2e9ce1f31adc239195614f4a8b1e2bd1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314356"
---
# <a name="microsoft-cursor-service-for-ole-db"></a><span data-ttu-id="7545a-102">Service de curseur Microsoft pour OLE DB</span><span class="sxs-lookup"><span data-stu-id="7545a-102">Microsoft Cursor Service for OLE DB</span></span>


<span data-ttu-id="7545a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7545a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7545a-p101">Lorsque vous sélectionnez un curseur côté client ou que vous affectez à la propriété **CursorLocation** la valeur **adUseClient**, vous appelez le service de curseur Microsoft pour OLE DB. Vous pouvez également voir des références au « moteur de curseur client », qui est quasiment identique dans le contexte d'ADO. Ce service complète les fonctions de prise en charge de curseurs des fournisseurs de données. Ainsi, vous pouvez bénéficier de fonctionnalités relativement uniformes, quels que soient les fournisseurs de données.</span><span class="sxs-lookup"><span data-stu-id="7545a-p101">When you select a client-side cursor, or set the **CursorLocation** property to **adUseClient**, you are invoking the Microsoft Cursor Service for OLE DB. You might also see references to the "Client Cursor Engine", which is essentially the same thing in the context of ADO. This service supplements the cursor-support functions of data providers. As a result, you can perceive relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="7545a-p102">Le service de curseur pour OLE DB permet d'utiliser des propriétés dynamiques et améliore le comportement de certaines méthodes. Par exemple, la propriété dynamique **Optimize** permet la création d'index temporaires afin de faciliter certaines opérations, notamment la méthode **Find**.</span><span class="sxs-lookup"><span data-stu-id="7545a-p102">The Cursor Service for OLE DB makes dynamic properties available and enhances the behavior of certain methods. For example, the **Optimize** dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the **Find** method.</span></span>

<span data-ttu-id="7545a-p103">Dans tous les cas, le service de curseur prend en charge la mise à jour par lot. Il simule aussi des types de curseur plus performants, tels que les curseurs dynamiques, alors qu'un fournisseur de données peut uniquement fournir des curseurs dont les performances sont plus limitées, tels que les curseurs statiques.</span><span class="sxs-lookup"><span data-stu-id="7545a-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

