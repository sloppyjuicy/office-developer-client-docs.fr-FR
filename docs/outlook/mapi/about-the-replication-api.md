---
title: À propos de l’API de réplication
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: 'Dernière modification : 25 juin 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396056"
---
# <a name="about-the-replication-api"></a>À propos de l’API de réplication

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’API de réplication fournit les fonctionnalités pour un fournisseur de magasin de message MAPI synchroniser des éléments Microsoft Outlook 2013 ou Microsoft Outlook 2010 entre un serveur et un magasin local privé basée sur .pst est créé pour ce fournisseur. 
  
> [!NOTE]
> Un fournisseur de magasins de message MAPI doit implémenter l’API de réplication conformément aux instructions de [L’ordinateur d’état de réplication](about-the-replication-state-machine.md). Le fournisseur doit utiliser l’API uniquement sur un magasin personnel créé pour lui-même et pas sur les banques d’informations personnelles créés pour d’autres fournisseurs, car les banques d’informations personnelles créées pour d’autres fournisseurs déjà configuré leurs propres mécanismes de réplication avec le serveur respectif. Par exemple, un fichier de dossiers en mode hors connexion (.ost) conserve sa propre relation de réplication avec un serveur Microsoft Exchange. 
  
Pour utiliser l’API de réplication, un fournisseur de magasins de message MAPI doit tout d’abord ouvrir et renvoyer un magasin local .pst en appelant **[NSTServiceEntry](nstserviceentry.md)**. Le fournisseur peut utiliser ensuite les interfaces principales des API, **[IOSTX](iostxiunknown.md)** et **[IPSTX](ipstxiunknown.md)**, pour effectuer la réplication. **IPSTX** est fourni par l’interrogation [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), et **IOSTX** est fourni par **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**. 
  
## <a name="the-iostx-interface"></a>L’Interface IOSTX

L’interface **IOSTX** est l’interface principale qui effectue la synchronisation de l’API de réplication. **IOSTX** déplace le magasin local à travers une série d’états, récupération des informations sur les modifications dans le magasin local dans chaque état, ainsi que pour informer le magasin des modifications sur le serveur local. L’API de réplication spécifie également de nombreuses structures de données qui prennent en charge la synchronisation. 
  
Un fournisseur de magasins, en tant que client à cette API, utilise l’API de réplication pour encapsuler le magasin local et déplacer par le biais de ces États, envoi de modifications dans le magasin local (tel que les modifications à la hiérarchie de dossiers ou l’ajout de nouveaux éléments) pour le serveur et en les extrayant également informations sur les modifications sur le serveur et fournit des informations à l’interface **IOSTX** . L’interface **IOSTX** adopte la synchronisation de modification incrémentielle (ICS) fourni par Microsoft Exchange Server. Pour plus d’informations sur le partage de connexion Internet, voir [Critères d’évaluation de partage de connexion Internet](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx). Par le biais **IOSTX**, le client utilise ICS pour surveiller et synchroniser les modifications incrémentielles apportées à la hiérarchie ou du contenu sur un magasin local. 
  
## <a name="the-ipstx-interface"></a>L’Interface IPSTX

 **IPSTX** et cinq autres ** IPSTX *n* ** interfaces qui héritent de **IPSTX** fournissent des fonctionnalités d’assistance qui peuvent être utilisée lors de l’exécution de la réplication via l’interface **IOSTX** . Par exemple, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permet de rendre la banque locale émuler le Gestionnaire de protocole Outlook pour mettre en attente des messages sortants vers un serveur. 
  
Pour plus d’informations sur les transitions d’état lors de la réplication, consultez la rubrique [Sur l’ordinateur d’état de réplication](about-the-replication-state-machine.md).
  
## <a name="the-replication-api"></a>L’API de réplication

L’API de réplication fournit les définitions, les types de données et les interfaces suivantes. Pour un exemple d’implémentation d’un fournisseur de magasin de fichiers encapsulés de dossiers personnels (PST), voir [Sur l’exemple encapsulé PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).
  
Définitions :
  
- [Constantes pour l’API de réplication](mapi-constants.md)
    
Fonctions :
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
Types de données :
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
Interfaces :
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

