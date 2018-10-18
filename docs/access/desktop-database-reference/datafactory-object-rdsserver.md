---
title: DataFactory, objet (RDSServer)
TOCTitle: DataFactory Object (RDSServer)
ms:assetid: 1de76cdd-34dc-8547-29aa-48ad6067bdea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248971(v=office.15)
ms:contentKeyID: 48543605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2249ea154ac40b9114dd3dab8006a6d26539adff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605659"
---
# <a name="datafactory-object-rdsserver"></a><span data-ttu-id="adaf7-102">DataFactory, objet (RDSServer)</span><span class="sxs-lookup"><span data-stu-id="adaf7-102">DataFactory Object (RDSServer)</span></span>


<span data-ttu-id="adaf7-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="adaf7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="adaf7-104">Cet objet métier côté serveur par défaut implémente des méthodes qui procurent un accès en lecture-écriture aux sources de données spécifiées pour des applications côté client.</span><span class="sxs-lookup"><span data-stu-id="adaf7-104">This default server-side business object implements methods that provide read/write data access to specified data sources for client-side applications.</span></span>

## <a name="remarks"></a><span data-ttu-id="adaf7-105">Notes</span><span class="sxs-lookup"><span data-stu-id="adaf7-105">Remarks</span></span>

<span data-ttu-id="adaf7-106"><<<<<<< Tête de l’objet **RDSServer.DataFactory** est conçu comme un objet Automation côté serveur qui reçoit les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="adaf7-106"><<<<<<< HEAD The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="adaf7-107">Dans une implémentation Internet, il réside sur un serveur Web et est instancié par le composant ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="adaf7-107">In an Internet implementation, it resides on a Web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="adaf7-108">L'objet **RDSServer.DataFactory** fournit un accès en lecture-écriture aux sources de données spécifiées, mais ne contient pas de logique de validation ou de règles métier.</span><span class="sxs-lookup"><span data-stu-id="adaf7-108">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="adaf7-p102">Si vous utilisez une méthode disponible à la fois pour les objets **RDSServer.DataFactory** et [RDS.DataControl](datacontrol-object-rds.md), Remote Data Service utilise la version **RDS.DataControl** par défaut. Un scénario de programmation de base est pris comme point de départ par défaut, **RDSServer.DataFactory** étant utilisé comme objet métier côté serveur générique.</span><span class="sxs-lookup"><span data-stu-id="adaf7-p102">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<a name="if-you-want-your-web-application-to-handle-task-specific-server-side-processing-you-can-replace-the-rdsserverdatafactory-with-a-custom-business-object"></a><span data-ttu-id="adaf7-111">Si vous voulez que votre application Web gère le traitement spécifique des tâches côté serveur, vous pouvez remplacer **RDSServer.DataFactory** par un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="adaf7-111">If you want your Web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
=======
<span data-ttu-id="adaf7-112">L'objet **RDSServer.DataFactory** est conçu comme un objet Automation côté serveur, qui reçoit les demandes clientes.</span><span class="sxs-lookup"><span data-stu-id="adaf7-112">The **RDSServer.DataFactory** object is designed as a server-side Automation object that receives client requests.</span></span> <span data-ttu-id="adaf7-113">Dans une implémentation Internet, il réside sur un serveur web et est instancié par le composant ADISAPI.</span><span class="sxs-lookup"><span data-stu-id="adaf7-113">In an Internet implementation, it resides on a web server and is instantiated by the ADISAPI component.</span></span> <span data-ttu-id="adaf7-114">L'objet **RDSServer.DataFactory** fournit un accès en lecture-écriture aux sources de données spécifiées, mais ne contient pas de logique de validation ou de règles métier.</span><span class="sxs-lookup"><span data-stu-id="adaf7-114">The **RDSServer.DataFactory** object provides read and write access to specified data sources, but doesn't contain any validation or business rules logic.</span></span>

<span data-ttu-id="adaf7-p104">Si vous utilisez une méthode disponible à la fois pour les objets **RDSServer.DataFactory** et [RDS.DataControl](datacontrol-object-rds.md), Remote Data Service utilise la version **RDS.DataControl** par défaut. Un scénario de programmation de base est pris comme point de départ par défaut, **RDSServer.DataFactory** étant utilisé comme objet métier côté serveur générique.</span><span class="sxs-lookup"><span data-stu-id="adaf7-p104">If you use a method that is available in both the **RDSServer.DataFactory** and [RDS.DataControl](datacontrol-object-rds.md) objects, Remote Data Service uses the **RDS.DataControl** version by default. The default assumes a basic programming scenario, where the **RDSServer.DataFactory** serves as a generic server-side business object.</span></span>

<span data-ttu-id="adaf7-117">Si vous souhaitez que votre application web gère le traitement du côté serveur spécifiques à la tâche, vous pouvez remplacer **RDSServer.DataFactory** par un objet métier personnalisé.</span><span class="sxs-lookup"><span data-stu-id="adaf7-117">If you want your web application to handle task-specific server-side processing, you can replace the **RDSServer.DataFactory** with a custom business object.</span></span>
>>>>>>> <span data-ttu-id="adaf7-118">master</span><span class="sxs-lookup"><span data-stu-id="adaf7-118">master</span></span>

<span data-ttu-id="adaf7-p105">Vous pouvez créer des objets métier côté serveur qui appellent les méthodes de **RDSServer.DataFactory**, comme [Query](query-method-rds.md) et [CreateRecordset](createrecordset-method-rds.md). Cela s'avère utile si vous voulez ajouter des fonctionnalités à vos objets métier tout en profitant des technologies Remote Data Service existantes.</span><span class="sxs-lookup"><span data-stu-id="adaf7-p105">You can create server-side business objects that call the **RDSServer.DataFactory** methods, such as [Query](query-method-rds.md) and [CreateRecordset](createrecordset-method-rds.md). This is helpful if you want to add functionality to your business objects, but take advantage of existing Remote Data Service technologies.</span></span>

<span data-ttu-id="adaf7-121">L'identificateur de classe de l'objet **RDSServer.DataFactory** est 9381D8F5-0288-11D0-9501-00AA00B911A5.</span><span class="sxs-lookup"><span data-stu-id="adaf7-121">The class ID for the **RDSServer.DataFactory** object is 9381D8F5-0288-11D0-9501-00AA00B911A5.</span></span>

