---
title: Exécution d'objets métier dans les services de composants
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c398dc0733b58c72fb021c104eaf1a546fd9c66a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881677"
---
# <a name="running-business-objects-in-component-services"></a>Exécution d'objets métier dans les services de composants


**S’applique à**: Access 2013, Office 2013

Les objets métier peuvent représenter des fichiers exécutables (.exe) ou des bibliothèques de liens dynamiques (.dll). La configuration que vous utilisez pour exécuter l'objet métier varie selon qu'il s'agit d'un fichier .dll ou d'un fichier .exe :

  - Les objets métier créés sous forme de fichiers .exe peuvent être appelés via DCOM. S'ils sont utilisés par l'intermédiaire d'Internet Information Services (IIS), ils font l'objet d'un marshaling de données supplémentaire, ce qui ralentit les performances du client.

  - Les objets métier créés en tant que fichiers .dll peuvent être utilisés via IIS (et par conséquent HTTP). Ils peuvent également être utilisés avec DCOM, mais uniquement en passant par les services de composants (ou par Microsoft Transaction Server si vous utilisez Windows NT). Les DLL de l'objet métier doivent être inscrites sur le serveur IIS pour permettre l'accès via IIS. (Pour connaître les étapes nécessaires à la configuration d'une DLL utilisable avec DCOM, consultez la section « [Configuration d'une DLL pour son exécution sur DCOM](enabling-a-dll-to-run-on-dcom.md) ».)


> [!NOTE]
> Lorsque la couche intermédiaire des objets métier sont implémentées en tant que les composants de Services de composants (à l’aide de **GetObjectContext**, **SetComplete**et **SetAbort**), ils peuvent utiliser les Services de composants (ou MTS, si vous utilisez Windows NT) contexte des objets à mettre à jour leur état entre plusieurs appels clients. Ce cas de figure, généralement implémenté entre des clients et des serveurs de confiance (dans un intranet), est possible grâce à DCOM. 
>
> L'objet [RDS.DataSpace](dataspace-object-rds.md) et la méthode [CreateObject](createobject-method-rds.md) sur le client sont remplacés par l'objet de contexte de transaction et la méthode **CreateInstance** (fournie par l'interface **ITransactionContext** ) est implémentée par les services de composants.


## <a name="see-also"></a>Voir aussi

- [Exécution des objets métier dans les Services de composants (SQL Server)](https://docs.microsoft.com/sql/ado/guide/remote-data-service/running-business-objects-in-component-services?view=sql-server-2017)