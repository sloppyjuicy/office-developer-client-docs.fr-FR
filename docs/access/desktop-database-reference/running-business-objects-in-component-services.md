---
title: Exécution d'objets métier dans les services de composants
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41424fd62e915ecb2d54fdb49c939b788f458804
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470296"
---
# <a name="running-business-objects-in-component-services"></a><span data-ttu-id="03d13-102">Exécution d'objets métier dans les services de composants</span><span class="sxs-lookup"><span data-stu-id="03d13-102">Running Business Objects in Component Services</span></span>


<span data-ttu-id="03d13-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="03d13-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="03d13-p101">Les objets métier peuvent représenter des fichiers exécutables (.exe) ou des bibliothèques de liens dynamiques (.dll). La configuration que vous utilisez pour exécuter l'objet métier varie selon qu'il s'agit d'un fichier .dll ou d'un fichier .exe :</span><span class="sxs-lookup"><span data-stu-id="03d13-p101">Business objects can be executable files (.exe) or dynamic-link libraries (.dll). The configuration you use to run the business object depends on whether the object is a .dll or .exe file:</span></span>

  - <span data-ttu-id="03d13-p102">Les objets métier créés sous forme de fichiers .exe peuvent être appelés via DCOM. S'ils sont utilisés par l'intermédiaire d'Internet Information Services (IIS), ils font l'objet d'un marshaling de données supplémentaire, ce qui ralentit les performances du client.</span><span class="sxs-lookup"><span data-stu-id="03d13-p102">Business objects created as .exe files can be called through DCOM. If these business objects are used through Internet Information Services (IIS), they are subject to additional marshalingof data, which will slow client performance.</span></span>

  - <span data-ttu-id="03d13-p103">Les objets métier créés en tant que fichiers .dll peuvent être utilisés via IIS (et par conséquent HTTP). Ils peuvent également être utilisés avec DCOM, mais uniquement en passant par les services de composants (ou par Microsoft Transaction Server si vous utilisez Windows NT). Les DLL de l'objet métier doivent être inscrites sur le serveur IIS pour permettre l'accès via IIS. (Pour connaître les étapes nécessaires à la configuration d'une DLL utilisable avec DCOM, consultez la section « [Configuration d'une DLL pour son exécution sur DCOM](enabling-a-dll-to-run-on-dcom.md) ».)</span><span class="sxs-lookup"><span data-stu-id="03d13-p103">Business objects created as .dll files can be used via IIS (and therefore HTTP). They can also be used over DCOM only via Component Services (or Microsoft Transaction Server, if you are using Windows NT). Business object DLLs will need to be registered on the IIS server computer to give you accessibility via IIS. (For steps on how to configure a DLL to run on DCOM, see the section, "[Enabling a DLL to Run on DCOM](enabling-a-dll-to-run-on-dcom.md).")</span></span>


> [!NOTE]
> <P><span data-ttu-id="03d13-112">Lorsque la couche intermédiaire des objets métier sont implémentées en tant que les composants de Services de composants (à l’aide de <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>et <STRONG>SetAbort</STRONG>), ils peuvent utiliser les Services de composants (ou MTS, si vous utilisez Windows NT) contexte des objets à mettre à jour leur état entre plusieurs appels clients.</span><span class="sxs-lookup"><span data-stu-id="03d13-112">When business objects on the middle tier are implemented as Component Services components (using <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>, and <STRONG>SetAbort</STRONG>), they can use Component Services (or MTS, if you are using Windows NT) context objects to maintain their state across multiple client calls.</span></span> <span data-ttu-id="03d13-113">Ce cas de figure, généralement implémenté entre des clients et des serveurs de confiance (dans un intranet), est possible grâce à DCOM.</span><span class="sxs-lookup"><span data-stu-id="03d13-113">This scenario is possible with DCOM, which is typically implemented between trusted clients and servers (an intranet).</span></span> <span data-ttu-id="03d13-114">L'objet <A href="dataspace-object-rds.md">RDS.DataSpace</A> et la méthode <A href="createobject-method-rds.md">CreateObject</A> sur le client sont remplacés par l'objet de contexte de transaction et la méthode <STRONG>CreateInstance</STRONG> (fournie par l'interface <STRONG>ITransactionContext</STRONG> ) est implémentée par les services de composants.</span><span class="sxs-lookup"><span data-stu-id="03d13-114">In this case, the <A href="dataspace-object-rds.md">RDS.DataSpace</A> object and <A href="createobject-method-rds.md">CreateObject</A> method on the client side are replaced by the transaction context object and <STRONG>CreateInstance</STRONG> method (provided by the <STRONG>ITransactionContext</STRONG> interface), implemented by Component Services.</span></span></P>


