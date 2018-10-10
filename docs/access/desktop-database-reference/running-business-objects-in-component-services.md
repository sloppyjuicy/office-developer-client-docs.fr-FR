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
# <a name="running-business-objects-in-component-services"></a>Exécution d'objets métier dans les services de composants


**S’applique à**: Access 2013 | Office 2013

Les objets métier peuvent représenter des fichiers exécutables (.exe) ou des bibliothèques de liens dynamiques (.dll). La configuration que vous utilisez pour exécuter l'objet métier varie selon qu'il s'agit d'un fichier .dll ou d'un fichier .exe :

  - Les objets métier créés sous forme de fichiers .exe peuvent être appelés via DCOM. S'ils sont utilisés par l'intermédiaire d'Internet Information Services (IIS), ils font l'objet d'un marshaling de données supplémentaire, ce qui ralentit les performances du client.

  - Les objets métier créés en tant que fichiers .dll peuvent être utilisés via IIS (et par conséquent HTTP). Ils peuvent également être utilisés avec DCOM, mais uniquement en passant par les services de composants (ou par Microsoft Transaction Server si vous utilisez Windows NT). Les DLL de l'objet métier doivent être inscrites sur le serveur IIS pour permettre l'accès via IIS. (Pour connaître les étapes nécessaires à la configuration d'une DLL utilisable avec DCOM, consultez la section « [Configuration d'une DLL pour son exécution sur DCOM](enabling-a-dll-to-run-on-dcom.md) ».)


> [!NOTE]
> <P>Lorsque la couche intermédiaire des objets métier sont implémentées en tant que les composants de Services de composants (à l’aide de <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>et <STRONG>SetAbort</STRONG>), ils peuvent utiliser les Services de composants (ou MTS, si vous utilisez Windows NT) contexte des objets à mettre à jour leur état entre plusieurs appels clients. Ce cas de figure, généralement implémenté entre des clients et des serveurs de confiance (dans un intranet), est possible grâce à DCOM. L'objet <A href="dataspace-object-rds.md">RDS.DataSpace</A> et la méthode <A href="createobject-method-rds.md">CreateObject</A> sur le client sont remplacés par l'objet de contexte de transaction et la méthode <STRONG>CreateInstance</STRONG> (fournie par l'interface <STRONG>ITransactionContext</STRONG> ) est implémentée par les services de composants.</P>


