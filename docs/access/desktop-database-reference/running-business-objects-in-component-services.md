---
title: Exécution des objets métiers dans les services de composants
TOCTitle: Running business objects in component services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23cb90161e5e0728aa652ae5d496216676f781a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309204"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="408b1-102">Exécution des objets métiers dans les services de composants</span><span class="sxs-lookup"><span data-stu-id="408b1-102">Running business objects in component services</span></span>

<span data-ttu-id="408b1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="408b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="408b1-p101">Les objets métier peuvent représenter des fichiers exécutables (.exe) ou des bibliothèques de liens dynamiques (.dll). La configuration que vous utilisez pour exécuter l'objet métier varie selon qu'il s'agit d'un fichier .dll ou d'un fichier .exe :</span><span class="sxs-lookup"><span data-stu-id="408b1-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

- <span data-ttu-id="408b1-p102">Les objets métier créés sous forme de fichiers .exe peuvent être appelés via DCOM. S'ils sont utilisés par l'intermédiaire d'Internet Information Services (IIS), ils font l'objet d'un marshaling de données supplémentaire, ce qui ralentit les performances du client.</span><span class="sxs-lookup"><span data-stu-id="408b1-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

- <span data-ttu-id="408b1-p103">Les objets métier créés en tant que fichiers .dll peuvent être utilisés via IIS (et par conséquent HTTP). Ils peuvent également être utilisés avec DCOM, mais uniquement en passant par les services de composants (ou par Microsoft Transaction Server si vous utilisez Windows NT). Les DLL de l'objet métier doivent être inscrites sur le serveur IIS pour permettre l'accès via IIS. (Pour connaître les étapes nécessaires à la configuration d'une DLL utilisable avec DCOM, consultez la section « [Configuration d'une DLL pour son exécution sur DCOM](enabling-a-dll-to-run-on-dcom.md) ».)</span><span class="sxs-lookup"><span data-stu-id="408b1-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <span data-ttu-id="408b1-112">Lorsque les objets métier du niveau intermédiaire sont implémentés en tant que composants des services de composants (à l’aide de **GetObjectContext,** **SetComplete** et **SetAbort),** ils peuvent utiliser des objets de contexte des services de composants (ou MTS, si vous utilisez Windows NT) pour maintenir leur état dans plusieurs appels clients.</span><span class="sxs-lookup"><span data-stu-id="408b1-112">When business objects on the middle tier are implemented as Component Services components (using **GetObjectContext**, **SetComplete**, and **SetAbort**), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="408b1-113">Ce cas de figure, généralement implémenté entre des clients et des serveurs de confiance (dans un intranet), est possible grâce à DCOM.</span><span class="sxs-lookup"><span data-stu-id="408b1-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> 
>
> <span data-ttu-id="408b1-114">L'objet [RDS.DataSpace](dataspace-object-rds.md) et la méthode [CreateObject](createobject-method-rds.md) sur le client sont remplacés par l'objet de contexte de transaction et la méthode **CreateInstance** (fournie par l'interface **ITransactionContext** ) est implémentée par les services de composants.</span><span class="sxs-lookup"><span data-stu-id="408b1-114">In this case, the [RDS.DataSpace](dataspace-object-rds.md) object and [CreateObject](createobject-method-rds.md) method on the client side are replaced by the transaction context object and **CreateInstance** method (provided by the **ITransactionContext** interface), implemented by Component Services.</span></span>


## <a name="see-also"></a><span data-ttu-id="408b1-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="408b1-115">See also</span></span>

- [<span data-ttu-id="408b1-116">Exécution des objets métier dans les services de composants (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="408b1-116">Running Business Objects in Component Services (SQL Server)</span></span>](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)
