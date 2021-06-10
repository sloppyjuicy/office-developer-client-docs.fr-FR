---
title: Objet DataFactory (RDSServer)
TOCTitle: DataFactory object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 77cd06992ef0062859d0a1372d115f8e65246a5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294476"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="03721-102">Objet DataFactory (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="03721-102">DataFactory object (RDSServer)</span></span>


<span data-ttu-id="03721-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="03721-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03721-104">Cet objet métier côté serveur par défaut implémente des méthodes qui procurent un accès en lecture-écriture aux sources de données spécifiées pour des applications côté client.</span><span class="sxs-lookup"><span data-stu-id="03721-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="03721-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="03721-105">Remarks</span></span>

<span data-ttu-id="03721-106">L'objet **RDSServer.DataFactory** est conçu comme un objet Automation côté serveur, qui reçoit les demandes clientes.</span><span class="sxs-lookup"><span data-stu-id="03721-106">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="03721-107">Dans une implémentation Internet, elle réside sur un serveur web et est insérée par le composant ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="03721-107">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="03721-108">L'objet **RDSServer.DataFactory** fournit un accès en lecture-écriture aux sources de données spécifiées, mais ne contient pas de logique de validation ou de règles métier.</span><span class="sxs-lookup"><span data-stu-id="03721-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="03721-p102">Si vous utilisez une méthode disponible à la fois pour les objets **RDSServer.DataFactory** et [RDS.DataControl](datacontrol-object-rds.md), Remote Data Service utilise la version **RDS.DataControl** par défaut. Un scénario de programmation de base est pris comme point de départ par défaut, **RDSServer.DataFactory** étant utilisé comme objet métier côté serveur générique.</span><span class="sxs-lookup"><span data-stu-id="03721-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="03721-111">Si vous souhaitez que votre application web gère le traitement côté serveur spécifique à une tâche, vous pouvez remplacer **RDSServer.DataFactory** par un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="03721-111">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>

<span data-ttu-id="03721-p103">Vous pouvez créer des objets métier côté serveur qui appellent les méthodes de **RDSServer.DataFactory**, comme [Query](query-method-rds.md) et [CreateRecordset](createrecordset-method-rds.md). Cela s'avère utile si vous voulez ajouter des fonctionnalités à vos objets métier tout en profitant des technologies Remote Data Service existantes.</span><span class="sxs-lookup"><span data-stu-id="03721-p103">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="03721-114">L'identificateur de classe de l'objet **RDSServer.DataFactory** est 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="03721-114">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

